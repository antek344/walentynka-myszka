<!DOCTYPE html>
<html lang="pl">
<head>
  <meta charset="UTF-8">
  <title>Valentine 💘</title>
  <style>
    body { font-family: Arial, sans-serif; text-align: center; margin-top: 40px; }
    #no { position: absolute; }
  </style>
</head>
<body>

<h2>Will you be my Valentine? 💘</h2>
<img src="love.jpg" width="250">

<button onclick="yes()">YES 💖</button>
<button id="no" onmouseover="moveNo()">NO 😜</button>

<script>
  let tries = 0;

  function yes() {
    document.body.innerHTML = "<h1>😈 I got you</h1><p>I love you so much ❤️</p>";
  }

  function moveNo() {
    tries++;
    if (tries > 5) {
      const noBtn = document.getElementById("no");
      noBtn.innerText = "TAK";
      noBtn.onclick = yes;
      return;
    }
    const x = Math.random() * (window.innerWidth - 100);
    const y = Math.random() * (window.innerHeight - 50);
    const noBtn = document.getElementById("no");
    noBtn.style.left = x + "px";
    noBtn.style.top = y + "px";
  }
</script>

</body>
</html>
