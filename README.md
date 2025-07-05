<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Cartões Interativos</title>
  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: #f0f0f0;
      display: flex;
      justify-content: center;
      align-items: center;
      min-height: 100vh;
      flex-direction: column;
    }

    h1 {
      margin-bottom: 30px;
      color: #333;
    }

    .cards-container {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 20px;
      padding: 20px;
      max-width: 1000px;
      width: 100%;
    }

    .card {
      perspective: 1000px;
      cursor: pointer;
    }

    .card-inner {
      position: relative;
      width: 100%;
      height: 200px;
      transition: transform 0.8s;
      transform-style: preserve-3d;
    }

    .card.flipped .card-inner {
      transform: rotateY(180deg);
    }

    .card-face {
      position: absolute;
      width: 100%;
      height: 100%;
      border-radius: 15px;
      box-shadow: 0 4px 8px rgba(0,0,0,0.2);
      backface-visibility: hidden;
      display: flex;
      justify-content: center;
      align-items: center;
      padding: 20px;
      font-size: 18px;
      text-align: center;
    }

    .card-front {
      background: #ffffff;
    }

    .card-back {
      background: #4caf50;
      color: white;
      transform: rotateY(180deg);
    }
  </style>
</head>
<body>
  <h1>Cartões de Perguntas</h1>

  <div class="cards-container">
    <div class="card" onclick="this.classList.toggle('flipped')">
      <div class="card-inner">
        <div class="card-face card-front">
          O que é HTML?
        </div>
        <div class="card-face card-back">
          HTML é a linguagem de marcação usada para estruturar páginas web.
        </div>
      </div>
    </div>

    <div class="card" onclick="this.classList.toggle('flipped')">
      <div class="card-inner">
        <div class="card-face card-front">
          Para que serve o CSS?
        </div>
        <div class="card-face card-back">
          CSS é usado para estilizar e deixar bonito o conteúdo HTML.
        </div>
      </div>
    </div>

    <div class="card" onclick="this.classList.toggle('flipped')">
      <div class="card-inner">
        <div class="card-face card-front">
          O que é JavaScript?
        </div>
        <div class="card-face card-back">
          JavaScript é a linguagem de programação que torna a página interativa.
        </div>
      </div>
    </div>

    <!-- Você pode adicionar mais cartões copiando e colando esse bloco -->
  </div>
</body>
</html>
