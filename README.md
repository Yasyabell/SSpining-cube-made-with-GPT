<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>3D Spinning Cube</title>
<style>
  body {
    margin: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    background-color: #f0f0f0;
  }
  .cube-container {
    width: 200px;
    height: 200px;
    perspective: 800px;
  }
  .cube {
    width: 100%;
    height: 100%;
    transform-style: preserve-3d;
    animation: rotate 5s linear infinite;
  }
  .face {
    position: absolute;
    width: 200px;
    height: 200px;
    background-color: rgba(0, 0, 0, 0.2);
    border: 1px solid black;
  }
  .front { transform: translateZ(100px); }
  .back { transform: translateZ(-100px) rotateY(180deg); }
  .top { transform: rotateX(90deg) translateZ(100px); }
  .bottom { transform: rotateX(-90deg) translateZ(100px); }
  .left { transform: rotateY(-90deg) translateZ(100px); }
  .right { transform: rotateY(90deg) translateZ(100px); }

  @keyframes rotate {
    0% { transform: rotateY(0); }
    100% { transform: rotateY(360deg); }
  }
</style>
</head>
<body>
<div class="cube-container">
  <div class="cube">
    <div class="face front"></div>
    <div class="face back"></div>
    <div class="face top"></div>
    <div class="face bottom"></div>
    <div class="face left"></div>
    <div class="face right"></div>
  </div>
</div>
</body>
</html>
