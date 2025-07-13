# prank-hack
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Warning!</title>
  <style>
    body {
      background-color: black;
      color: red;
      text-align: center;
      font-family: 'Courier New', Courier, monospace;
      padding-top: 100px;
      animation: blinkBackground 0.5s infinite;
    }

    h1 {
      font-size: 30px;
      animation: blinkText 1s infinite;
    }

    #countdown {
      font-size: 50px;
      margin-top: 40px;
      color: white;
    }

    @keyframes blinkBackground {
      0% { background-color: black; }
      50% { background-color: darkred; }
      100% { background-color: black; }
    }

    @keyframes blinkText {
      0% { opacity: 1; }
      50% { opacity: 0; }
      100% { opacity: 1; }
    }
  </style>
</head>
<body>
  <h1>⚠️ Your Phone Will Be Hacked In <span id="countdown">15</span> Seconds! ⚠️</h1>

  <script>
    let count = 15;
    const countdownEl = document.getElementById('countdown');

    const interval = setInterval(() => {
      count--;
      if (count >= 0) {
        countdownEl.textContent = count;
      } else {
        clearInterval(interval);
        countdownEl.textContent = '💀 Hacked! 💀';
        document.body.style.backgroundColor = 'red';
        document.body.style.color = 'black';
      }
    }, 1000);
  </script>
</body>
</html>
