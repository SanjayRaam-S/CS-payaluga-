<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>BSc Computer Science</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      background: black;
      color: #00ffcc;
      font-family: 'Courier New', Courier, monospace;
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
      text-align: center;
      overflow: hidden; /* corrected */
    }

    .section {
      display: none;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      height: 100%;
      width: 100%;
      animation: fadeIn 1s ease forwards;
    }

    .active {
      display: flex;
    }

    h1, h2 {
      opacity: 0;
      transform: translateY(50px);
      animation: fadeInUp 2s ease forwards;
    }

    h1 {
      font-size: 3rem;
      animation-delay: 1s;
    }

    h2 {
      font-size: 1.5rem;
      animation-delay: 3s;
    }

    .glow {
      text-shadow: 0 0 5px #00ffcc, 0 0 20px #00ffcc;
    }

    .button {
      margin-top: 40px;
      padding: 15px 30px;
      font-size: 1rem;
      color: #000;
      background-color: #00ffcc;
      border: none;
      border-radius: 10px;
      cursor: pointer;
      box-shadow: 0 0 10px #00ffcc, 0 0 30px #00ffcc;
      transition: background 0.3s ease, transform 0.2s ease;
      opacity: 0;
      animation: fadeInUp 2s ease forwards;
      animation-delay: 5s;
    }

    .button:hover {
      background-color: #00e6b8;
      transform: scale(1.05);
    }

    @keyframes fadeInUp {
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    @keyframes fadeIn {
      from {
        opacity: 0;
        transform: scale(0.95);
      }
      to {
        opacity: 1;
        transform: scale(1);
      }
    }

    @media (max-width: 600px) {
      h1 {
        font-size: 2rem;
      }

      h2 {
        font-size: 1.2rem;
      }

      .button {
        padding: 12px 25px;
        font-size: 0.9rem;
      }
    }
  </style>
</head>
<body>
  <!-- Welcome Section -->
  <div class="section active" id="welcome">
    <h1 class="glow">Welcome to Our Classroom</h1>
    <h2 class="glow">BSc ComputerScience (Payaluga 🕺💃)</h2>
    <button class="button" onclick="showTutor()">Enter Classroom</button>
  </div>

  <!-- Tutor Section -->
  <div class="section" id="tutor">
    <h2 class="glow">Class Tutor: Mrs Dr. Sridevi</h2>
    <h1 class="glow">Head of Department: Mrs Dr. Deepa</h1>
  </div>

  <script>
    function showTutor() {
      document.getElementById('welcome').classList.remove('active');
      document.getElementById('tutor').classList.add('active');
    }
    
  </script>
</body>
</html>
