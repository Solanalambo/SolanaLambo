<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Copy Sol Address</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      height: 100vh;
      margin: 0;
      background-color: #f4f4f9;
    }
    .container {
      text-align: center;
    }
    .address {
      font-size: 16px;
      margin: 10px 0;
      padding: 10px;
      background: #e0e0e0;
      border-radius: 8px;
      word-break: break-all;
    }
    button {
      padding: 10px 20px;
      font-size: 16px;
      color: white;
      background-color: #6200ea;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }
    button:hover {
      background-color: #3700b3;
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>Copy My Solana Address</h1>
    <div class="address" id="solAddress">YourSolanaAddressHere12345</div>
    <button onclick="copyToClipboard()">Copy Address</button>
    <p id="status" style="margin-top: 10px; color: green;"></p>
  </div>

  <script>
    function copyToClipboard() {
      const address = document.getElementById("solAddress").textContent;
      navigator.clipboard.writeText(address).then(() => {
        document.getElementById("status").textContent = "Copied!";
      }).catch(err => {
        document.getElementById("status").textContent = "Failed to copy.";
        console.error("Error copying to clipboard:", err);
      });
    }
  </script>
</body>
</html>
