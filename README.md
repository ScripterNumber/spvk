<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8">
  <title>Симулятор падения в Канаву</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    :root {
      --main-bg: #111;
      --accent: #00A2FF;
      --accent-light: #3DB8FF;
      --text: #F0F0F0;
    }
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }
    body {
      font-family: "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
      background: var(--main-bg);
      color: var(--text);
      line-height: 1.6;
      overflow-x: hidden;
    }
    header {
      height: 100vh;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      text-align: center;
      background: radial-gradient(circle at 50% 50%, #1a1a1a 0%, #000 100%);
      position: relative;
    }
    header::before { /* лёгкая пыль/звёзды */
      content: '';
      position: absolute;
      inset: 0;
      background: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 800"><circle cx="100" cy="100" r="1" fill="white" opacity=".6"/><circle cx="300" cy="150" r="1.3" fill="white" opacity=".4"/><circle cx="500" cy="300" r="1" fill="white" opacity=".5"/><circle cx="700" cy="450" r="1.5" fill="white" opacity=".3"/><circle cx="900" cy="200" r="1" fill="white" opacity=".4"/></svg>');
      animation: twinkle 10s infinite linear;
    }
    @keyframes twinkle {
      0% {transform: translateY(0);}
      100% {transform: translateY(-20px);}
    }
    h1 {
      font-size: clamp(2.5rem, 5vw, 4rem);
      margin-bottom: .5em;
      background: linear-gradient(90deg, var(--accent-light), var(--accent));
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      animation: glow 2s ease-in-out infinite alternate;
    }
    @keyframes glow {
      from {text-shadow: 0 0 10px var(--accent);}
      to {text-shadow: 0 0 20px var(--accent-light);}
    }
    .subtitle {
      font-size: 1.2rem;
      margin-bottom: 2rem;
      opacity: .8;
    }
    .btn {
      position: relative;
      display: inline-block;
      padding: .9em 2.2em;
      font-size: 1.1rem;
      font-weight: bold;
      color: #fff;
      background: var(--accent);
      border: none;
      border-radius: 50px;
      cursor: pointer;
      transition: transform .2s, box-shadow .3s;
      overflow: hidden;
      text-decoration: none;
    }
    .btn:hover {
      transform: translateY(-3px);
      box-shadow: 0 0 20px var(--accent-light);
    }
    .btn::after {
      content: '';
      position: absolute;
      top: 50%;
      left: 50%;
      width: 300%;
      height: 300%;
      background: rgba(255,255,255,.2);
      border-radius: 50%;
      transform: translate(-50%, -50%) scale(0);
      transition: transform .5s;
    }
    .btn:hover::after {
      transform: translate(-50%, -50%) scale(1);
    }
    section.features {
      padding: 4rem 1.5rem;
      max-width: 900px;
      margin: auto;
      display: grid;
      gap: 2rem;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    }
    .feature-card {
      background: #1a1a1a;
      border: 1px solid #2a2a2a;
      border-radius: 12px;
      padding: 2rem;
      text-align: center;
      transition: transform .3s, border-color .3s;
    }
    .feature-card:hover {
      transform: translateY(-5px);
      border-color: var(--accent);
    }
    footer {
      padding: 2rem 1rem;
      text-align: center;
      font-size: .9rem;
      opacity: .5;
    }
  </style>
</head>
<body>

  <header>
    <h1>Симулятор хуйни</h1>
    <p class="subtitle">Погрузись в ебанный анрег при пвп и хуёвое коммьюнити!</p>
    <a class="btn" href="https://www.roblox.com/games/7002808196" target="_blank">Играть</a>
  </header>

  <section class="features">
    <div class="feature-card">
      <h3>🔥 Уникальный геймплей</h3>
      <p>Только у нас — эксклюзивные механики, которых нет больше нигде. Ибо регистрации хитов хуёве чем у нас нет - нигде.</p>
    </div>
    <div class="feature-card">
      <h3>👥 Играй с друзьями</h3>
      <p>Сделайте клан хуесосов и гасите всех толпой!</p>
    </div>
    <div class="feature-card">
      <h3>🎁 Регулярные коды и обновления</h3>
      <p>Мы обновляем игру раз в три года. А коды вообще нахуй не делаем!</p>
    </div>
  </section>

  <footer>
    © 2025 DrotaTri_poRusski. Все права защищены.
  </footer>

</body>
</html>
