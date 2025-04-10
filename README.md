# Free-Fire-dimod-<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Fake Diamond Sender</title>
  <style>
    body {
      background-color: #111;
      color: white;
      font-family: Arial, sans-serif;
      text-align: center;
      padding-top: 50px;
    }

    .container {
      background-color: rgba(0, 0, 0, 0.8);
      padding: 20px;
      width: 350px;
      margin: 0 auto;
      border-radius: 12px;
      box-shadow: 0 0 25px #00ffcc;
    }

    h1 {
      color: #00ffcc;
      font-size: 22px;
    }

    input, button {
      padding: 8px;
      margin: 8px;
      width: 80%;
      font-size: 14px;
      border-radius: 6px;
    }

    button {
      background-color: #00ffcc;
      border: none;
      color: black;
      cursor: pointer;
    }

    button:hover {
      background-color: #00e6b8;
    }

    .loader {
      display: none;
      border: 12px solid #f3f3f3;
      border-top: 12px solid #00ffcc;
      border-radius: 50%;
      width: 40px;
      height: 40px;
      animation: spin 2s linear infinite;
      margin-top: 20px;
    }

    @keyframes spin {
      0% { transform: rotate(0deg); }
      100% { transform: rotate(360deg); }
    }

    .status {
      font-size: 16px;
      margin-top: 10px;
    }

  </style>
</head>
<body>

  <div class="container">
    <h1>Fake Diamond Sender</h1>
    <input type="text" id="uid" placeholder="Enter UID" />
    <input type="number" id="diamondAmount" placeholder="Enter Diamond Amount" />
    <button onclick="sendDiamonds()">Send Diamonds</button>
    <div class="loader" id="loader"></div>
    <div class="status" id="status"></div>
  </div>

  <script>
    function sendDiamonds() {
      var uid = document.getElementById('uid').value;
      var amount = document.getElementById('diamondAmount').value;

      if (!uid || !amount) {
        alert("Please fill in all fields!");
        return;
      }

      document.getElementById('status').innerText = "";
      document.getElementById('loader').style.display = "block";

      setTimeout(function() {
        document.getElementById('loader').style.display = "none";
        document.getElementById('status').innerText = "Successfully sent " + amount + " Diamonds to UID " + uid + "!";
      }, 3000);  // Simulate sending process (3 seconds)
    }
  </script>

</body>
</html>
