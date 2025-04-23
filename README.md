<!DOCTYPE html><html lang="tr">
<head>
  <meta charset="UTF-8">
  <title>cvnexe</title>
  <style>
    body {
      margin: 0;
      background-color: black;
      overflow: hidden;
      font-family: Arial, sans-serif;
    }
    #startBtn {
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      padding: 20px 40px;
      font-size: 24px;
      background-color: white;
      border: none;
      cursor: pointer;
      border-radius: 10px;
      z-index: 10;
    }
    .neon-line {
      position: absolute;
      width: 100%;
      height: 4px;
      background: linear-gradient(to right, cyan, magenta);
      animation: moveNeon 1s linear forwards;
    }
    @keyframes moveNeon {
      0% { top: 0; opacity: 0; }
      100% { top: 100%; opacity: 1; }
    }
    .text-container {
      position: absolute;
      top: 0;
      width: 100%;
      height: 100%;
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
      gap: 20px;
      color: white;
      font-size: 36px;
      z-index: 5;
    }
    .text {
      opacity: 0;
      position: relative;
      font-weight: bold;
    }
    .text.red {
      color: red;
    }
    .text.black {
      color: black;
      text-shadow: 0 0 10px white;
    }
    @keyframes slideTop {
      0% { top: -100px; opacity: 0; }
      100% { top: 0; opacity: 1; }
    }
    @keyframes slideBottom {
      0% { top: 100px; opacity: 0; }
      100% { top: 0; opacity: 1; }
    }
    @keyframes zoomIn {
      0% { transform: scale(0); opacity: 0; }
      100% { transform: scale(1); opacity: 1; }
    }
    .heart {
      font-size: 80px;
      animation: zoomIn 1s ease forwards;
      opacity: 0;
    }
  </style>
</head>
<body>
  <button id="startBtn">Başla</button>
  <div class="text-container" id="textContainer" style="display:none">
    <div class="text red" id="t1">Vxgh</div>
    <div class="text black" id="t2">Ehq</div>
    <div class="text red" id="t3">Vhql</div>
    <div class="text black" id="t4">Frn</div>
    <div class="text red" id="t5">Özohglp</div>
    <div class="heart" id="heart">🤍</div>
  </div>  <script>
    const startBtn = document.getElementById("startBtn");
    const textContainer = document.getElementById("textContainer");

    startBtn.addEventListener("click", () => {
      startBtn.style.display = "none";
      for (let i = 0; i < 7; i++) {
        setTimeout(() => {
          const line = document.createElement("div");
          line.className = "neon-line";
          line.style.top = `${Math.random() * 100}%`;
          document.body.appendChild(line);
          setTimeout(() => line.remove(), 1000);
        }, i * 300);
      }

      setTimeout(() => {
        textContainer.style.display = "flex";
        document.getElementById("t1").style.animation = "slideTop 1s forwards";
        setTimeout(() => {
          document.getElementById("t2").style.animation = "slideBottom 1s forwards";
        }, 800);
        setTimeout(() => {
          document.getElementById("t3").style.animation = "slideTop 1s forwards";
        }, 1600);
        setTimeout(() => {
          document.getElementById("t4").style.animation = "slideBottom 1s forwards";
        }, 2400);
        setTimeout(() => {
          document.getElementById("t5").style.animation = "zoomIn 1s forwards";
        }, 3200);
        setTimeout(() => {
          document.getElementById("heart").style.animation = "zoomIn 1s forwards";
        }, 4200);
      }, 2300);
    });
  </script></body>
</html># awrda-
