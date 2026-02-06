<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>💌 Valentine?</title>
  <style>
    body{
      font-family: system-ui, -apple-system, Segoe UI, Roboto, Arial, sans-serif;
      display:flex; align-items:center; justify-content:center;
      min-height:100vh; margin:0; background:#fff5f8;
      color:#1a1a1a;
    }
    .card{
      width:min(520px, 92vw);
      background:white;
      border-radius:18px;
      padding:28px;
      box-shadow:0 12px 30px rgba(0,0,0,.12);
      text-align:center;
    }
    h1{ margin:0 0 10px; font-size:28px; }
    p{ margin:0 0 18px; font-size:16px; opacity:.9; }
    .btns{ display:flex; gap:12px; justify-content:center; flex-wrap:wrap; }
    button{
      border:0; padding:12px 18px; border-radius:999px;
      font-size:16px; cursor:pointer;
    }
    .yes{ background:#ff3b7a; color:white; }
    .no{ background:#f1f1f1; }
    .msg{
      margin-top:18px; padding:14px; border-radius:14px;
      background:#fff0f5; display:none;
    }
    .small{ font-size:13px; opacity:.8; margin-top:10px; }
    a{ color:#ff3b7a; text-decoration:none; font-weight:600; }
  </style>
</head>
<body>
  <div class="card">
    <h1>💘 Do you want to be my Valentine?</h1>
    <p>Just tap a button 😊</p>

    <div class="btns">
      <button class="yes" id="yesBtn">Yes 💖</button>
      <button class="no" id="noBtn">No 😅</button>
    </div>

    <div class="msg" id="msgBox"></div>
    <div class="small">Made with love.</div>
  </div>

  <script>
    const msgBox = document.getElementById("msgBox");

    function showMessage(html){
      msgBox.style.display = "block";
      msgBox.innerHTML = html;
    }

    document.getElementById("yesBtn").addEventListener("click", () => {
      showMessage(`
        <h2 style="margin:0 0 8px;">Yessss!! 😍💐</h2>
        <p style="margin:0 0 10px;">You just made my day. I can’t wait to celebrate you ❤️</p>
        <a href="mailto:?subject=My%20Answer%20💘&body=YES%20💖%20I%27ll%20be%20your%20Valentine!">Reply “YES”</a>
      `);
    });

    document.getElementById("noBtn").addEventListener("click", () => {
      showMessage(`
        <h2 style="margin:0 0 8px;">Aww okay 😊</h2>
        <p style="margin:0 0 10px;">No pressure at all. You’re still amazing 💛</p>
        <a href="mailto:?subject=My%20Answer%20💘&body=No%20thanks%20%E2%98%BA%EF%B8%8F">Send “No”</a>
      `);
    });
  </script>
</body>
</html>
