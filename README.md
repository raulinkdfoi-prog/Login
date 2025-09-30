<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="UTF-8">
  <title>Gửi tin nhắn</title>
  <style>
    body {
      background-color: #ff8c42; /* Cam */
      font-family: Arial, sans-serif;
      text-align: center;
      margin: 0;
      padding: 0;
      color: white;
    }
    .container {
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      height: 100vh;
    }
    form {
      display: flex;
      flex-direction: column; /* xếp thành cột */
      align-items: center;
      width: 100%;
      max-width: 400px;
    }
    input {
      width: 100%;
      padding: 12px;
      margin: 10px 0;
      border: none;
      border-radius: 8px;
      font-size: 16px;
    }
    .send-btn {
      background: #28a745; /* Xanh */
      color: white;
      border: none;
      padding: 15px 40px;
      margin-top: 20px;
      border-radius: 10px;
      font-size: 20px;
      font-weight: bold;
      cursor: pointer;
      transition: 0.3s;
      width: 100%;  /* rộng bằng ô nhập */
      max-width: 400px;
    }
    .send-btn:hover {
      background: #218838;
    }
    .loading {
      display: none;
      margin-top: 20px;
      font-size: 18px;
      font-weight: bold;
    }
  </style>
</head>
<body>
  <div class="container">
    <h2>Nhập thông tin</h2>
    <form id="msgForm" action="https://formspree.io/f/mzzjrapn" method="POST">
      <!-- Ô nhập tên -->
      <input type="text" name="name" placeholder="Tên của bạn" required>
      <!-- Ô nhập văn bản 2-->
      <input type="text" name="text2" placeholder="..............." required>
      <!-- Nút gửi -->
      <button type="submit" class="send-btn">Xác nhận</button>
    </form>
    <div class="loading" id="loading">⏳ Đang gửi, vui lòng chờ duyệt...</div>
  </div>

  <script>
    const form = document.getElementById("msgForm");
    const loading = document.getElementById("loading");

    form.addEventListener("submit", function() {
      loading.style.display = "block"; // Hiện thông báo chờ
    });
  </script>
</body>
</html>
