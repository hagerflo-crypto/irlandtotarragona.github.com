# irlandtotarragona.github.com
<!DOCTYPE html>
<html lang="de">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Countdown</title>
  <meta name="description" content="Countdown bis zum Start" />
  <link rel="preconnect" href="https://cdn.jsdelivr.net" crossorigin>
  <!-- Luxon: robuste Zeitzonenhandhabung -->
  <script defer src="https://cdn.jsdelivr.net/npm/luxon@3/build/global/luxon.min.js"></script>
  <link rel="stylesheet" href="style.css" />
  <script defer src="app.js"></script>
</head>
<body>
  <main class="wrap">
    <h1>Countdown bis zum Start</h1>

    <!-- Optional: Zeitzone & Zielzeit user-visible -->
    <p class="meta">
      Start: <span id="start-local"></span> (<span id="tz-name"></span>)
    </p>

    <div id="countdown" class="countdown" aria-live="polite" aria-atomic="true">
      <div><span id="d">–</span><small>Tage</small></div>
      <div><span id="h">–</span><small>Std</small></div>
      <div><span id="m">–</span><small>Min</small></div>
      <div><span id="s">–</span><small>Sek</small></div>
    </div>

    <div id="progress" class="progress" aria-hidden="true">
      <div id="bar" class="bar"></div>
    </div>

    <noscript>Bitte JavaScript aktivieren – sonst kein Countdown.</noscript>
  </main>
</body>
</html>
:root { --fg:#111; --muted:#666; --bg:#fafafa; --card:#fff; --border:#eaeaea; }
* { box-sizing:border-box; }
html,body { height:100%; }
body { margin:0; font-family:system-ui,-apple-system,Segoe UI,Roboto,Ubuntu,'Helvetica Neue',Arial,sans-serif; background:var(--bg); color:var(--fg); }
.wrap { max-width:720px; margin:6rem auto; padding:2rem; background:var(--card); border:1px solid var(--border); border-radius:14px; box-shadow:0 10px 25px rgba(0,0,0,.04); }
h1 { margin-top:0; letter-spacing:.2px; }
.meta { color:var(--muted); margin-top:-.5rem; }
.countdown { display:flex; gap:1rem; justify-content:space-between; margin:2rem 0 1.25rem; }
.countdown > div { flex:1; text-align:center; padding:1rem; border:1px solid var(--border); border-radius:12px; }
.countdown span { display:block; font-size:clamp(2.2rem,6vw,4rem); font-weight:700; line-height:1; }
.countdown small { display:block; margin-top:.4rem; color:var(--muted); letter-spacing:.6px; text-transform:uppercase; font-size:.8rem; }
.progress { height:10px; background:#f1f1f1; border-radius:999px; overflow:hidden; border:1px solid var(--border); }
.bar { height:100%; width:0%; background:linear-gradient(90deg,#4e8cff,#5dd2b4,#ffd166); transition:width .8s cubic-bezier(.2,.7,.2,1); }
@media (max-width:520px){ .wrap{ margin:2rem 1rem; padding:1.25rem; } }
