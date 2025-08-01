<!DOCTYPE html>
<html lang="tr">
<head>
  <meta charset="UTF-8">
  <title>Sen Dünyanın En Güzel Kızısın</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      overflow: hidden;
      background-image: url('https://images.unsplash.com/photo-1506744038136-46273834b3fb?auto=format&fit=crop&w=1920&q=80'); /* Doğa manzarası */
      background-size: cover;
      background-position: center;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    }

    .center-text {
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      color: white;
      font-size: 48px;
      text-shadow: 2px 2px 8px rgba(0, 0, 0, 0.7);
      text-align: center;
    }

    .heart {
      position: absolute;
      width: 20px;
      height: 20px;
      background-color: red;
      transform: rotate(45deg);
      animation: float 10s linear infinite;
    }

    .heart::before,
    .heart::after {
      content: "";
      position: absolute;
      width: 20px;
      height: 20px;
      background-color: red;
      border-radius: 50%;
    }

    .heart::before {
      top: -10px;
      left: 0;
    }

    .heart::after {
      left: -10px;
      top: 0;
    }

    @keyframes float {
      0% {
        transform: translateY(100vh) rotate(45deg);
        opacity: 1;
      }
      100% {
        transform: translateY(-10vh) rotate(45deg);
        opacity: 0;
      }
    }
  </style>
</head>
<body>

  <div class="center-text">Sen dünyanın en güzel kızısın</div>

  <!-- Kalpler -->
  <script>
    const numberOfHearts = 40;

    for (let i = 0; i < numberOfHearts; i++) {
      const heart = document.createElement('div');
      heart.className = 'heart';
      heart.style.left = Math.random() * 100 + 'vw';
      heart.style.animationDuration = 5 + Math.random() * 5 + 's';
      heart.style.animationDelay = Math.random() * 10 + 's';
      document.body.appendChild(heart);
    }
  </script>

</body>
</html>
