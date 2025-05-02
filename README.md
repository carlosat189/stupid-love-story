<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Carta en tonos morados con corazón grande</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=Indie+Flower&display=swap');

  body {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    background: linear-gradient(135deg, #e9dbf7 0%, #f0e6fa 100%);
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    margin: 0;
    padding: 20px;
    overflow: hidden;
    position: relative;
  }

  /* Sparkle/glow effect around letter */
  .letter {
    background: #f7f0ff;
    border-radius: 12px;
    padding: 35px 40px 30px 40px;
    box-shadow:
      0 0 10px 2px #a88fff88,
      0 4px 18px rgba(121, 63, 182, 0.3);
    max-width: 400px;
    font-size: 1.2rem;
    color: #4b2e83;
    line-height: 1.75;
    opacity: 0;
    transform: translateY(30px);
    animation: fadeSlideIn 1.8s forwards;
    position: relative;
    font-family: 'Indie Flower', cursive;
  }

  /* Sparkle particles */
  .sparkle {
    position: absolute;
    width: 6px;
    height: 6px;
    background: #b08aff;
    border-radius: 50%;
    filter: drop-shadow(0 0 5px #b08aff);
    animation: sparkleAnim 2.5s infinite;
    opacity: 0.85;
  }

  /* Different delays and positions for sparkles */
  .sparkle1 {
    top: 10px; left: 10px;
    animation-delay: 0s;
  }
  .sparkle2 {
    top: 45px; right: 30px;
    animation-delay: 0.8s;
  }
  .sparkle3 {
    bottom: 40px; left: 25px;
    animation-delay: 1.5s;
  }
  .sparkle4 {
    bottom: 20px; right: 20px;
    animation-delay: 2.1s;
  }

  @keyframes sparkleAnim {
    0%, 100% { opacity: 0.85; transform: scale(1) rotate(0deg); }
    50% { opacity: 0; transform: scale(1.5) rotate(90deg);}
  }

  /* Text paragraphs styling */
  .letter p {
    margin: 0.5em 0;
    opacity: 0;
    transform: translateY(15px);
    animation: paragraphFadeUp 0.8s forwards;
  }
  .letter p:nth-child(1) { animation-delay: 1.9s; }
  .letter p:nth-child(2) { animation-delay: 2.1s; }
  .letter p:nth-child(3) { animation-delay: 2.3s; }
  .letter p:nth-child(4) { animation-delay: 2.5s; }
  .letter p:nth-child(5) { animation-delay: 2.7s; }
  .letter p:nth-child(6) { animation-delay: 2.9s; }
  .letter p:nth-child(7) { animation-delay: 3.1s; }
  .letter p:nth-child(8) { animation-delay: 3.3s; }

  @keyframes paragraphFadeUp {
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }

  /* Heart container */
  .heart-container {
    margin-top: 24px;
    font-size: 5rem; /* bigger heart */
    text-align: center;
    color: #7b3fdb;
    user-select: none;
    filter: drop-shadow(0 0 6px #9256ff);
    cursor: pointer;
    animation: heartbeat 1.4s infinite;
  }
  .heart-container.paused {
    animation-play-state: paused;
    color: #a28add;
    filter: drop-shadow(0 0 3px #b3a6ff);
  }

  /* Heartbeat animation */
  @keyframes heartbeat {
    0%, 100% {
      transform: scale(1);
      color: #7b3fdb;
      text-shadow:
        0 0 8px #7b3fdb,
        0 0 16px #7b3fdb,
        0 0 24px #7b3fdb;
    }
    25% {
      transform: scale(1.3);
      color: #b08aff;
      text-shadow:
        0 0 16px #b08aff,
        0 0 24px #b08aff,
        0 0 32px #b08aff;
    }
    50% {
      transform: scale(1);
      color: #7b3fdb;
      text-shadow:
        0 0 8px #7b3fdb,
        0 0 16px #7b3fdb,
        0 0 24px #7b3fdb;
    }
  }

  /* Fade+slide in for letter */
  @keyframes fadeSlideIn {
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }

  /* Footer with date */
  .footer {
    margin-top: 30px;
    font-size: 0.85rem;
    text-align: center;
    color: #6a4f9c;
    font-style: italic;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  }

  /* Button styling */
  .btn-toggle-heart {
    margin: 18px auto 0;
    display: block;
    background: #7b3fdb;
    color: white;
    border: none;
    border-radius: 20px;
    padding: 10px 24px;
    font-size: 1rem;
    cursor: pointer;
    box-shadow: 0 2px 8px #9759ff;
    transition: background-color 0.3s, box-shadow 0.3s;
  }
  .btn-toggle-heart:hover {
    background: #9256ff;
    box-shadow: 0 2px 14px #b18aff;
  }

</style>
</head>
<body>
  <article class="letter" role="article" aria-label="Carta de amor para Fernanda Denise">
    <span class="sparkle sparkle1"></span>
    <span class="sparkle sparkle2"></span>
    <span class="sparkle sparkle3"></span>
    <span class="sparkle sparkle4"></span>

    <p><strong>Querida Fernanda Denise,</strong></p>
    <p>Recuerda que te amo muchísimo,</p>
    <p>y que tienes unos ojos hermosos.</p>
    <p>Recuerda que eres muy importante para mí,</p>
    <p>Sólo sé que te amo con todo mi corazón,</p>
    <p>y serás una excelente maquillista,</p>
    <p>¡Te amo!</p>
    <p>Con todo mi amor,<br />Tu todo tonto</p>

    <div class="heart-container" role="img" aria-label="corazón bombeando" tabindex="0">🫀</div>

    <button class="btn-toggle-heart" aria-pressed="true" aria-label="Pausar o reanudar animación del corazón">
      Pausar latido del corazón
    </button>

    <footer class="footer" aria-live="polite" aria-atomic="true"></footer>
  </article>

  <script>
    const heart = document.querySelector('.heart-container');
    const btn = document.querySelector('.btn-toggle-heart');
    const footer = document.querySelector('.footer');

    btn.addEventListener('click', () => {
      const isPaused = heart.classList.toggle('paused');

      if (isPaused) {
        btn.textContent = 'Reanudar latido del corazón';
        btn.setAttribute('aria-pressed', 'false');
        footer.textContent = 'Animación del corazón pausada';
      } else {
        btn.textContent = 'Pausar latido del corazón';
        btn.setAttribute('aria-pressed', 'true');
        footer.textContent = 'Animación del corazón reanudada';
      }
    });

    // Initialize footer date
    const today = new Date();
    footer.textContent = `Carta enviada el ${today.toLocaleDateString('es-ES', { year: 'numeric', month: 'long', day: 'numeric' })}`;
  </script>
</body>
</html>

```

