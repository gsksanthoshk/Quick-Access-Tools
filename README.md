# QAT
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Dashboard — Attendance Tools</title>
  <style>
    :root {
      --bg: #f5f7fa;
      --accent: #007bff;
      --muted: #6b7280;
      --nav-bg: rgba(3,105,255,0.05);
    }

    * { box-sizing: border-box; }
    body {
      font-family: system-ui, sans-serif;
      background: var(--bg);
      margin: 0;
      display: flex;
      align-items: center;
      justify-content: center;
      height: 100vh;
      padding: 20px;
    }

    .card {
      background: #fff;
      border-radius: 16px;
      box-shadow: 0 6px 24px rgba(0,0,0,0.06);
      padding: 30px;
      width: 360px;
      text-align: center;
      animation: fadeIn 0.4s ease;
    }

    .card h1 {
      margin: 0 0 20px 0;
      font-size: 22px;
      color: #0f172a;
    }

    .nav {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(120px, 1fr));
      gap: 16px;
      justify-items: center;
      margin-top: 8px;
    }

    .nav-link {
      width: 110px;
      height: 110px;
      border-radius: 14px;
      text-decoration: none;
      color: var(--muted);
      background: transparent;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      transition: all 0.2s ease;
      position: relative;
      user-select: none;
      border: 1px solid transparent;
    }

    .nav-link .icon {
      font-size: 30px;
      margin-bottom: 8px;
      background: var(--nav-bg);
      border-radius: 10px;
      padding: 10px;
      color: var(--accent);
      transition: transform .2s ease, background .2s ease;
    }

    .nav-link .label {
      font-weight: 600;
      font-size: 14px;
      color: #111827;
    }

    .nav-link:hover {
      transform: translateY(-6px);
      box-shadow: 0 10px 22px rgba(3,105,255,0.08);
      background: rgba(0,123,255,0.03);
    }

    .nav-link:hover .icon {
      transform: scale(1.1);
      background: rgba(3,105,255,0.12);
    }

    .nav-link .tip {
      position: absolute;
      bottom: calc(100% + 8px);
      left: 50%;
      transform: translateX(-50%) translateY(6px);
      background: rgba(15,23,42,0.9);
      color: #fff;
      font-size: 12px;
      padding: 5px 8px;
      border-radius: 6px;
      opacity: 0;
      pointer-events: none;
      transition: all .15s ease;
      white-space: nowrap;
    }

    .nav-link:hover .tip {
      opacity: 1;
      transform: translateX(-50%) translateY(0);
    }

    @media (max-width: 480px) {
      .nav-link {
        width: 100px;
        height: 100px;
      }
      .nav-link .icon { font-size: 26px; }
      .nav-link .label { font-size: 13px; }
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(10px); }
      to { opacity: 1; transform: translateY(0); }
    }
  </style>
</head>
<body>
  <div class="card">
    <h1>📚 Quick Access Tools</h1>
    <nav class="nav" aria-label="Main navigation">
      <a class="nav-link" href="attendance.html">
        <span class="icon" aria-hidden>📊</span>
        <span class="label">Attendance</span>
        <span class="tip">Open Attendance</span>
      </a>

      <a class="nav-link" href="calendar.html">
        <span class="icon" aria-hidden>🗓</span>
        <span class="label">Calendar</span>
        <span class="tip">Open Calendar</span>
      </a>

      <a class="nav-link" href="weather.html">
        <span class="icon" aria-hidden>🌦</span>
        <span class="label">Weather</span>
        <span class="tip">View Weather</span>
      </a>

      <a class="nav-link" href="quantnum.html">
        <span class="icon" aria-hidden>🧮</span>
        <span class="label">QuantumCalc</span>
        <span class="tip">Open Calculator</span>
      </a>
    </nav>
  </div>
</body>
</html>

