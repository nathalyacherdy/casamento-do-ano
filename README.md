<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Convite de Casamento</title>
  <style>
    body {
      font-family: 'Segoe UI', sans-serif;
      background-color: #fff8f0;
      color: #5a3e36;
      margin: 0;
      padding: 0;
    }
    header {
      background-image: url('https://images.unsplash.com/photo-1525393835820-e4f7f0d0edcf');
      background-size: cover;
      background-position: center;
      text-align: center;
      padding: 4em 1em;
      color: white;
    }
    header h1 {
      margin: 0;
      font-size: 3em;
    }
    header p {
      font-size: 1.5em;
      margin-top: 0.5em;
    }
    .section {
      padding: 2em;
      text-align: center;
    }
    .localizacao, .confirmar, .galeria, .playlist, .contagem {
      background-color: #fff;
      margin: 2em auto;
      max-width: 700px;
      padding: 2em;
      border-radius: 15px;
      box-shadow: 0 0 15px rgba(0,0,0,0.1);
    }
    input, button {
      padding: 0.8em;
      margin-top: 1em;
      width: 100%;
      border: 1px solid #ccc;
      border-radius: 5px;
      font-size: 1em;
    }
    button {
      background-color: #d29591;
      color: white;
      border: none;
      cursor: pointer;
    }
    button:hover {
      background-color: #b97b77;
    }
    .galeria img {
      width: 100%;
      border-radius: 10px;
      margin-bottom: 1em;
    }
    .playlist iframe {
      width: 100%;
      border: none;
      height: 80px;
    }
    .contagem span {
      font-size: 1.5em;
      display: inline-block;
      margin: 0.5em;
    }
  </style>
</head>
<body>
  <header>
    <h1>Camila & Rafael</h1>
    <p>Com alegria convidamos você para o nosso casamento!</p>
  </header>

  <section class="section contagem">
    <h2>Faltam:</h2>
    <div id="contador"></div>
  </section>

  <section class="section localizacao">
    <h2>Local da Cerimônia</h2>
    <p>Sítio Encanto das Flores</p>
    <p>Rua das Palmeiras, 123 - São Paulo, SP</p>
    <p>Data: 15 de Novembro de 2025</p>
    <p>Horário: 16h</p>
  </section>

  <section class="section galeria">
    <h2>Momentos Especiais</h2>
    <img src="https://images.unsplash.com/photo-1520975916090-3105956dac38" alt="Casal">
    <img src="https://images.unsplash.com/photo-1523601343247-4aa0e3d26a31" alt="Ensaio">
  </section>

  <section class="section playlist">
    <h2>Nossa Trilha Sonora</h2>
    <iframe src="https://open.spotify.com/embed/playlist/37i9dQZF1DX0BcQWzuB7ZO?utm_source=generator"></iframe>
  </section>

  <section class="section confirmar">
    <h2>Confirme sua Presença</h2>
    <form>
      <input type="text" placeholder="Seu nome" required />
      <input type="email" placeholder="Seu e-mail" required />
      <button type="submit">Confirmar</button>
    </form>
  </section>

  <script>
    const contador = document.getElementById('contador');
    const dataCasamento = new Date('2025-11-15T16:00:00');

    function atualizarContador() {
      const agora = new Date();
      const diferenca = dataCasamento - agora;

      const dias = Math.floor(diferenca / (1000 * 60 * 60 * 24));
      const horas = Math.floor((diferenca / (1000 * 60 * 60)) % 24);
      const minutos = Math.floor((diferenca / (1000 * 60)) % 60);
      const segundos = Math.floor((diferenca / 1000) % 60);

      contador.innerHTML = `
        <span>${dias} dias</span>
        <span>${horas}h</span>
        <span>${minutos}min</span>
        <span>${segundos}s</span>
      `;
    }

    setInterval(atualizarContador, 1000);
    atualizarContador();
  </script>
</body>
</html>
