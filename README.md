<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>🖼️ OCR Detector - Screenshots MeLi</title>
  <style>
    :root{
      --bg:#0f172a; /* slate-900 */
      --card:#111827; /* gray-900 */
      --muted:#94a3b8; /* slate-400 */
      --text:#e5e7eb; /* gray-200 */
      --accent:#22d3ee; /* cyan-400 */
      --ok:#22c55e; /* green-500 */
      --border:rgba(255,255,255,.08);
    }
    *{box-sizing:border-box}
    html,body{height:100%}
    body{margin:0;background:linear-gradient(180deg,var(--bg),#060b1b);color:var(--text);font:16px/1.6 system-ui, -apple-system, Segoe UI, Roboto, Ubuntu, Cantarell, Noto Sans, Helvetica, Arial, "Apple Color Emoji","Segoe UI Emoji"}
    .wrap{max-width:900px;margin:48px auto;padding:0 20px}
    header{display:flex;align-items:center;gap:14px;margin-bottom:24px}
    .logo{font-size:32px}
    h1{font-size:clamp(28px,4vw,40px);margin:0}
    h2{margin:28px 0 12px;font-size:22px}
    p.lead{color:var(--muted);margin:6px 0 0}
    .card{background:linear-gradient(180deg,rgba(255,255,255,.03),rgba(255,255,255,.02));border:1px solid var(--border);border-radius:18px;padding:18px 18px}
    code, pre{font-family: ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, "Liberation Mono", "Courier New", monospace}
    pre{background:#0b1226;border:1px solid var(--border);border-radius:14px;padding:14px;overflow:auto}
    .list{display:grid;gap:8px;padding-left:18px}
    a{color:var(--accent);text-decoration:none}
    a:hover{text-decoration:underline}
    .badge{display:inline-block;background:rgba(34,211,238,.12);border:1px solid rgba(34,211,238,.35);color:var(--accent);padding:2px 8px;border-radius:999px;font-size:12px}
    .footer{margin-top:36px;color:var(--muted);font-size:14px}
    .pill{display:inline-flex;align-items:center;gap:8px;border:1px solid var(--border);border-radius:999px;padding:6px 10px;background:rgba(255,255,255,.03)}
    .grid{display:grid;gap:16px}
    @media (min-width:800px){.grid{grid-template-columns:1fr 1fr}}
  </style>
</head>
<body>
  <div class="wrap">
    <header>
      <div class="logo">🖼️</div>
      <div>
        <h1>OCR Detector – Screenshots MeLi</h1>
        <p class="lead">Script para detectar <strong>“usado”</strong> y términos de <strong>refacciones</strong> en títulos usando Tesseract OCR.</p>
      </div>
    </header>

    <section class="card">
      <span class="badge">Sencillo · Directo · En tu estilo</span>
      <h2>⚙️ Requisitos</h2>
      <ul class="list">
        <li>Python 3.9+</li>
        <li>Instalar librerías:
          <pre><code>pip install pillow pytesseract</code></pre>
        </li>
        <li>
          Tesseract OCR instalado 👉
          <a href="https://github.com/tesseract-ocr/tesseract" target="_blank" rel="noopener">Repositorio oficial</a>
          <br />
          Ruta ya configurada en el script:
          <pre><code>pytesseract.pytesseract.tesseract_cmd = r'C:\Users\dreynosoh\AppData\Local\Programs\Tesseract-OCR\tesseract.exe'</code></pre>
        </li>
      </ul>
    </section>

    <section class="card">
      <h2>📋 requirements.txt</h2>
      <p>Recomendado instalar con <code>pip install -r requirements.txt</code>. Contenido sugerido:</p>
      <pre><code>pytesseract==0.3.10
Pillow==10.3.0
selenium==4.21.0
numpy==1.26.4
opencv-python==4.11.0.86  # Compatible con numpy 1.26.4
pdf2image==1.17.0  # Si quieres leer PDFs escaneados</code></pre>
      <p class="pill">Nota: <code>opencv-python</code> y <code>pdf2image</code> son opcionales según tu flujo.</p>
    </section>

    <div class="grid">
      <section class="card">
        <h2>🚀 Uso</h2>
        <ol class="list">
          <li>Coloca tus <strong>screenshots</strong> en una carpeta.</li>
          <li>Actualiza la variable <code>screens</code> al final del script.</li>
          <li>Instala dependencias y ejecuta:
            <pre><code>pip install -r requirements.txt
python ocr_detect.py</code></pre>
          </li>
        </ol>
      </section>

      <section class="card">
        <h2>🔍 ¿Qué hace?</h2>
        <ul class="list">
          <li><code>extraer_texto_ocr()</code> → busca palabras relacionadas con <strong>“usado”</strong>.</li>
          <li><code>ref_extraer_texto_ocr()</code> → recorta el área del título y busca términos de <strong>refacciones</strong>.</li>
        </ul>
        <p>Ejemplo de salida:</p>
        <pre><code>Encontradas palabras que empiezan con "usado" en img1.png:
- Usado
- (usado)

No se encontraron palabras que empiecen con "refacciones" en img2.png. 👍</code></pre>
      </section>
    </div>

    <section class="card">
      <h2>📦 Output</h2>
      <p>Devuelve una <strong>lista con los nombres de las imágenes</strong> que traen las palabras detectadas e imprime los matches en consola.</p>
    </section>

    <section class="card">
      <h2>✍️ Nota personal</h2>
      <p>Hecho para revisar rápido screenshots de publicaciones en Mercado Libre y marcar cuáles se detectan como <strong>usadas</strong> o <strong>refacciones</strong>. Menos manual, más foco. 👌</p>
      <p class="pill">Tip: ajusta el <code>--psm</code> o la región del <code>crop()</code> si cambian los layouts.</p>
    </section>

    <p class="footer">© Tu script, tus reglas. 🚀</p>
  </div>
</body>
</html>
