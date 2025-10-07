<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Thế giới của anh 💞</title>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;600&display=swap');
    body {
      margin: 0;
      height: 100vh;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      background: linear-gradient(-45deg, #000000, #1a0033, #6600ff, #ff0099);
      background-size: 400% 400%;
      animation: gradient 8s ease infinite;
      font-family: 'Poppins', sans-serif;
      color: white;
      overflow: hidden;
    }

    @keyframes gradient {
      0% {background-position: 0% 50%;}
      50% {background-position: 100% 50%;}
      100% {background-position: 0% 50%;}
    }

    h1 {
      font-size: 2em;
      margin-bottom: 40px;
      text-shadow: 0 0 20px #ff66cc;
    }

    .buttons {
      display: flex;
      gap: 30px;
    }

    button {
      padding: 15px 30px;
      font-size: 1.1em;
      border: none;
      border-radius: 30px;
      cursor: pointer;
      color: white;
      font-weight: 600;
      transition: 0.3s;
    }

    #yesBtn {
      background: linear-gradient(45deg, #ff00cc, #3333ff);
      box-shadow: 0 0 20px #ff00cc;
    }

    #yesBtn:hover {
      transform: scale(1.1);
      box-shadow: 0 0 30px #ff33cc;
    }

    #noBtn {
      background: linear-gradient(45deg, #444, #111);
      box-shadow: 0 0 10px #000;
      position: relative;
    }

    #message {
      margin-top: 40px;
      font-size: 1.5em;
      text-align: center;
      opacity: 0;
      transition: opacity 1s ease;
    }
  </style>
</head>
<body>

  <h1>Thế giới của anh 💞</h1>
  <div class="buttons">
    <button id="yesBtn">Ở lại với anh 💘</button>
    <button id="noBtn">Rời đi 😢</button>
  </div>
  <div id="message">Anh biết mà 💞 Em chính là định mệnh của anh 💖</div>

  <!-- 🎵 Nhạc nền tự phát từ khi mở trang -->
  <audio id="bgMusic" autoplay loop>
    <source src="https://cdn.pixabay.com/audio/2023/03/23/audio_8b1f6c6d89.mp3" type="audio/mpeg">
  </audio>

  <script>
    const yesBtn = document.getElementById("yesBtn");
    const noBtn = document.getElementById("noBtn");
    const message = document.getElementById("message");
    const music = document.getElementById("bgMusic");

    // Một số trình duyệt chặn autoplay — bật nếu người dùng có tương tác đầu tiên
    document.addEventListener("click", () => {
      music.play().catch(() => {});
    }, { once: true });

    yesBtn.addEventListener("click", () => {
      message.style.opacity = 1;
      setTimeout(() => {
        // 👉 ĐỔI LINK FACEBOOK CỦA BẠN TẠI DÒNG NÀY
        window.location.href = "https://www.facebook.com/hieu.duong.513245";
      }, 3000);
    });

    // Nút "Rời đi" chạy trốn khi rê chuột vào
    noBtn.addEventListener("mouseover", () => {
      const x = Math.random() * (window.innerWidth - 150);
      const y = Math.random() * (window.innerHeight - 150);
      noBtn.style.position = "absolute";
      noBtn.style.left = `${x}px`;
      noBtn.style.top = `${y}px`;
    });
  </script>

</body>
</html>
