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
