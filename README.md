<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Valentine Message</title>
  <style>
    * {
      box-sizing: border-box;
    }

    body {
      margin: 0;
      padding: 0;
      font-family: sans-serif;
      background-color: #f8f8f8;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      height: 100vh;
      overflow: hidden;
      position: relative;
    }

    h2 {
      color: #e63946;
      margin-top: 20px;
    }

    #image-container {
      display: flex;
      justify-content: center;
      align-items: center;
      margin-top: 20px;
    }

    #image {
      width: 200px;
      display: block;
    }

    .btn {
      padding: 10px 30px;
      border-radius: 20px;
      border: 2px solid #e63946;
      font-weight: bold;
      cursor: pointer;
      transition: transform 0.3s ease;
      font-size: 16px;
    }

    .btn:hover {
      transform: scale(1.05);
    }

    .yes {
      background-color: #e63946;
      color: white;
      margin-right: 20px;
    }

    .no {
      background-color: white;
      color: #e63946;
      cursor: not-allowed; /* Disables clicking */
    }

    .button-container {
      display: flex;
      justify-content: center;
      gap: 20px;
      margin-top: 20px;
    }
  </style>
</head>
<body>

  <h2 id="message">Will You Be My Valentine?</h2>
  <div id="image-container">
    <img id="image" src="https://media.giphy.com/media/5GoVLqeAOo6PK/giphy.gif" alt="Heart Balloon" />
  </div>

  <div class="button-container">
    <button class="btn yes" id="yesBtn" onclick="sayYes()">Yes</button>
    <button class="btn no" id="noBtn" disabled>No</button> <!-- Disabled No button -->
  </div>

  <script>
    const yesBtn = document.getElementById("yesBtn");
    const noBtn = document.getElementById("noBtn");
    const image = document.getElementById("image");
    const message = document.getElementById("message");

    function sayYes() {
      message.innerText = "Yay! ❤️";
      image.style.display = "none";
      yesBtn.style.display = "none";
      noBtn.style.display = "none"; // Hide both buttons after Yes is clicked
    }

    // The "No" button does nothing now since it's disabled.
  </script>

</body>
</html>
