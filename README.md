<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    body {
      font-family: 'Arial', sans-serif;
      text-align: center;
      margin-top: 100px;
      background-color: #ffe6f2; /* Rose pâle */
    }

    #question {
      font-size: 24px;
      margin-bottom: 20px;
      color: #ff66b2; /* Rose vif */
    }

    #buttons {
      display: flex;
      justify-content: center;
    }

    button {
      padding: 10px 20px;
      font-size: 18px;
      margin: 0 10px;
      cursor: pointer;
      background-color: #ff99cc; /* Rose moyen */
      border: none;
      color: white;
      border-radius: 5px;
      transition: transform 0.3s ease-in-out;
    }

    #noButton:hover {
      transform: translate(
        ${(Math.random() * 200 - 100).toFixed(2)}px,
        ${(Math.random() * 200 - 100).toFixed(2)}px
      );
    }
  </style>
  <script>
    function showAlert(message) {
      alert(message);
    }
  </script>
</head>
<body>

  <div id="question">Will you marry me?</div>

  <div id="buttons">
    <button onclick="showAlert('Congratulations!')">YES</button>
    <button id="noButton" onmouseover="moveNoButton()">NO</button>
  </div>

  <script>
    function moveNoButton() {
      document.getElementById('noButton').style.transform = `translate(
        ${(Math.random() * 200 - 100).toFixed(2)}px,
        ${(Math.random() * 200 - 100).toFixed(2)}px
      )`;
    }
  </script>
</body>
</html>
