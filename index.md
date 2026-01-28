<!doctype html>
<html lang="zh-CN">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Portfolio | Nine</title>
  <style>
    :root{
      --card:#d87545;
      --lang:#e8a7a7;
      --ink:#111;
      --border:#222;
      --radius:18px;
    }
    *{box-sizing:border-box;}
    body{
      margin:0;
      font-family: system-ui, -apple-system, "Noto Sans SC", "Noto Sans JP", sans-serif;
      background:#fff;
      color:var(--ink);
    }
    .wrap{max-width:1280px; margin:0 auto; padding:28px 28px 40px;}

    .top{
      display:grid;
      grid-template-columns: 220px 1fr 260px;
      align-items:start;
      gap:18px;
      margin-bottom:34px;
    }
    .avatar{
      width:180px; height:180px;
      border-radius:16px;
      object-fit:contain;
    }
    .titleBadge{margin-top:10px; display:flex; justify-content:center;}
    .badge{
      min-width:520px;
      text-align:center;
      padding:26px 24px;
      border:2px solid var(--border);
      border-radius:18px;
      background:#fff;
      font-weight:800;
      letter-spacing:.08em;
      font-size:34px;
      box-shadow:10px 10px 0 #000;
    }
    .langBtn{
      justify-self:end;
      margin-top:6px;
      width:240px;
      padding:22px 18px;
      border-radius:14px;
      border:0;
      background:var(--lang);
      font-size:18px;
      font-weight:700;
      cursor:pointer;
    }

    .grid{
      display:grid;
      grid-template-columns: repeat(4, 1fr);
      gap:40px;
      margin-top:10px;
    }
    .card{
      border-radius:var(--radius);
      background:var(--card);
      height:420px;
      overflow:hidden;
      cursor:pointer;
      text-decoration:none;
      color:#111;
      display:flex;
      align-items:center;
      justify-content:center;
      font-weight:700;
      font-size:20px;
      transition: transform .15s ease, box-shadow .15s ease, filter .15s ease;
    }
    .card:hover{transform:translateY(-4px); filter:brightness(1.03); box-shadow:0 12px 28px rgba(0,0,0,.12);}
    .label{padding:0 14px; text-align:center;}

    /* VTuber：卡片里直接放视频 */
    .card.video{padding:16px; align-items:stretch; justify-content:stretch;}
    .videoBox{
      border-radius:14px;
      overflow:hidden;
      background:#000;
      width:100%;
      height:100%;
      position:relative;
    }
    .videoBox iframe{
      width:100%;
      height:100%;
      border:0;
      pointer-events:none; /* 让整张卡片仍然可点击跳转 */
    }
    .videoTag{
      position:absolute;
      left:14px; top:14px;
      z-index:3;
      background:rgba(255,255,255,.9);
      padding:8px 10px;
      border-radius:999px;
      font-size:14px;
      font-weight:800;
    }

    @media (max-width:1100px){
      .top{grid-template-columns:180px 1fr 220px;}
      .badge{min-width:420px; font-size:30px;}
      .grid{grid-template-columns: repeat(2, 1fr);}
    }
    @media (max-width:720px){
      .top{grid-template-columns:1fr; justify-items:center;}
      .badge{min-width:0; width:100%; font-size:28px;}
      .langBtn{width:100%;}
      .grid{grid-template-columns:1fr;}
      .card{height:320px;}
    }
  </style>
</head>
<body>
  <div class="wrap">
    <div class="top">
      <!-- 头像：你可以先不放，或之后把图片上传到 /assets/avatar.png -->
    <img src="avatar.jpg" alt="avatar" width="330" style="image-rendering: pixelated;">

      <div class="titleBadge">
        <div class="badge">ポートフォリオ</div>
      </div>

      <button class="langBtn" id="langBtn">语言 EN/JP/CH</button>
    </div>

    <div class="grid">
      <!-- 自我介绍（先占位，之后你再做 about 页面） -->
      <a class="card" href="#" onclick="alert('这里之后接自我介绍页（about）'); return false;">
        <div class="label">自我介绍</div>
      </a>

      <!-- 项目经历（先占位，之后你再做 projects 页面） -->
      <a class="card" href="#" onclick="alert('这里之后接项目经历页（projects）'); return false;">
        <div class="label">项目经历</div>
      </a>

      <!-- VTuber：直接嵌入你的 YouTube Shorts，整张卡点击会在新标签打开 -->
      <a class="card video"
         href="https://www.youtube.com/shorts/9y1Tc6-LKw0"
         target="_blank" rel="noopener">
        <div class="videoTag">vtuber设计</div>
        <div class="videoBox">
          <iframe
            src="https://www.youtube.com/embed/9y1Tc6-LKw0"
            title="VTuber YouTube"
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
            allowfullscreen></iframe>
        </div>
      </a>

      <!-- 年贺状：跳转到你旧站的年贺状页面（最稳） -->
      <a class="card"
         href="https://anine998.github.io/998.github.io/newyear2026/"
         target="_blank" rel="noopener">
        <div class="label">年贺状</div>
      </a>
    </div>
  </div>

  <script>
    document.getElementById('langBtn').addEventListener('click', () => {
      alert('下一步可以做：EN/JP/CH 三套文字切换（先把布局跑通）。');
    });
  </script>
</body>
</html>
