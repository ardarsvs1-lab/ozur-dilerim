<!DOCTYPE html>
<html lang="tr">
<head>
<meta charset="UTF-8">
<title>Özür Dilerim</title>
<style>
  body {
    height: 100vh;
    margin: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    background: linear-gradient(135deg, #f5c6c6, #f8e1e1);
    font-family: Arial, sans-serif;
  }

  .container {
    text-align: center;
    position: relative;
    width: 100%;
    height: 100%;
  }

  h1 {
    color: #7a1c1c;
  }

  button {
    padding: 15px 30px;
    font-size: 18px;
    border: none;
    border-radius: 12px;
    cursor: pointer;
    position: absolute;
  }

  #yes {
    background-color: #b33a3a;
    color: white;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
  }

  #no {
    background-color: #e0e0e0;
    left: 45%;
    top: 60%;
  }
</style>
</head>

<body>

<div class="container">
  <h1>Beni affediyor musun? 🥺</h1>
  <button id="yes" onclick="alert('💖 Yaşasın!')">Evet 💕</button>
  <button id="no">Hayır 🙄</button>
</div>

<script>
  const noBtn = document.getElementById("no");

  noBtn.addEventListener("click", () => {
    const maxX = window.innerWidth - noBtn.offsetWidth;
    const maxY = window.innerHeight - noBtn.offsetHeight;

    const randomX = Math.random() * maxX;
    const randomY = Math.random() * maxY;

    noBtn.style.left = randomX + "px";
    noBtn.style.top = randomY + "px";
  });
</script>

</body>
</html>
