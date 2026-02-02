<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Valentine?</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #ffe6eb;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      text-align: center;
    }

    h1 {
      font-size: 2.5rem;
      margin-bottom: 30px;
    }

    button {
      font-size: 1.2rem;
      padding: 15px 30px;
      margin: 10px;
      border: none;
      border-radius: 10px;
      cursor: pointer;
      transition: transform 0.3s ease;
    }

    #yes {
      background-color: #ff4d6d;
      color: white;
    }

    #no {
      background-color: #ccc;
    }
  </style>
</head>
<body>
  <div>
    <h1>Will you be my Valentine? 💘</h1>
    <button id="yes">Yes ❤️</button>
    <button id="no">No 💔</button>
  </div>

  <script>
    let scale = 1;
    const yesBtn = document.getElementById("yes");
    const noBtn = document.getElementById("no");

    noBtn.addEventListener("click", () => {
      scale += 0.3;
      yesBtn.style.transform = `scale(${scale})`;

      if (scale > 3) {
        noBtn.style.display = "none";
      }
    });

    yesBtn.addEventListener("click", () => {
      document.body.innerHTML = "<h1>YAY! 💖🥰</h1>";
    });
  </script>
</body>
</html>
