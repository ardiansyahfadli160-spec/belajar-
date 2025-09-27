<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Animasi Naga Sederhana</title>
<style>
  body {
    background: #111;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    margin: 0;
  }

  .dragon {
    position: relative;
    width: 200px;
    height: 100px;
    background: linear-gradient(90deg, #2e8b57, #3cb371);
    border-radius: 80px 80px 60px 60px;
    animation: moveDragon 6s linear infinite;
  }

  /* Kepala */
  .head {
    position: absolute;
    left: -60px;
    top: 20px;
    width: 80px;
    height: 60px;
    background: linear-gradient(135deg, #3cb371, #2e8b57);
    border-radius: 50% 50% 40% 40%;
    border: 3px solid #006400;
    animation: headMove 1.2s ease-in-out infinite alternate;
  }

  /* Sayap */
  .wing {
    position: absolute;
    top: 0;
    right: 30px;
    width: 80px;
    height: 80px;
    background: #228b22;
    border-radius: 50% 50% 0 0;
    transform-origin: bottom center;
    animation: flap 1s ease-in-out infinite alternate;
    border: 2px solid #006400;
  }

  /* Sayap bawah */
  .wing::after {
    content: '';
    position: absolute;
    bottom: 0;
    left: 10px;
    width: 60px;
    height: 30px;
    background: #2e8b57;
    border-radius: 40% 40% 0 0;
  }

  /* Ekor */
  .tail {
    position: absolute;
    right: -40px;
    top: 50px;
    width: 70px;
    height: 30px;
    background: linear-gradient(90deg, #3cb371, #2e8b57);
    border-radius: 50% 50% 50% 50% / 30% 30% 70% 70%;
    animation: tailWave 2s ease-in-out infinite alternate;
  }

  @keyframes flap {
    0% { transform: rotate(15deg); }
    100% { transform: rotate(-15deg); }
  }

  @keyframes tailWave {
    0% { transform: rotate(10deg); }
    100% { transform: rotate(-10deg); }
  }

  @keyframes moveDragon {
    0% { transform: translateX(-250px); }
    100% { transform: translateX(100vw); }
  }

  @keyframes headMove {
    0% { transform: translateY(0); }
    100% { transform: translateY(8px); }
  }
</style>
</head>
<body>

<div class="dragon">
  <div class="head"></div>
  <div class="wing"></div>
  <div class="tail"></div>
</div>

</body>
</html>

