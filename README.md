# dozeroaoprimeiroriff
<!doctype html>
<html lang="pt-BR">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width,initial-scale=1" />
<title>Domine a Guitarra – Do Zero ao Primeiro Riff</title>

<!-- FONTS -->
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&family=Inter:wght@300;400;600&display=swap" rel="stylesheet">

<style>
  /* === VARIÁVEIS === */
  :root{
    --bg: #24151a;
    --card: #1a1316;
    --muted: #cfc6c8;
    --text: #fff6f6;
    --accent: #ffb300;
    --primary: #29bb40;
    --primary-hover: #23a636;
    --glass: rgba(255,255,255,0.03);
    --radius: 14px;
    --maxw: 1120px;
    --gap: 22px;
  }

  /* === RESET === */
  *{box-sizing:border-box}
  html,body{height:100%;margin:0;font-family:'Poppins',Inter,system-ui,-apple-system,Segoe UI; background:linear-gradient(180deg,var(--bg), #3b212b); color:var(--text); -webkit-font-smoothing:antialiased;}
  img{max-width:100%;display:block}
  a{color:inherit;text-decoration:none}
  .container{width:min(var(--maxw),94vw);margin:0 auto;padding:0 16px}

  /* === ESPAÇAMENTO GLOBAL === */
  h1, h2, h3, h4, p, ul, details { margin-bottom: 16px; }

  /* HERO */
  header{padding:60px 0 40px}
  .hero{display:grid;grid-template-columns:1fr 420px;gap:var(--gap);align-items:center}
  @media (max-width:980px){ .hero{grid-template-columns:1fr;gap:18px} }
  .badge{display:inline-flex;align-items:center;gap:8px;background:var(--glass);border:1px solid rgba(255,255,255,0.04);padding:8px 12px;border-radius:999px;color:var(--accent);font-weight:700;font-size:12px}
  h1{font-size:clamp(26px,3.6vw,44px);line-height:1.03;margin:20px 0 16px;color:var(--text)}
  p.lead{color:var(--muted);font-size:16px;margin-bottom:18px}
  .hero-ctas{display:flex;gap:12px;margin-top:18px;flex-wrap:wrap}
  .btn{background:var(--primary); color:#081206; font-weight:800; padding:12px 22px;border-radius:999px;border:0;cursor:pointer;display:inline-block; box-shadow:0 6px 18px rgba(41,187,64,0.14); transition:all .18s ease;}
  .btn:hover{transform:translateY(-3px);background:var(--primary-hover)}
  .btn.secondary{background:transparent;color:var(--text);border:1px solid rgba(255,255,255,0.06);box-shadow:none;padding:10px 18px;font-weight:700;}
  .btn:focus{outline:3px solid rgba(255,255,255,0.06);outline-offset:2px}
  .hero-card{background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01)); border:1px solid rgba(255,255,255,0.04); padding:24px;border-radius:var(--radius); box-shadow:0 8px 30px rgba(0,0,0,0.45);}
  .hero-grid{display:grid;grid-template-columns:1fr 1fr;gap:20px}
  .hero-grid h3{margin-bottom:12px;font-size:15px}
  .small-muted{color:var(--muted);font-size:14px;margin-top:8px}

  /* VSL */
  .vsl-wrap{display:flex;flex-direction:column;align-items:center;margin:50px auto;gap:20px;max-width:760px;padding:0 6px}
  .vsl-card{width:100%;background:var(--card);border-radius:16px;padding:28px;border:1px solid rgba(255,255,255,0.03); box-shadow:0 10px 30px rgba(0,0,0,0.45);}
  .vsl-title{color:var(--accent);font-weight:800;margin-bottom:18px;font-size:18px;text-align:center}
  .video-wrapper{position:relative;width:100%;padding-bottom:56.25%;border-radius:12px;overflow:hidden;border:2px solid rgba(0,0,0,0.35);background:#000}
  .video-wrapper video{position:absolute;inset:0;width:100%;height:100%;object-fit:cover}
  .vsl-info{color:var(--muted);font-size:14px;margin-top:16px;text-align:center}
  .ticker{margin-top:14px;overflow:hidden;border-radius:10px;padding:8px;background:linear-gradient(90deg, rgba(255,179,0,0.04), rgba(255,179,0,0.02));border:1px solid rgba(255,179,0,0.06)}
  .ticker-track{display:inline-block;white-space:nowrap;padding-left:2%;animation:scroll 18s linear infinite}
  .ticker-item{display:inline-block;padding:0 28px;color:var(--text);font-weight:700;opacity:0.98}
  @keyframes scroll{0%{transform:translateX(0)}100%{transform:translateX(-50%)}}

  /* PROOF */
  .proof{margin:50px auto;padding:18px;background:linear-gradient(180deg, rgba(0,0,0,0.18), rgba(0,0,0,0.06));border-radius:12px;border:1px solid rgba(255,255,255,0.02)}
  .proof-inner{display:grid;grid-template-columns:repeat(4,1fr);gap:14px;align-items:center}
  @media (max-width:760px){ .proof-inner{grid-template-columns:repeat(2,1fr)} }
  .proof-item{font-size:14px;color:var(--muted);text-align:center;padding:12px 8px}

  /* SECTIONS */
  section{padding:70px 0}
  .section-title{font-size:22px;margin-bottom:20px}
  .section-sub{color:var(--muted);margin-bottom:36px}

  /* Cards */
  .cards{
    display:grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap:50px; /* aumentei o espaçamento */
    margin:40px auto;
    max-width:900px;
    justify-content:center;
  }
  .card{
    background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));
    padding:28px;
    border-radius:12px;
    border:1px solid rgba(255,255,255,0.03);
    margin:0 auto;
  }

  /* Features */
  .features{
    display:grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap:40px;
    margin:40px auto;
    max-width:900px;
    justify-content:center;
  }
  .feature{
    background:var(--card);
    padding:28px;
    border-radius:12px;
    border:1px solid rgba(255,255,255,0.03);
    margin:0 auto;
  }
  .feature h4{margin-bottom:12px}

  /* PRICING */
  .pricing{display:grid;grid-template-columns:2fr 1fr;gap:50px;align-items:start;margin-top:50px}
  @media (max-width:980px){ .pricing{grid-template-columns:1fr} }
  .price-box{background:var(--card);padding:30px;border-radius:12px;border:1px solid rgba(255,255,255,0.03);margin-top:20px}
  .price-row{display:flex;align-items:center;gap:20px;margin-bottom:20px}
  .old{color:#9e8f8f;text-decoration:line-through}
  .price-now{font-size:34px;font-weight:900;color:var(--accent)}
  .guarantee{background:linear-gradient(180deg, rgba(255,255,255,0.01), rgba(255,255,255,0.00));padding:26px;border-radius:12px;border:1px solid rgba(255,255,255,0.02);margin-bottom:20px}

  /* FAQ */
  section.faq-section { /* fundo uniforme corrigido */
    background:var(--bg);
    padding:70px 0;
  }
  .faq{display:grid;grid-template-columns:1fr 1fr;gap:20px;margin-top:30px}
  @media (max-width:980px){ .faq{grid-template-columns:1fr} }
  details{background:var(--card);padding:20px;border-radius:10px;border:1px solid rgba(255,255,255,0.02);margin-bottom:16px}

  /* FOOTER */
  footer{padding:36px 0;color:var(--muted);font-size:14px;border-top:1px solid rgba(255,255,255,0.02);margin-top:60px}
</style>
</head>
<body>

<!-- HERO -->

<p>    <p/>

<p>    <p/>

<header class="container">
  <div class="hero">
    <div>
      <div class="badge">LANÇAMENTO • MÉTODO PRÁTICO</div>
      <h1>DOMINE A GUITARRA DO ZERO AO INTERMEDIÁRIO</h1>
      <p class="lead">Aprenda acordes, riffs, solos e improviso com um passo a passo direto, visual e sem enrolação.</p>
      <div class="hero-ctas">
        <a class="btn" href="#comprar">QUERO COMEÇAR</a>
        <a class="btn secondary" href="#conteudo">VER CONTEÚDO</a>
      </div>
      <p class="small-muted">Por <strong>Pedro Henrique</strong> • Guitarrista desde os 7 anos</p>
    </div>
    <aside class="hero-card">
      <div class="hero-grid">
        <div><h3>O que você recebe</h3><p class="small-muted">E-book + Parte 2 intermediário + PDFs de escalas</p></div>
        <div><h3>Resultados práticos</h3><p class="small-muted">Tocar riffs, solar e montar timbres que soam bem</p></div>
      </div>
    </aside>
  </div>
</header>

<!-- VSL -->
<div class="vsl-wrap container">
  <div class="vsl-card">
    <h3 class="vsl-title">ASSISTA AO VÍDEO ABAIXO</h3>
    <div class="video-wrapper">
      <video controls playsinline poster="thumbnail.jpg">
        <source src="C:\Users\pedro\Downloads/videovsl.mp4" type="video/mp4">
        Seu navegador não suporta a reprodução de vídeo.
      </video>
    </div>
    <div class="vsl-info">Veja como funciona o método na prática</div>
    <div class="ticker">
      <div class="ticker-track">
        <span class="ticker-item">🔥 OFERTA DE LANÇAMENTO: -50% HOJE</span>
        <span class="ticker-item">🎁 Bônus exclusivos incluídos</span>
        <span class="ticker-item">🛡 Garantia de 7 dias</span>
      </div>
    </div>
  </div>
</div>

<!-- PROOF -->
<div class="container">
  <div class="proof">
    <div class="proof-inner">
      <div class="proof-item">✅ Acesso imediato</div>
      <div class="proof-item">🛡 Garantia 7 dias</div>
      <div class="proof-item">🎁 Bônus exclusivos</div>
      <div class="proof-item">🔄 Atualizações vitalícias</div>
    </div>
  </div>
</div>

<!-- CONTEÚDO -->
<section id="conteudo" class="container">
  <h2 class="section-title">O que você vai aprender</h2>
  <p class="section-sub">Do zero absoluto até conseguir tocar suas primeiras músicas completas.</p>
  <p>                 <p/>
  <div class="cards">
    <article class="card">
      <h3>Parte 1 – Iniciante</h3>
      <ul class="small-muted">
        <li>Postura correta para evitar dores</li>
        <li>Como segurar a palheta e palhetar sem travar</li>
        <li>Acordes básicos mais usados (maiores e menores)</li>
        <li>Primeiros riffs fáceis para ganhar confiança</li>
        <li>Batidas rítmicas para acompanhar músicas</li>
        <li>Leitura simples de tablaturas (tabs)</li>
        <li>Tocar músicas completas já nas primeiras semanas</li>
      </ul>
    </article>
    <article class="card">
      <h3>Bônus</h3>
      <ul class="small-muted">
        <li>Guia de manutenção do instrumento (mantendo afinação e regulagem)</li>
        <li>PDFs com todas as tablaturas usadas no curso</li>
        <li>Dicas de treino para acelerar o aprendizado</li>
        <li>Recomendações de apps e recursos para praticar</li>
      </ul>
    </article>
  </div>
</section>

<!-- PREÇO -->
<section id="comprar" class="container">
  <div class="pricing">
    <div class="guarantee">
      <h3>Garantia 7 dias</h3>
      <p class="small-muted">Teste sem risco: se não gostar, devolvemos 100% do valor investido, sem burocracia.</p>
    </div>
    <div class="price-box center">
      <div class="price-row"><div class="old">R$ 45,90</div><div class="price-now">R$ 20,90</div></div>
      <p class="small-muted">Oferta de lançamento</p>
      <a class="btn" href="https://hotmart.com/pt-br/marketplace/produtos/acesso-vitalicio-audio-expert-gold/X89238379J">GARANTIR AGORA</a>
    </div>
  </div>
</section>

<!-- FAQ -->
<section class="faq-section">
  <div class="container">
    <h2 class="section-title">Perguntas frequentes</h2>
    <div class="faq">
      <details>
        <summary>É para iniciantes?</summary>
        <p>
          Sim! Esse guia foi criado justamente para quem nunca pegou em uma guitarra antes. 
          Você vai aprender desde como segurar o instrumento até tocar suas primeiras músicas completas, 
          de forma simples, direta e prática.
        </p>
      </details>
      <details>
        <summary>Preciso de guitarra cara?</summary>
        <p>
          Não. Uma guitarra de entrada já é suficiente para aplicar tudo o que ensino. 
          O mais importante é praticar. Inclusive, muitas dicas podem ser adaptadas até mesmo no violão, 
          caso você não tenha uma guitarra ainda.
        </p>
      </details>
      <details>
        <summary>Recebo na hora?</summary>
        <p>
          Sim! Assim que o pagamento for confirmado, você recebe imediatamente o link para baixar o e-book e os bônus. 
          Nada de esperar dias: você já pode começar a estudar no mesmo instante.
        </p>
      </details>
      <details>
        <summary>Tenho suporte?</summary>
        <p>
          Sim. Você terá acesso direto a mim para tirar dúvidas pontuais e receber orientações. 
          Não vai ficar perdido tentando aprender sozinho — terá apoio para continuar evoluindo.
        </p>
      </details>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer class="container center">
  <p>© 2025 Pedro Henrique – Todos os direitos reservados.</p>
</footer>

</body>
</html>
