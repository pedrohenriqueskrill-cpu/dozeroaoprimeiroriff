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
    --maxw: 1200px;
    --gap: 32px;
    --section-padding: 80px;
  }

  /* === RESET === */
  *{
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }
  
  html, body{
    height: 100%;
    font-family: 'Poppins', Inter, system-ui, -apple-system, 'Segoe UI', sans-serif;
    background: linear-gradient(180deg, var(--bg), #3b212b);
    color: var(--text);
    -webkit-font-smoothing: antialiased;
    line-height: 1.6;
  }
  
  img{
    max-width: 100%;
    display: block;
    height: auto;
  }
  
  a{
    color: inherit;
    text-decoration: none;
  }
  
  .container{
    width: min(var(--maxw), 95vw);
    margin: 0 auto;
    padding: 0 20px;
  }

  /* === ESPAÇAMENTO GLOBAL MELHORADO === */
  h1, h2, h3, h4 { 
    margin-bottom: 1rem;
    line-height: 1.2;
  }
  
  p, ul, details { 
    margin-bottom: 1.25rem;
  }

  /* === HERO MELHORADO === */
  header{
    padding: var(--section-padding) 0 60px;
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
  
  .hero{
    display: grid;
    grid-template-columns: 1.2fr 0.8fr;
    gap: var(--gap);
    align-items: center;
    width: 100%;
  }
  
  @media (max-width: 1024px){ 
    .hero{
      grid-template-columns: 1fr;
      gap: 2rem;
      text-align: center;
    }
    
    header{
      min-height: auto;
      padding: 60px 0 40px;
    }
  }
  
  .badge{
    display: inline-flex;
    align-items: center;
    gap: 8px;
    background: var(--glass);
    border: 1px solid rgba(255,255,255,0.08);
    padding: 10px 16px;
    border-radius: 999px;
    color: var(--accent);
    font-weight: 700;
    font-size: 13px;
    margin-bottom: 1.5rem;
    backdrop-filter: blur(10px);
  }
  
  h1{
    font-size: clamp(2rem, 4vw, 3.5rem);
    line-height: 1.1;
    margin-bottom: 1.5rem;
    color: var(--text);
    font-weight: 700;
  }
  
  p.lead{
    color: var(--muted);
    font-size: 1.125rem;
    margin-bottom: 2rem;
    max-width: 600px;
  }
  
  .hero-ctas{
    display: flex;
    gap: 1rem;
    margin-top: 2rem;
    flex-wrap: wrap;
  }
  
  .btn{
    background: var(--primary);
    color: #081206;
    font-weight: 800;
    padding: 16px 32px;
    border-radius: 999px;
    border: 0;
    cursor: pointer;
    display: inline-block;
    box-shadow: 0 8px 24px rgba(41,187,64,0.2);
    transition: all 0.3s ease;
    font-size: 1rem;
    text-transform: uppercase;
    letter-spacing: 0.5px;
  }
  
  .btn:hover{
    transform: translateY(-4px);
    background: var(--primary-hover);
    box-shadow: 0 12px 32px rgba(41,187,64,0.3);
  }
  
  .btn.secondary{
    background: transparent;
    color: var(--text);
    border: 2px solid rgba(255,255,255,0.1);
    box-shadow: none;
    padding: 14px 30px;
    font-weight: 700;
  }
  
  .btn.secondary:hover{
    background: rgba(255,255,255,0.05);
    border-color: rgba(255,255,255,0.2);
  }
  
  .btn:focus{
    outline: 3px solid rgba(255,255,255,0.1);
    outline-offset: 2px;
  }
  
  .hero-card{
    background: linear-gradient(135deg, rgba(255,255,255,0.05), rgba(255,255,255,0.02));
    border: 1px solid rgba(255,255,255,0.08);
    padding: 2rem;
    border-radius: 20px;
    box-shadow: 0 20px 40px rgba(0,0,0,0.3);
    backdrop-filter: blur(20px);
  }
  
  .hero-grid{
    display: grid;
    grid-template-columns: 1fr;
    gap: 1.5rem;
  }
  
  .hero-grid > div{
    padding: 1rem;
    background: rgba(255,255,255,0.02);
    border-radius: 12px;
    border: 1px solid rgba(255,255,255,0.05);
  }
  
  .hero-grid h3{
    margin-bottom: 0.75rem;
    font-size: 1rem;
    color: var(--accent);
    font-weight: 600;
  }
  
  .small-muted{
    color: var(--muted);
    font-size: 0.875rem;
    margin-top: 1rem;
  }

  /* === VSL MELHORADO === */
  .vsl-wrap{
    display: flex;
    flex-direction: column;
    align-items: center;
    margin: var(--section-padding) auto;
    gap: 2rem;
    max-width: 800px;
    padding: 0 1rem;
  }
  
  .vsl-card{
    width: 100%;
    background: var(--card);
    border-radius: 24px;
    padding: 2.5rem;
    border: 1px solid rgba(255,255,255,0.05);
    box-shadow: 0 20px 40px rgba(0,0,0,0.4);
  }
  
  .vsl-title{
    color: var(--accent);
    font-weight: 800;
    margin-bottom: 2rem;
    font-size: 1.25rem;
    text-align: center;
    text-transform: uppercase;
    letter-spacing: 1px;
  }
  
  .video-wrapper{
    position: relative;
    width: 100%;
    padding-bottom: 56.25%;
    border-radius: 16px;
    overflow: hidden;
    border: 3px solid rgba(0,0,0,0.5);
    background: #000;
    box-shadow: 0 10px 30px rgba(0,0,0,0.5);
  }
  
  .video-wrapper video{
    position: absolute;
    inset: 0;
    width: 100%;
    height: 100%;
    object-fit: cover;
  }
  
  .vsl-info{
    color: var(--muted);
    font-size: 0.875rem;
    margin-top: 1.5rem;
    text-align: center;
  }
  
  .ticker{
    margin-top: 1.5rem;
    overflow: hidden;
    border-radius: 12px;
    padding: 1rem;
    background: linear-gradient(90deg, rgba(255,179,0,0.08), rgba(255,179,0,0.04));
    border: 1px solid rgba(255,179,0,0.1);
  }
  
  .ticker-track{
    display: inline-block;
    white-space: nowrap;
    padding-left: 2%;
    animation: scroll 20s linear infinite;
  }
  
  .ticker-item{
    display: inline-block;
    padding: 0 2rem;
    color: var(--text);
    font-weight: 700;
    opacity: 0.95;
  }
  
  @keyframes scroll{
    0%{transform: translateX(0)}
    100%{transform: translateX(-50%)}
  }

  /* === PROOF MELHORADO === */
  .proof{
    margin: var(--section-padding) auto;
    padding: 1.5rem;
    background: linear-gradient(135deg, rgba(0,0,0,0.2), rgba(0,0,0,0.1));
    border-radius: 16px;
    border: 1px solid rgba(255,255,255,0.05);
    backdrop-filter: blur(10px);
  }
  
  .proof-inner{
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 1rem;
    align-items: center;
  }
  
  .proof-item{
    font-size: 0.875rem;
    color: var(--muted);
    text-align: center;
    padding: 1rem;
    background: rgba(255,255,255,0.02);
    border-radius: 10px;
    border: 1px solid rgba(255,255,255,0.05);
    transition: all 0.3s ease;
  }
  
  .proof-item:hover{
    background: rgba(255,255,255,0.05);
    transform: translateY(-2px);
  }

  /* === SECTIONS MELHORADAS === */
  section{
    padding: var(--section-padding) 0;
  }
  
  .section-title{
    font-size: 2.5rem;
    margin-bottom: 1.5rem;
    text-align: center;
    font-weight: 700;
  }
  
  .section-sub{
    color: var(--muted);
    margin-bottom: 3rem;
    text-align: center;
    font-size: 1.125rem;
    max-width: 600px;
    margin-left: auto;
    margin-right: auto;
  }

  /* === CARDS MELHORADOS === */
  .cards{
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
    gap: 2rem;
    margin: 3rem auto;
    max-width: 1000px;
    justify-content: center;
  }
  
  .card{
    background: linear-gradient(135deg, rgba(255,255,255,0.05), rgba(255,255,255,0.02));
    padding: 2.5rem;
    border-radius: 20px;
    border: 1px solid rgba(255,255,255,0.08);
    margin: 0 auto;
    transition: all 0.3s ease;
    backdrop-filter: blur(10px);
  }
  
  .card:hover{
    transform: translateY(-8px);
    box-shadow: 0 20px 40px rgba(0,0,0,0.3);
    border-color: rgba(255,255,255,0.15);
  }
  
  .card h3{
    color: var(--accent);
    font-size: 1.5rem;
    margin-bottom: 1.5rem;
    font-weight: 600;
  }
  
  .card ul{
    list-style: none;
    padding: 0;
  }
  
  .card li{
    padding: 0.5rem 0;
    border-bottom: 1px solid rgba(255,255,255,0.05);
    position: relative;
    padding-left: 1.5rem;
  }
  
  .card li:before{
    content: "✓";
    position: absolute;
    left: 0;
    color: var(--primary);
    font-weight: bold;
  }
  
  .card li:last-child{
    border-bottom: none;
  }

  /* === PRICING MELHORADO === */
  .pricing{
    display: grid;
    grid-template-columns: 1.5fr 1fr;
    gap: 3rem;
    align-items: start;
    margin-top: 3rem;
  }
  
  @media (max-width: 1024px){ 
    .pricing{
      grid-template-columns: 1fr;
      gap: 2rem;
    }
  }
  
  .price-box{
    background: linear-gradient(135deg, var(--card), #2a1a20);
    padding: 2.5rem;
    border-radius: 20px;
    border: 2px solid rgba(255,179,0,0.2);
    margin-top: 1rem;
    text-align: center;
    box-shadow: 0 20px 40px rgba(0,0,0,0.3);
    position: relative;
    overflow: hidden;
  }
  
  .price-box:before{
    content: "";
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    height: 4px;
    background: linear-gradient(90deg, var(--accent), var(--primary));
  }
  
  .price-row{
    display: flex;
    align-items: center;
    gap: 1.5rem;
    margin-bottom: 1.5rem;
    justify-content: center;
  }
  
  .old{
    color: #9e8f8f;
    text-decoration: line-through;
    font-size: 1.25rem;
  }
  
  .price-now{
    font-size: 3rem;
    font-weight: 900;
    color: var(--accent);
  }
  
  .guarantee{
    background: linear-gradient(135deg, rgba(255,255,255,0.03), rgba(255,255,255,0.01));
    padding: 2rem;
    border-radius: 16px;
    border: 1px solid rgba(255,255,255,0.05);
    margin-bottom: 1.5rem;
  }
  
  .guarantee h3{
    color: var(--primary);
    margin-bottom: 1rem;
    font-size: 1.25rem;
  }

  /* === FAQ MELHORADO === */
  section.faq-section {
    background: var(--bg);
    padding: var(--section-padding) 0;
  }
  
  .faq{
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(400px, 1fr));
    gap: 1.5rem;
    margin-top: 2rem;
  }
  
  details{
    background: var(--card);
    padding: 1.5rem;
    border-radius: 16px;
    border: 1px solid rgba(255,255,255,0.05);
    margin-bottom: 1rem;
    transition: all 0.3s ease;
  }
  
  details:hover{
    border-color: rgba(255,255,255,0.1);
    box-shadow: 0 8px 24px rgba(0,0,0,0.2);
  }
  
  details summary{
    cursor: pointer;
    font-weight: 600;
    color: var(--accent);
    margin-bottom: 1rem;
    font-size: 1.1rem;
  }
  
  details[open] summary{
    margin-bottom: 1rem;
    padding-bottom: 1rem;
    border-bottom: 1px solid rgba(255,255,255,0.1);
  }

  /* === FOOTER MELHORADO === */
  footer{
    padding: 3rem 0;
    color: var(--muted);
    font-size: 0.875rem;
    border-top: 1px solid rgba(255,255,255,0.05);
    margin-top: 4rem;
    text-align: center;
    background: rgba(0,0,0,0.2);
  }

  /* === RESPONSIVIDADE MELHORADA === */
  @media (max-width: 768px){
    .container{
      padding: 0 1rem;
    }
    
    .hero-ctas{
      flex-direction: column;
      align-items: center;
    }
    
    .btn{
      width: 100%;
      max-width: 300px;
    }
    
    .cards{
      grid-template-columns: 1fr;
      gap: 1.5rem;
    }
    
    .section-title{
      font-size: 2rem;
    }
    
    .vsl-card{
      padding: 1.5rem;
    }
  }
</style>
</head>
<body>

<!-- HERO -->
<header class="container">
  <div class="hero">
    <div>
      <div class="badge">🎸 LANÇAMENTO • MÉTODO PRÁTICO</div>
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
        <div>
          <h3>O que você recebe</h3>
          <p class="small-muted">E-book + Parte 2 intermediário + PDFs de escalas</p>
        </div>
        <div>
          <h3>Resultados práticos</h3>
          <p class="small-muted">Tocar riffs, solar e montar timbres que soam bem</p>
        </div>
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
        <source src="videovsl.mp4" type="video/mp4">
        Seu navegador não suporta a reprodução de vídeo.
      </video>
    </div>
    <div class="vsl-info">Veja como funciona o método na prática</div>
    <div class="ticker">
      <div class="ticker-track">
        <span class="ticker-item">🔥 OFERTA DE LANÇAMENTO: -50% HOJE</span>
        <span class="ticker-item">🎁 Bônus exclusivos incluídos</span>
        <span class="ticker-item">🛡 Garantia de 7 dias</span>
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
      <h3>🛡 Garantia 7 dias</h3>
      <p class="small-muted">Estamos confiantes de que você vai adorar o seu produto. Por isso, oferecemos 7 dias de garantia: se dentro desse período você não ficar totalmente satisfeito, basta entrar em contato conosco e devolver o produto para receber seu reembolso completo, sem complicações. Sua satisfação é a nossa prioridade!</p>
    </div>
    <div class="price-box">
      <div class="price-row">
        <div class="old">R$ 45,90</div>
        <div class="price-now">R$ 20,90</div>
      </div>
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
<footer class="container">
  <p>© 2025 Pedro Henrique – Todos os direitos reservados.</p>
</footer>

</body>
</html>

