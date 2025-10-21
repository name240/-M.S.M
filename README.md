
![School Logo](https://github.com/user-attachments/assets/be5ab79f-ad4b-4ab7-ad8f-3553c8dac341)

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Beautiful Logo</title>
  <style>
    body {
      margin: 0;
      height: 100vh;
      background: linear-gradient(135deg, #1e1e2f, #121212);
      display: flex;
      align-items: center;
      justify-content: center;
      overflow: hidden;
      font-family: 'Segoe UI', sans-serif;
    }

    .logo-container {
      position: relative;
      width: 200px;
      height: 200px;
      border-radius: 50%;
      background: linear-gradient(135deg, #00f2fe, #4facfe);
      box-shadow: 0 0 20px rgba(79, 172, 254, 0.8),
                  0 0 40px rgba(0, 242, 254, 0.6),
                  0 0 60px rgba(0, 242, 254, 0.4);
      display: flex;
      align-items: center;
      justify-content: center;
      animation: pulse 3s infinite;
      cursor: pointer;
    }

    .logo-text {
      font-size: 32px;
      color: white;
      font-weight: bold;
      text-shadow: 0 0 10px #fff,
                   0 0 20px #00f2fe,
                   0 0 30px #4facfe;
      transition: transform 0.3s ease;
    }

    .logo-container:hover .logo-text {
      transform: scale(1.1);
    }

    @keyframes pulse {
      0% {
        box-shadow: 0 0 20px rgba(79, 172, 254, 0.8),
                    0 0 40px rgba(0, 242, 254, 0.6),
                    0 0 60px rgba(0, 242, 254, 0.4);
      }
      50% {
        box-shadow: 0 0 30px rgba(79, 172, 254, 1),
                    0 0 60px rgba(0, 242, 254, 0.8),
                    0 0 90px rgba(0, 242, 254, 0.6);
      }
      100% {
        box-shadow: 0 0 20px rgba(79, 172, 254, 0.8),
                    0 0 40px rgba(0, 242, 254, 0.6),
                    0 0 60px rgba(0, 242, 254, 0.4);
      }
    }
  </style>
</head>
<body>

  <div class="logo-container" onclick="glowEffect()">
    <div class="logo-text"> M.S.M </div>
  </div>

  <script>
    function glowEffect() {
      const logo = document.querySelector('.logo-container');
      logo.style.animation = 'none';
      void logo.offsetWidth; // Trigger reflow
      logo.style.animation = 'pulse 3s infinite';
    }
  </script>

</body>
</html>
