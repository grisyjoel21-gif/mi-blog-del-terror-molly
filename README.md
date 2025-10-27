# mi-blog-del-terror-molly
<!doctype html>
<html lang="es">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <meta name="description" content="Blog del Terror — relatos y piezas extrañas inspiradas en el diario de Molly." />
  <title>BLOG DEL TERROR</title>
  <style>
    /* Reset / base */
    :root {
      --bg: #0d0d0d;
      --panel: #1a1a1a;
      --text: #e0e0e0;
      --muted: #999;
      --accent: #ffcc00;
      --danger: #ff4444;
      --nav-height: 64px;
    }
    * { box-sizing: border-box; }
    html { scroll-behavior: smooth; }
    body {
      margin: 0;
      background: var(--bg);
      color: var(--text);
      font-family: Georgia, 'Times New Roman', serif;
      line-height: 1.6;
      padding: calc(var(--nav-height) + 20px) 20px 60px; /* leave space for fixed nav */
    }

    /* Skip link */
    .skip-link {
      position: absolute;
      left: -999px;
      top: auto;
      width: 1px;
      height: 1px;
      overflow: hidden;
    }
    .skip-link:focus {
      left: 10px;
      top: 10px;
      width: auto;
      height: auto;
      padding: 8px 12px;
      background: #111;
      color: #fff;
      z-index: 9999;
      border-radius: 4px;
    }

    /* Fixed navigation */
    nav#main-nav {
      position: fixed;
      top: 0;
      left: 0;
      right: 0;
      height: var(--nav-height);
      background-color: rgba(17,17,17,0.98);
      color: #fff;
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 12px;
      padding: 0 12px;
      z-index: 1000;
      box-shadow: 0 2px 8px rgba(0,0,0,0.6);
    }
    nav#main-nav a {
      color: var(--accent);
      text-decoration: none;
      padding: 8px 10px;
      border-radius: 4px;
      font-weight: 600;
    }
    nav#main-nav a:focus,
    nav#main-nav a:hover {
      background: rgba(255,204,0,0.08);
      outline: none;
    }

    header, footer { text-align: center; max-width: 900px; margin: 0 auto 20px; }
    header p { margin: 6px 0; color: var(--muted); }
    h1 { color: var(--danger); font-size: 2.4rem; margin: 6px 0 14px; }
    h2 { color: var(--accent); margin-top: 0; }

    /* Story card */
    .historia {
      max-width: 900px;
      margin: 28px auto;
      background: var(--panel);
      padding: 20px;
      border-radius: 10px;
      box-shadow: 0 0 18px rgba(0,0,0,0.6);
    }

    img {
      display: block;
      margin: 20px auto;
      max-width: 100%;
      border: 2px solid #444;
      border-radius: 6px;
    }

    .advertencia {
      color: #ff9b9b;
      font-weight: bold;
    }

    /* Anchor spacing for fixed nav */
    section:target,
    .historia {
      scroll-margin-top: calc(var(--nav-height) + 12px);
    }

    /* Small actions */
    .actions { text-align: center; margin-top: 18px; }
    .btn {
      background: #222;
      color: #fff;
      border: 1px solid rgba(255,255,255,0.04);
      padding: 10px 16px;
      border-radius: 6px;
      text-decoration: none;
      display: inline-block;
      cursor: pointer;
      font-family: inherit;
    }
    .btn.secondary { background: transparent; color: var(--accent); border: 1px solid rgba(255,204,0,0.08); }

    footer { color: var(--muted); margin-top: 40px; }

    /* Responsive tweaks */
    @media (max-width: 520px) {
      h1 { font-size: 1.8rem; }
      nav#main-nav { gap: 8px; padding: 0 6px; }
      body { padding: calc(var(--nav-height) + 12px) 12px 40px; }
    }
  </style>
