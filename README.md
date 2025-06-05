<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Click Surprise</title>
  <style>
    body {
      background-color: #f0f0f0;
      text-align: center;
      padding-top: 100px;
      font-family: Arial, sans-serif;
    }

    #scare {
      display: none;
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: black;
      z-index: 9999;
    }

    #scare img {
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      max-width: 100%;
      max-height: 100%;
    }
  </style>
</head>
<body>

  <h1>Click the Button Below!</h1>
  <button onclick="triggerJumpScare()">Click Me</button>

  <div id="scare">
    <img src="https://i.imgur.com/6QKX3rC.png" alt="Scary Face">
    <audio id="scream" src="https://www.soundjay.com/human/sounds/scream-01.mp3"></audio>
  </div>

  <script>
    function triggerJumpScare() {
      const scareDiv = document.getElementById('scare');
      const scream = document.getElementById('scream');

      scareDiv.style.display = 'block';
      scream.play();

      // Optional: hide after 3 seconds
      setTimeout(() => {
        scareDiv.style.display = 'none';
      }, 3000);
    }
  </script>

</body>
</html>

