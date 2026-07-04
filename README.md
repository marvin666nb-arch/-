<!doctype html>
<html lang="zh-CN">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>正在下载源码 ZIP - 程序员在线工具箱</title>
  <meta name="robots" content="noindex">
  <style>
    body{margin:0;font-family:Arial,"Microsoft YaHei",sans-serif;background:#f8fafc;color:#172033}
    main{min-height:100vh;display:grid;place-items:center;padding:24px}
    section{max-width:560px;border:1px solid #bfdbfe;background:#fff;border-radius:8px;padding:28px;box-shadow:0 12px 28px rgba(37,99,235,.10)}
    h1{margin:0 0 12px;font-size:24px}
    p{line-height:1.8;color:#475569}
    a{color:#2563eb;font-weight:700}
  </style>
</head>
<body>
  <main>
    <section>
      <h1>正在开始下载</h1>
      <p>页面会自动跳转到 GitHub 源码 ZIP 下载地址。如果没有自动下载，请点击下面链接。</p>
      <p><a id="downloadLink" href="#">点击自动下载源码 ZIP</a></p>
    </section>
  </main>
  <script>
    (function(){
      var host = location.hostname;
      var parts = location.pathname.split('/').filter(Boolean);
      var user = '';
      var repo = '';
      if (/\.github\.io$/i.test(host)) {
        user = host.replace(/\.github\.io$/i, '');
        repo = parts[0] || '';
      }
      var url = user && repo
        ? 'https://github.com/' + encodeURIComponent(user) + '/' + encodeURIComponent(repo) + '/archive/refs/heads/main.zip'
        : 'https://github.com/你的GitHub用户名/仓库名/archive/refs/heads/main.zip';
      var link = document.getElementById('downloadLink');
      link.href = url;
      setTimeout(function(){ location.href = url; }, 500);
    })();
  </script>
</body>
</html>