</head>
<body>
  <a class="skip-link" href="#main">Saltar al contenido</a>

  <nav id="main-nav" role="navigation" aria-label="Navegación principal">
    <a href="#el-alfil-del-vacio">El Alfil del Vacío</a>
    <a href="#solmira-la-flor-del-olvido">Solmira</a>
    <a href="#vane-la-que-saluda">Vane</a>
    <a href="#el-marionetista-de-raices">Marionetista</a>
    <a href="#kronox-el-guardian-del-miedo">Krönox</a>
  </nav>

  <header>
    <p>Nadie sabe quién fue Molly. Nadie la recuerda, nadie la conoció. Pero su diario apareció una noche de 1991, abandonado en una caja de madera, en el rincón más oscuro de una biblioteca olvidada.</p>
    <p>Las páginas estaban escritas con una tinta que parecía moverse, y cada historia hablaba de criaturas, objetos que no deberían existir.</p>
    <p>Fue entonces, en algún momento entre 1991 y 1993 —en un país que ya no figura en los mapas— que se fundó el Blog del Terror, inspirado por sus relatos.</p>
    <p>Lo que comenzó como una recopilación de dibujos malditos se convirtió en un museo virtual, donde cada sala revive una parte del diario.</p>
    <p>© 2025 Molly/Spike | Proyecto Blog del Terror</p>
    <h1>BLOG DEL TERROR</h1>

    <!-- Audio control: not autoplaying to respect browser policies and UX -->
    <div class="actions" aria-hidden="false">
      <button id="audio-toggle" class="btn" aria-pressed="false">▶︎ Reproducir música ambiental</button>
      <button id="mute-toggle" class="btn secondary" aria-pressed="false" style="margin-left:8px;">Activar/Desactivar silencio</button>
    </div>
  </header>

  <main id="main" tabindex="-1">
    <section class="historia" id="el-alfil-del-vacio" aria-labelledby="h-el-alfil">
      <div style="margin-bottom:15px;text-align:center;">
        <a href="#solmira-la-flor-del-olvido" style="margin:0 10px;color:var(--accent);text-decoration:underline;">Solmira</a>
        <a href="#vane-la-que-saluda" style="margin:0 10px;color:var(--accent);text-decoration:underline;">Vane</a>
        <a href="#el-marionetista-de-raices" style="margin:0 10px;color:var(--accent);text-decoration:underline;">Marionetista</a>
        <a href="#kronox-el-guardian-del-miedo" style="margin:0 10px;color:var(--accent);text-decoration:underline;">Krönox</a>
      </div>

      <h2 id="h-el-alfil">El Alfil del Vacío</h2>
      <p>En 1893, durante un torneo clandestino en el sótano del Teatro de La Cordura Perdida, un jugador desconocido apareció con un tablero tallado en obsidiana y piezas que parecían vivas. Su alfil no tenía forma humana ni animal. Era una figura retorcida con tentáculos, un ojo central, y una base que parecía absorber la luz. Cada vez que lo movía, el oponente sufría alucinaciones o sangraba por la nariz. Se dice que El Alfil del Vacío no se mueve en diagonales, sino entre dimensiones. Su presencia altera el tiempo, y quienes lo enfrentan sienten que la partida nunca termina. El jugador desapareció tras ganar todas las partidas sin pronunciar una sola palabra. El tablero fue encontrado años después en una caja sellada, junto con una nota:</p>
      <p class="advertencia">⚠️ Advertencia: “No juegues con lo que no entiendes. El alfil ya está en tu mente.”</p>
      <img alt="Ilustración: El Alfil del Vacío" src="alfil.jpg" loading="lazy" />
      <div style="text-align:center; margin-top:20px;">
        <a href="#top" class="btn">🔝 Volver al inicio</a>
      </div>
    </section>

    <section class="historia" id="solmira-la-flor-del-olvido" aria-labelledby="h-solmira">
      <div style="margin-bottom:15px;text-align:center;">
        <a href="#el-alfil-del-vacio" style="margin:0 10px;color:var(--accent);text-decoration:underline;">El Alfil</a>
        <a href="#vane-la-que-saluda" style="margin:0 10px;color:var(--accent);text-decoration:underline;">Vane</a>
        <a href="#el-marionetista-de-raices" style="margin:0 10px;color:var(--accent);text-decoration:underline;">Marionetista</a>
        <a href="#kronox-el-guardian-del-miedo" style="margin:0 10px;color:var(--accent);text-decoration:underline;">Krönox</a>
      </div>

      <h2 id="h-solmira">Solmira, la Flor del Olvido</h2>
      <p>En un jardín olvidado detrás del hospital psiquiátrico de la Cordura perdida, creció una flor que nadie sembró. Tenía pétalos como ojos, tallos como dedos, y un rostro que parecía recordar cosas que nadie quería recordar. Se dice que Solmira florece cada vez que alguien olvida un trauma profundo. Sus raíces se alimentan de memorias reprimidas, y sus ojos vigilan a quienes intentan escapar del pasado. Los pacientes que la miraban fijamente comenzaban a hablar en lenguas que no conocían. Algunos decían que veían a sus versiones infantiles atrapadas en el tallo. Nadie ha podido arrancarla. Cada intento termina con el jardinero desapareciendo, y una nueva flor creciendo en su lugar… con una sonrisa más amplia.</p>
      <img alt="Ilustración: Solmira, la Flor del Olvido" src="bailarin.jpg" loading="lazy" />
      <div style="text-align:center; margin-top:20px;">
        <a href="#top" class="btn">🔝 Volver al inicio</a>
      </div>
    </section>

    <section class="historia" id="vane-la-que-saluda" aria-labelledby="h-vane">
      <div style="margin-bottom:15px;text-align:center;">
        <a href="#el-alfil-del-vacio" style="margin:0 10px;color:var(--accent);text-decoration:underline;">El Alfil</a>
        <a href="#solmira-la-flor-del-olvido" style="margin:0 10px;color:var(--accent);text-decoration:underline;">Solmira</a>
        <a href="#el-marionetista-de-raices" style="margin:0 10px;color:var(--accent);text-decoration:underline;">Marionetista</a>
        <a href="#kronox-el-guardian-del-miedo" style="margin:0 10px;color:var(--accent);text-decoration:underline;">Krönox</a>
      </div>

      <h2 id="h-vane">Vane, la que saluda</h2>
      <p>Vane no nació. Vane apareció. Los registros del orfanato de La Cordura Perdida muestran una entrada sin fecha, sin firma, sin origen. Solo una nota escrita con carbón: “No la ignores si te saluda.” Vane siempre sonríe. Siempre levanta la mano. Pero nadie recuerda haberla visto moverse. Se dice que su cuerpo está hecho de ramas secas, y que su rostro fue tallado por los niños que desaparecieron en el bosque. Cuando alguien la ignora, comienza a aparecer en los reflejos. Primero en los espejos, luego en las ventanas, y finalmente… en los ojos de quienes la miran. Algunos lectores del blog aseguran haberla visto saludando desde dentro de las ilustraciones. Otros dicen que su sonrisa se amplía cada vez que alguien finge no tener miedo.</p>
      <p class="advertencia">⚠️ Advertencia: Si ves a Vane y no devuelves el saludo, ella te seguirá hasta que lo hagas. Y cuando lo hagas… ya será demasiado tarde.</p>
      <img alt="Ilustración: Vane, la que saluda" src="vanessa.jpg" loading="lazy" />
      <div style="text-align:center; margin-top:20px;">
        <a href="#top" class="btn">🔝 Volver al inicio</a>
      </div>
    </section>

    <section class="historia" id="el-marionetista-de-raices" aria-labelledby="h-marionetista">
      <div style="margin-bottom:15px;text-align:center;">
        <a href="#el-alfil-del-vacio" style="margin:0 10px;color:var(--accent);text-decoration:underline;">El Alfil</a>
        <a href="#solmira-la-flor-del-olvido" style="margin:0 10px;color:var(--accent);text-decoration:underline;">Solmira</a>
        <a href="#vane-la-que-saluda" style="margin:0 10px;color:var(--accent);text-decoration:underline;">Vane</a>
        <a href="#kronox-el-guardian-del-miedo" style="margin:0 10px;color:var(--accent);text-decoration:underline;">Krönox</a>
      </div>

      <h2 id="h-marionetista">El Marionetista de Raíces</h2>
      <p>Nadie lo ha visto directamente. Solo se han encontrado cuerpos con los ojos arrancados y una raíz conectada al cráneo. El Marionetista de Raíces no usa hilos. Usa pensamientos. Se dice que crece bajo tierra, alimentándose de secretos no confesados. Cuando alguien guarda un miedo demasiado profundo, una raíz comienza a formarse en su sombra. El ojo que sostiene no es suyo. Es el de su primer huésped, un niño que nunca habló. Desde entonces, cada vez que el Marionetista elige a alguien, ese ojo se abre y la raíz se extiende. Las víctimas no gritan. No luchan. Solo sonríen y obedecen. Algunos lectores del blog aseguran haber sentido un tirón en la nuca mientras dormían. Otros han despertado con tierra bajo las uñas.</p>
      <p class="advertencia">⚠️ Advertencia: Si sueñas con raíces, no las sigas. Ya no estás caminando… estás siendo guiado.</p>
      <img alt="Ilustración: El Marionetista de Raíces" src="marioneta.jpg" loading="lazy" />
      <div style="text-align:center; margin-top:20px;">
        <a href="#top" class="btn">🔝 Volver al inicio</a>
      </div>
    </section>

    <section class="historia" id="kronox-el-guardian-del-miedo" aria-labelledby="h-kronox">
      <div style="margin-bottom:15px;text-align:center;">
        <a href="#el-alfil-del-vacio" style="margin:0 10px;color:var(--accent);text-decoration:underline;">El Alfil</a>
        <a href="#solmira-la-flor-del-olvido" style="margin:0 10px;color:var(--accent);text-decoration:underline;">Solmira</a>
        <a href="#vane-la-que-saluda" style="margin:0 10px;color:var(--accent);text-decoration:underline;">Vane</a>
        <a href="#el-marionetista-de-raices" style="margin:0 10px;color:var(--accent);text-decoration:underline;">Marionetista</a>
      </div>

      <h2 id="h-kronox">Krönox: El Guardián del Miedo</h2>
      <p>Areli se burló de él. Dijo que no daba miedo. Que era solo un dibujo. Que los tiburones no existen en sueños. Pero Krönox no es un tiburón común. No fue creado. Fue despertado. Cada risa, cada desprecio, cada palabra que lo minimizó… lo alimentó. Ahora aparece. No en el mar, sino en los reflejos. En las pantallas apagadas. En los silencios entre pensamientos. Y siempre dice lo mismo: “Hola, Areli.” No grita. No corre. No ataca. Solo observa. Acecha. Porque Krönox no olvida. Y cada noche, se acerca más. Areli ya no duerme tranquila. Sabe que lo verá. Sabe que él la espera. Y sabe que algún día, cuando el sueño sea profundo y la mente esté indefensa… Krönox abrirá la boca. Y no será para saludar.</p>
      <img alt="Ilustración: Krönox, el Guardián del Miedo" src="tiburon.jpg" loading="lazy" />
      <div style="text-align:center; margin-top:20px;">
        <a href="#top" class="btn">🔝 Volver al inicio</a>
      </div>
    </section>
  </main>

  <footer>
    <p class="advertencia">⚠️ Advertencia: “No juegues con lo que no entiendes. El alfil ya está en tu mente.”</p>
  </footer>

  <!-- Audio element (hidden). Not autoplaying - plays when user clicks the "Reproducir" button -->
  <audio id="bg-audio" src="terror.mp3" loop preload="none"></audio>

  <script>
    // Audio controls: start/pause on user interaction
    (function () {
      const audio = document.getElementById('bg-audio');
      const btn = document.getElementById('audio-toggle');
      const muteBtn = document.getElementById('mute-toggle');

      btn.addEventListener('click', function () {
        // try to play or pause; browsers allow playback after user gesture
        if (audio.paused) {
          audio.play().then(() => {
            btn.textContent = '⏸️ Pausar música';
            btn.setAttribute('aria-pressed', 'true');
          }).catch((err) => {
            // if playback fails, inform the user
            console.warn('Reproducción fallida:', err);
            btn.textContent = '▶︎ Reproducir (intenta usar otro navegador)';
          });
        } else {
          audio.pause();
          btn.textContent = '▶︎ Reproducir música ambiental';
          btn.setAttribute('aria-pressed', 'false');
        }
      });

      muteBtn.addEventListener('click', function () {
        audio.muted = !audio.muted;
        muteBtn.setAttribute('aria-pressed', String(audio.muted));
        muteBtn.textContent = audio.muted ? 'Silenciado' : 'Activar/Desactivar silencio';
      });

      // Improve keyboard accessibility: allow Space/Enter activation
      [btn, muteBtn].forEach(b => b.addEventListener('keyup', (e) => {
        if (e.key === 'Enter' || e.key === ' ') b.click();
      }));
    })();
  </script>
</body>
</html>
