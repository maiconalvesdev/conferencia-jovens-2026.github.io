<!doctype html>
<html lang="pt-BR">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Conferência dos Jovens 2026 — Estaca Mossoró</title>
  <meta name="description" content="Conferência dos Jovens 2026 — Estaca Mossoró. 14 à 17 de fevereiro. Tema: 'Anda Comigo' (Moisés 6:36)." />

  <!-- Fontes parecidas com o estilo Canva do PDF -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Caveat:wght@700&family=Fredoka:wght@500;600;700&display=swap" rel="stylesheet">

  <style>
    :root{
      /* Paleta aproximada do PDF */
      --bg: #d9f2ef;          /* verde-água claro */
      --blue: #0b5f7a;        /* azul do texto/títulos */
      --blue2:#0a4f65;        /* azul mais escuro */
      --orange:#f29a2e;       /* laranja do "Estaca Mossoró" e datas */
      --white:#ffffff;

      --shadow: 0 18px 45px rgba(0,0,0,.16);
      --shadow2: 0 10px 26px rgba(0,0,0,.14);
      --line: rgba(11,95,122,.18);

      --max: 1120px;
      --r: 18px;
    }

    *{ box-sizing:border-box; }
    body{
      margin:0;
      font-family: "Fredoka", system-ui, -apple-system, Segoe UI, Roboto, Arial, sans-serif;
      background: var(--bg);
      color: var(--blue2);
      line-height: 1.35;
    }

    a{ color: inherit; text-decoration:none; }
    .container{ width:min(var(--max), calc(100% - 44px)); margin: 0 auto; }

    /* Header (discreto, para não “brigar” com o layout do PDF) */
    header{
      position: sticky;
      top: 0;
      z-index: 30;
      background: rgba(217,242,239,.84);
      backdrop-filter: blur(10px);
      border-bottom: 1px solid var(--line);
    }
    .nav{
      display:flex;
      align-items:center;
      justify-content:space-between;
      gap: 12px;
      padding: 12px 0;
    }
    .brand{
      display:flex;
      align-items:center;
      gap: 10px;
      font-weight: 700;
      color: var(--blue);
    }
    .badgeDot{
      width: 12px; height: 12px; border-radius: 999px;
      background: var(--orange);
      box-shadow: 0 0 0 7px rgba(242,154,46,.18);
    }
    .links{
      display:flex;
      gap: 14px;
      color: var(--blue);
      font-weight: 600;
      font-size: 14px;
    }
    .links a{
      padding: 8px 10px;
      border-radius: 12px;
    }
    .links a:hover{ background: rgba(255,255,255,.60); }
    .btn{
      display:inline-flex;
      align-items:center;
      justify-content:center;
      padding: 12px 16px;
      border-radius: 14px;
      font-weight: 700;
      border: 2px solid rgba(242,154,46,.45);
      background: rgba(255,255,255,.55);
      color: var(--blue);
      transition: transform .14s ease, background .14s ease;
      white-space: nowrap;
    }
    .btn:hover{ transform: translateY(-1px); background: rgba(255,255,255,.80); }
    .btn.primary{
      background: var(--orange);
      border-color: var(--orange);
      color: #fff;
      box-shadow: 0 16px 35px rgba(242,154,46,.25);
    }
    .btn.primary:hover{ background: #f08f12; }

    @media (max-width: 900px){
      .links{ display:none; }
    }

    /* HERO — capa */
    .hero{
      padding: 42px 0 18px;
      position: relative;
      overflow: hidden;
    }
    .heroGrid{
      display:grid;
      grid-template-columns: 1.05fr .95fr;
      gap: 18px;
      align-items: center;
    }
    @media (max-width: 950px){
      .heroGrid{ grid-template-columns: 1fr; }
    }

    .heroLeft{
      padding: 12px 4px;
    }
    .estaca{
      font-family: "Caveat", cursive;
      font-size: 28px;
      color: var(--orange);
      letter-spacing: .2px;
      margin-bottom: 10px;
    }
    h1{
      margin: 0;
      color: var(--blue);
      font-size: clamp(34px, 4.6vw, 54px);
      line-height: 1.0;
      letter-spacing: -.4px;
    }
    .year{
      margin-top: 8px;
      font-size: clamp(34px, 4.6vw, 54px);
      color: var(--blue);
      font-weight: 700;
    }
    .heroMeta{
      margin-top: 18px;
      display:flex;
      flex-wrap: wrap;
      gap: 12px;
      align-items:center;
    }
    .date{
      font-family: "Caveat", cursive;
      font-size: 26px;
      color: var(--orange);
    }
    .theme{
      display:inline-flex;
      align-items:center;
      gap: 10px;
      padding: 10px 12px;
      border-radius: 16px;
      background: rgba(255,255,255,.60);
      border: 1px solid rgba(11,95,122,.20);
      box-shadow: 0 10px 20px rgba(0,0,0,.08);
      color: var(--blue);
      font-weight: 700;
    }
    .theme small{
      display:block;
      font-weight: 600;
      opacity: .85;
    }

    .heroRight{
      display:flex;
      justify-content:center;
      align-items:center;
    }
    .heroIllus{
      width: min(520px, 100%);
      height: auto;
      border-radius: 22px;
      box-shadow: var(--shadow);
      background: rgba(255,255,255,.55);
      padding: 12px;
    }
    .heroIllus img{
      width: 100%;
      height: auto;
      display:block;
      border-radius: 16px;
    }

    /* Seções (cada dia) */
    section{
      padding: 28px 0;
    }
    .dayWrap{
      display:grid;
      grid-template-columns: 1.15fr .85fr;
      gap: 18px;
      align-items: start;
    }
    @media (max-width: 980px){
      .dayWrap{ grid-template-columns: 1fr; }
    }

    .dayText{
      padding: 10px 4px;
    }
    .dayTitle{
      margin: 0 0 10px;
      color: var(--blue);
      font-size: 26px;
      letter-spacing: -.2px;
    }
    .dayTitle .d{
      color: var(--blue2);
      font-weight: 600;
      font-size: 18px;
      margin-left: 6px;
      opacity: .9;
    }

    .list{
      margin: 0;
      padding-left: 18px;
      color: var(--blue2);
      font-weight: 600;
      font-size: 16px;
    }
    .list li{ margin: 10px 0; }
    .list b{ color: var(--blue); }
    .list ul{
      margin-top: 8px;
      padding-left: 18px;
      font-weight: 600;
      opacity: .95;
    }
    .list ul li{
      margin: 6px 0;
      font-size: 15px;
      opacity: .95;
    }

    /* Colagens (lado direito) */
    .collage{
      position: relative;
      min-height: 360px;
      margin-top: 6px;
    }

    /* Círculos (sábado/segunda) */
    .circle{
      position: absolute;
      border-radius: 999px;
      border: 10px solid rgba(255,255,255,.92);
      box-shadow: var(--shadow2);
      object-fit: cover;
      background: #fff;
    }

    /* Polaroids (domingo/terça) */
    .polaroid{
      position:absolute;
      width: 240px;
      background: rgba(255,255,255,.96);
      padding: 12px 12px 28px;
      border-radius: 14px;
      box-shadow: var(--shadow2);
      transform-origin: center;
      border: 1px solid rgba(0,0,0,.06);
    }
    .polaroid img{
      width: 100%;
      height: 175px;
      object-fit: cover;
      border-radius: 10px;
      display:block;
      background: #fff;
    }

    /* Sábado: 3 círculos */
    .sabado .c1{ width: 250px; height: 250px; left: 16px; top: 10px; transform: rotate(-4deg); }
    .sabado .c2{ width: 210px; height: 210px; right: 10px; top: 56px; transform: rotate(6deg); }
    .sabado .c3{ width: 260px; height: 260px; left: 92px; bottom: 10px; transform: rotate(4deg); }

    /* Domingo: polaroids */
    .domingo .p1{ left: 10px; top: 14px; transform: rotate(-6deg); }
    .domingo .p2{ right: 8px; top: 34px; transform: rotate(7deg); }
    .domingo .p3{ left: 72px; bottom: 12px; transform: rotate(3deg); }

    /* Segunda: círculos + árvore */
    .segunda .c1{ width: 250px; height: 250px; left: 16px; top: 10px; transform: rotate(-3deg); }
    .segunda .c2{ width: 215px; height: 215px; right: 10px; top: 62px; transform: rotate(5deg); }
    .segunda .c3{ width: 260px; height: 260px; left: 88px; bottom: 10px; transform: rotate(3deg); }
    .tree{
      position:absolute;
      right: 0;
      bottom: -8px;
      width: 140px;
      height: auto;
      opacity: .95;
      filter: drop-shadow(0 12px 18px rgba(0,0,0,.12));
    }

    /* Terça: polaroids + círculo */
    .terca .p1{ left: 10px; top: 16px; transform: rotate(-7deg); }
    .terca .p2{ right: 8px; top: 36px; transform: rotate(8deg); }
    .terca .p3{ left: 78px; bottom: 14px; transform: rotate(3deg); }
    .terca .c4{
      width: 140px; height: 140px;
      left: 6px; bottom: 4px;
      transform: rotate(-8deg);
      border-width: 8px;
    }

    /* CTA */
    .cta{
      margin-top: 8px;
      background: rgba(255,255,255,.60);
      border: 1px solid rgba(11,95,122,.20);
      border-radius: 22px;
      box-shadow: 0 16px 34px rgba(0,0,0,.10);
      padding: 18px;
      display:flex;
      justify-content: space-between;
      align-items:center;
      gap: 14px;
      flex-wrap: wrap;
    }
    .cta h3{
      margin:0 0 6px;
      color: var(--blue);
      font-size: 18px;
    }
    .cta p{
      margin:0;
      color: var(--blue2);
      opacity: .9;
      font-weight: 600;
      max-width: 72ch;
    }

    footer{
      padding: 22px 0 46px;
      border-top: 1px solid var(--line);
      color: var(--blue2);
      opacity: .9;
      font-weight: 600;
      font-size: 13px;
    }
  </style>
</head>

<body>
  <header>
    <div class="container nav">
      <div class="brand">
        <span class="badgeDot" aria-hidden="true"></span>
        <span>Estaca Mossoró</span>
      </div>

      <nav class="links" aria-label="Navegação">
        <a href="#programacao">Programação</a>
        <a href="#tema">Tema</a>
        <a href="#contato">Contato</a>
      </nav>

      <!-- Ajuste para seu link real (formulário / WhatsApp / etc.) -->
      <a class="btn primary" href="#contato">Informações</a>
    </div>
  </header>

  <main>
    <!-- HERO (capa) -->
    <section class="hero" id="tema">
      <div class="container heroGrid">
        <div class="heroLeft">
          <div class="estaca">Estaca Mossoró</div>

          <h1>Conferência<br/>dos jovens</h1>
          <div class="year">2026</div>

          <div class="heroMeta">
            <div class="date">14 à 17 de Fevereiro</div>
            <div class="theme">
              <div>
                Anda Comigo
                <small>(Moisés 6:36)</small>
              </div>
            </div>
          </div>
        </div>

        <div class="heroRight">
          <div class="heroIllus" aria-label="Ilustração da conferência">
            <!-- Coloque aqui a ilustração da capa -->
            <img src="assets/cover-illustration.png" alt="Ilustração da Conferência dos Jovens 2026" />
          </div>
        </div>
      </div>
    </section>

    <!-- PROGRAMAÇÃO -->
    <section id="programacao">
      <div class="container">
        <!-- SÁBADO -->
        <div class="dayWrap sabado">
          <div class="dayText">
            <h2 class="dayTitle">Sábado <span class="d">— 1º dia — 14/02/2026</span></h2>
            <ul class="list">
              <li>
                <b>08:00–09:00</b> Chegada
                <ul>
                  <li>Recepção dos jovens</li>
                  <li>Ficha de autorização, regras e orientações</li>
                  <li>Acomodação</li>
                </ul>
              </li>
              <li><b>11:00</b> Encerramento da recepção</li>
              <li><b>12:00–13:30</b> Almoço</li>
              <li>
                <b>14:00–17:00</b> Integração / divisão dos grupos
                <ul>
                  <li>Escolha do nome e bandeira</li>
                  <li>Jogos</li>
                  <li>Piscina</li>
                </ul>
              </li>
              <li><b>18:00–20:00</b> Jantar</li>
              <li><b>20:00–21:30</b> Atividades OR / OM</li>
            </ul>
          </div>

          <div class="collage" aria-label="Fotos do sábado">
            <img class="circle c1" src="assets/sabado-1.jpg" alt="Atividade em grupo" />
            <img class="circle c2" src="assets/sabado-2.jpg" alt="Jovens reunidos" />
            <img class="circle c3" src="assets/sabado-3.jpg" alt="Atividade ao ar livre" />
          </div>
        </div>

        <!-- DOMINGO -->
        <div class="dayWrap domingo" style="margin-top: 22px;">
          <div class="dayText">
            <h2 class="dayTitle">Domingo <span class="d">— 2º dia — 15/02/2026</span></h2>
            <ul class="list">
              <li><b>06:00–07:00</b> Despertar / estudo das escrituras</li>
              <li><b>07:00–08:00</b> Desjejum</li>
              <li><b>09:00–11:00</b> Sacramental</li>
              <li><b>12:00–14:00</b> Almoço</li>
              <li>
                <b>14:00–15:30</b> Cara a cara — Namoro e Castidade
                <ul>
                  <li>Pres. Gilvan e Zulienia</li>
                  <li>Pres. Maicon e Luana</li>
                  <li>Pres. Walber e Leidilane</li>
                </ul>
              </li>
              <li><b>16:00–17:00</b> Devocional com Patriarca Chicon e Irmã Emilce Chicon</li>
              <li><b>18:30–19:30</b> Jantar</li>
              <li><b>20:00–21:30</b> Atividade “árvore da vida”</li>
            </ul>
          </div>

          <div class="collage" aria-label="Fotos do domingo">
            <figure class="polaroid p1">
              <img src="assets/domingo-1.jpg" alt="Momento da sacramental" />
            </figure>
            <figure class="polaroid p2">
              <img src="assets/domingo-2.jpg" alt="Imagem inspiradora" />
            </figure>
            <figure class="polaroid p3">
              <img src="assets/domingo-3.jpg" alt="Imagem inspiradora" />
            </figure>
          </div>
        </div>

        <!-- SEGUNDA -->
        <div class="dayWrap segunda" style="margin-top: 22px;">
          <div class="dayText">
            <h2 class="dayTitle">Segunda-feira <span class="d">— 3º dia — 16/02/2026</span></h2>
            <ul class="list">
              <li><b>06:00–07:00</b> Despertar / estudo das escrituras</li>
              <li><b>07:30–08:00</b> Desjejum</li>
              <li>
                <b>09:00–12:00</b> Atividades em grupos
                <ul>
                  <li><b>09:00–10:30</b> Piscina Moças / Esporte Rapazes (bolas)</li>
                  <li><b>10:30–12:00</b> Piscina Rapazes / Esportes Moças (bolas)</li>
                </ul>
              </li>
              <li><b>12:00–14:00</b> Almoço</li>
              <li><b>14:30–16:30</b> Aulão do Seminário</li>
              <li><b>18:00</b> Baile — Tema: Filmes, Séries e Livros</li>
            </ul>
          </div>

          <div class="collage" aria-label="Fotos da segunda-feira">
            <img class="circle c1" src="assets/segunda-1.jpg" alt="Atividade recreativa" />
            <img class="circle c2" src="assets/segunda-2.jpg" alt="Atividade em grupo" />
            <img class="circle c3" src="assets/segunda-3.jpg" alt="Momento de integração" />

            <!-- Ícone da árvore (igual ao PDF) -->
            <img class="tree" src="assets/tree.png" alt="" aria-hidden="true" />
          </div>
        </div>

        <!-- TERÇA -->
        <div class="dayWrap terca" style="margin-top: 22px;">
          <div class="dayText">
            <h2 class="dayTitle">Terça-feira <span class="d">— 4º dia — 17/02/2026</span></h2>
            <ul class="list">
              <li><b>06:00–07:00</b> Despertar / estudo das escrituras</li>
              <li><b>07:30–08:00</b> Desjejum</li>
              <li><b>09:00–11:00</b> Gincanas</li>
              <li><b>12:00–14:00</b> Almoço</li>
              <li><b>14:00–15:00</b> Organização do local, malas etc.</li>
              <li><b>15:00–16:00</b> Reunião de testemunho</li>
              <li><b>16:00</b> Encerramento / saída do local</li>
            </ul>
          </div>

          <div class="collage" aria-label="Fotos da terça-feira">
            <figure class="polaroid p1">
              <img src="assets/terca-1.jpg" alt="Jovens em atividade" />
            </figure>
            <figure class="polaroid p2">
              <img src="assets/terca-2.jpg" alt="Jovens reunidos" />
            </figure>
            <figure class="polaroid p3">
              <img src="assets/terca-3.jpg" alt="Encerramento e integração" />
            </figure>

            <!-- Detalhe circular extra, como no layout do PDF -->
            <img class="circle c4" src="assets/terca-1.jpg" alt="" aria-hidden="true" />
          </div>
        </div>

        <!-- CTA / CONTATO -->
        <div class="cta" id="contato" style="margin-top: 26px;">
          <div>
            <h3>Informações e orientação</h3>
            <p>
              Para inscrição, confirmação de presença e orientações (autorização, regras e logística),
              utilize o canal oficial da organização da Estaca.
            </p>
          </div>
          <div style="display:flex; gap: 12px; flex-wrap:wrap;">
            <!-- Substitua pelos links reais -->
            <a class="btn primary" href="#" onclick="alert('Substitua pelo link do formulário/WhatsApp.'); return false;">Abrir formulário</a>
            <a class="btn" href="#" onclick="alert('Substitua pelo contato oficial.'); return false;">Falar com a organização</a>
          </div>
        </div>
      </div>
    </section>

    <footer>
      <div class="container" style="display:flex; justify-content:space-between; gap: 14px; flex-wrap:wrap;">
        <div>
          <b>Conferência dos Jovens 2026 — Estaca Mossoró</b><br/>
          Tema: “Anda Comigo” (Moisés 6:36) • 14 à 17 de fevereiro
        </div>
        <div style="text-align:right;">
          Ajuste links e contatos conforme a organização.
        </div>
      </div>
    </footer>
  </main>
</body>
</html>
