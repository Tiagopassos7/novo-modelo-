<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Tiago & Ricaely</title>
  <link href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@700&family=Open+Sans&display=swap" rel="stylesheet">
  <style>
    * { margin: 0; padding: 0; box-sizing: border-box; }
    body {
      font-family: 'Open Sans', sans-serif;
      background: url('IMG_20250517_185947_510.webp') no-repeat center center fixed;
      background-size: cover;
      height: 100vh;
      overflow: hidden;
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
      backdrop-filter: blur(6px);
      color: #fff;
      text-align: center;
    }
    h1 {
      font-family: 'Dancing Script', cursive;
      font-size: 3em;
      margin-bottom: 10px;
      text-shadow: 2px 2px 6px rgba(0,0,0,0.6);
    }
    p {
      font-size: 1.2em;
      max-width: 700px;
      margin: 10px 20px;
      text-shadow: 1px 1px 4px rgba(0,0,0,0.5);
    }
    .contador {
      font-size: 1.5em;
      margin-top: 20px;
    }
    #audio-control {
      margin-top: 20px;
      background: rgba(255,255,255,0.2);
      border: none;
      color: #fff;
      font-size: 1em;
      padding: 10px 20px;
      border-radius: 30px;
      cursor: pointer;
    }
    .coracoes {
      position: absolute;
      width: 100%;
      height: 100%;
      pointer-events: none;
      overflow: hidden;
    }
    .coracao {
      position: absolute;
      color: rgba(255, 192, 203, 0.7);
      font-size: 2em;
      animation: flutuar 10s infinite;
    }
    @keyframes flutuar {
      0% { transform: translateY(100vh) scale(1); opacity: 1; }
      100% { transform: translateY(-10vh) scale(0.5); opacity: 0; }
    }
  </style>
</head>
<body>
  <h1>Tiago & Ricaely</h1>
  <p>
    O tempo pode passar, os dias podem correr, mas nosso amor só cresce.  
    Somos dois corações que decidiram caminhar juntos, com respeito, cuidado e carinho.  
    A cada segundo, te amo mais.
  </p>
  <div class="contador" id="contador"></div>
  <button id="audio-control">Tocar música</button>
  <audio id="musica" src="musica.mp3" loop></audio>
  <div class="coracoes" id="coracoes"></div>
  <script>
    const dataInicio = new Date("2025-01-18T00:00:00");
    const contadorEl = document.getElementById('contador');
    function atualizarContador() {
      const agora = new Date();
      const diff = agora - dataInicio;
      const segundos = Math.floor(diff / 1000);
      const minutos = Math.floor(segundos / 60);
      const horas = Math.floor(minutos / 60);
      const dias = Math.floor(horas / 24);
      const semanas = Math.floor(dias / 7);
      const meses = Math.floor(dias / 30.437);
      contadorEl.innerHTML = `
        <strong>${meses}</strong> meses •
        <strong>${semanas}</strong> semanas •
        <strong>${dias}</strong> dias •
        <strong>${horas % 24}</strong>h •
        <strong>${minutos % 60}</strong>min •
        <strong>${segundos % 60}</strong>s
      `;
    }
    setInterval(atualizarContador, 1000);
    atualizarContador();

    const btn = document.getElementById('audio-control');
    const audio = document.getElementById('musica');
    let tocando = false;
    btn.onclick = () => {
      if (!tocando) {
        audio.play();
        btn.innerText = 'Pausar música';
      } else {
        audio.pause();
        btn.innerText = 'Tocar música';
      }
      tocando = !tocando;
    };

    function criarCoracao() {
      const coracoes = document.getElementById('coracoes');
      const coracao = document.createElement('div');
      coracao.className = 'coracao';
      coracao.innerHTML = '❤️';
      coracao.style.left = Math.random() * 100 + '%';
      coracao.style.animationDuration = 5 + Math.random() * 5 + 's';
      coracoes.appendChild(coracao);
      setTimeout(() => coracao.remove(), 10000);
    }
    setInterval(criarCoracao, 600);
  </script>
</body>
</html>
