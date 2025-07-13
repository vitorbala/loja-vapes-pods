<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Vapes e Pods EmVaporáveis - Loja Completa</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #111;
      color: #fff;
      margin: 0; padding: 0;
    }
    header {
      background: #222;
      padding: 15px 20px;
      text-align: center;
      position: sticky;
      top: 0;
      z-index: 100;
      box-shadow: 0 2px 8px rgba(0,0,0,0.6);
    }
    header h1 {
      color: #00ffcc;
      margin: 0;
      font-size: 2.3em;
      letter-spacing: 3px;
      text-transform: uppercase;
    }
    /* Banner */
    .banner {
      background: linear-gradient(135deg, #00ffcc 0%, #006666 100%);
      height: 220px;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      color: #000;
      font-size: 2.6em;
      font-weight: 900;
      text-align: center;
      padding: 0 20px;
      user-select: none;
      box-shadow: inset 0 0 20px rgba(255,255,255,0.3);
    }
    .banner small {
      font-size: 1.2em;
      font-weight: 600;
      margin-top: 8px;
      color: #004d4d;
    }
    /* Container */
    .container {
      max-width: 1200px;
      margin: 0 auto;
      padding: 20px 15px;
    }
    /* Biografia */
    .biografia {
      background: #222;
      padding: 20px;
      border-radius: 10px;
      margin-bottom: 40px;
      line-height: 1.6;
      font-size: 1.1em;
      box-shadow: 0 0 12px rgba(0,255,204,0.3);
    }
    .biografia h2 {
      color: #00ffcc;
      margin-bottom: 15px;
      letter-spacing: 1.5px;
      text-transform: uppercase;
    }
    /* Produtos */
    .produtos-section {
      margin-bottom: 50px;
    }
    .produtos-section h2 {
      color: #00ffcc;
      margin-bottom: 20px;
      letter-spacing: 1.5px;
      text-transform: uppercase;
      text-align: center;
    }
    .produtos-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit,minmax(150px,1fr));
      gap: 15px;
    }
    .produto {
      background-color: #1c1c1c;
      border-radius: 10px;
      padding: 10px;
      text-align: center;
      box-shadow: 0 0 12px rgba(0,255,200,0.2);
      transition: transform 0.2s ease;
      cursor: default;
      user-select: none;
    }
    .produto:hover {
      transform: scale(1.05);
    }
    .produto img {
      max-width: 100%;
      height: 130px;
      object-fit: cover;
      border-radius: 8px;
      margin-bottom: 10px;
      user-select: none;
    }
    .produto h3 {
      font-size: 1em;
      margin: 8px 0 4px;
      min-height: 40px;
      color: #00ffcc;
      user-select: text;
    }
    .produto p {
      margin: 3px 0 8px;
      font-weight: 700;
      color: #00cc99;
      user-select: text;
    }
    .whatsapp-btn {
      display: inline-block;
      background-color: #25D366;
      color: white;
      padding: 8px 12px;
      border-radius: 8px;
      text-decoration: none;
      font-weight: 700;
      font-size: 0.9em;
      transition: background-color 0.3s ease;
      user-select: none;
    }
    .whatsapp-btn:hover {
      background-color: #1ebe57;
    }
    /* Depoimentos */
    .depoimentos {
      background-color: #222;
      padding: 25px 20px;
      border-radius: 10px;
      margin-bottom: 40px;
      box-shadow: 0 0 15px rgba(0,255,200,0.25);
      max-width: 900px;
      margin-left: auto;
      margin-right: auto;
    }
    .depoimentos h2 {
      text-align: center;
      color: #00ffcc;
      margin-bottom: 25px;
      letter-spacing: 1.8px;
      text-transform: uppercase;
    }
    .depoimento {
      background-color: #111;
      padding: 12px 15px;
      border-radius: 8px;
      margin-bottom: 12px;
      font-style: italic;
      position: relative;
      box-shadow: 0 0 10px rgba(0,255,200,0.2);
      user-select: text;
    }
    .depoimento::before {
      content: "“";
      font-size: 2.5em;
      color: #00ffcc;
      position: absolute;
      top: 7px;
      left: 12px;
      opacity: 0.25;
      font-family: serif;
    }
    .depoimento p {
      margin-left: 30px;
      margin-right: 15px;
    }
    .depoimento .cliente {
      text-align: right;
      font-weight: 700;
      margin-top: 10px;
      color: #25D366;
      user-select: text;
    }
    /* Botão ver mais depoimentos */
    #btnVerMais {
      display: block;
      margin: 10px auto 0 auto;
      background: #00ffcc;
      border: none;
      padding: 10px 25px;
      font-weight: 700;
      font-size: 1em;
      border-radius: 20px;
      color: #000;
      cursor: pointer;
      transition: background-color 0.3s ease;
      user-select: none;
    }
    #btnVerMais:hover {
      background: #00cc99;
    }
    /* Informações */
    .info {
      background-color: #1a1a1a;
      padding: 20px;
      border-radius: 10px;
      max-width: 900px;
      margin: 0 auto 40px auto;
      line-height: 1.6;
      font-size: 1em;
      user-select: text;
    }
    /* Rodapé */
    footer {
      background-color: #111;
      color: #888;
      text-align: center;
      padding: 15px;
      font-size: 0.9em;
      user-select: none;
    }
    /* Redes sociais */
    .redes {
      text-align: center;
      margin-top: 10px;
    }
    .redes a {
      color: #00ffcc;
      text-decoration: none;
      margin: 0 10px;
      font-weight: 700;
      user-select: none;
    }
    .redes a:hover {
      text-decoration: underline;
    }
    /* Responsivo */
    @media(max-width: 600px) {
      .banner {
        font-size: 1.5em;
        height: 180px;
        padding: 0 10px;
      }
      .produto img {
        height: 100px;
      }
      .produtos-grid {
        grid-template-columns: repeat(auto-fit,minmax(130px,1fr));
      }
    }
  </style>
</head>
<body>
  <header>
    <h1>Vapes e Pods EmVaporáveis</h1>
  </header>

  <div class="banner" role="banner" aria-label="Banner promocional da loja">
    <div>🔥 Chegou o melhor em Pods e Vapes!</div>
    <small>Entrega rápida e atendimento exclusivo via WhatsApp</small>
  </div>

  <main class="container" role="main">
    <section class="biografia" aria-label="Biografia da loja">
      <h2>Sobre a Vapes e Pods EmVaporáveis</h2>
      <p>Somos uma loja especializada em pods e vapes, oferecendo os melhores sabores, qualidade e atendimento personalizado. Com anos de experiência, garantimos produtos originais e entregas rápidas para sua total satisfação.</p>
      <p>Nosso compromisso é com a confiança, transparência e segurança em cada pedido. Atendimento direto via WhatsApp para tirar dúvidas e facilitar sua compra. Faça parte da nossa comunidade de clientes satisfeitos!</p>
    </section>

    <section class="produtos-section" aria-label="Lista de Pods">
      <h2>Pods Populares</h2>
      <div class="produtos-grid" id="podsList">
        <!-- Pods vão aqui via JavaScript -->
      </div>
    </section>

    <section class="produtos-section" aria-label="Lista de Vapes">
      <h2>Vapes Disponíveis</h2>
      <div class="produtos-grid" id="vapesList">
        <!-- Vapes vão aqui via JavaScript -->
      </div>
    </section>

    <section class="depoimentos" aria-label="Depoimentos dos clientes">
      <h2>O que nossos clientes dizem</h2>

      <div id="depoimentosContainer">
        <!-- 10 depoimentos iniciais -->
      </div>

      <button id="btnVerMais" aria-expanded="false" aria-controls="depoimentosExtras">Ver mais depoimentos</button>

      <div id="depoimentosExtras" style="display:none; margin-top:15px;" aria-hidden="true">
        <!-- 40 depoimentos extras -->
      </div>
    </section>

    <section class="info" aria-label="Informações sobre pagamento e entrega">
      <h2>Pagamento e Entrega</h2>
      <p>✅ Aceitamos Pix, transferência e cartão de crédito via link seguro.</p>
      <p>✅ Entregamos em toda Fortaleza com rapidez e segurança.</p>
      <p>✅ Para pedidos maiores, entre em contato via WhatsApp para condições especiais.</p>
    </section>
  </main>

  <footer>
    © 2025 - Vapes e Pods EmVaporáveis | WhatsApp: (85) 98129-9573
    <div class="redes">
      <a href="https://instagram.com/vapesepodsloja" target="_blank" rel="noopener">Instagram</a> | 
      <a href="https://wa.me/5585981299573" target="_blank" rel="noopener">WhatsApp</a>
    </div>
  </footer>

  <script>
    // Dados simulados para produtos e depoimentos

    const pods = [
      {nome:"Pod Uva Ice", preco:60, img:"https://images.unsplash.com/photo-1603213055300-bf9a038bc74e?auto=format&fit=crop&w=400&q=80"},
      {nome:"Pod Melancia", preco:60, img:"https://images.unsplash.com/photo-1590080877777-c3a2b98e8b58?auto=format&fit=crop&w=400&q=80"},
      {nome:"Pod Menta", preco:65, img:"https://images.unsplash.com/photo-1556905055-8f358a7a47b4?auto=format&fit=crop&w=400&q=80"},
      {nome:"Pod Morango", preco:65, img:"https://images.unsplash.com/photo-1542762936-4a8d2874b3f6?auto=format&fit=crop&w=400&q=80"},
      // Repita e varie até 50, vou gerar 50 com nomes + índice e repetir imagens
    ];

    const vapes = [
      {nome:"Vape Azul", preco:150, img:"https://images.unsplash.com/photo-1512499617640-c2f99942c17e?auto=format&fit=crop&w=400&q=80"},
      {nome:"Vape Vermelho", preco:160, img:"https://images.unsplash.com/photo-1549924231-f129b911e442?auto=format&fit=crop&w=400&q=80"},
      {nome:"Vape Preto", preco:170, img:"https://images.unsplash.com/photo-1517841905240-472988babdf9?auto=format&fit=crop&w=400&q=80"},
      {nome:"Vape Branco", preco:150, img:"https://images.unsplash.com/photo-1549887538-cf2a09de73c6?auto=format&fit=crop&w=400&q=80"},
      // Também repita até 50 com nomes + índice e imagens
    ];

    const depoimentos = [
      {texto:"Entrega rápida e atendimento excelente! Recomendo demais os pods da EmVaporáveis.", cliente:"Lucas M."},
      {texto:"Sabores incríveis e qualidade top! Sempre peço o pod de Uva Ice, meu favorito.", cliente:"Mariana S."},
      {texto:"Ótima experiência de compra, atendimento pelo WhatsApp muito prático e rápido.", cliente:"João P."},
      {texto:"Produtos originais e entrega muito rápida. Super satisfeito!", cliente:"Ana C."},
      {texto:"Gostei muito da variedade e do atendimento personalizado.", cliente:"Carlos F."},
      {texto:"Recomendo para todos que querem qualidade e preço justo.", cliente:"Fernanda L."},
      {texto:"Comprei e recebi rápido, tudo certo. Voltarei a comprar!", cliente:"Rafael S."},
      {texto:"Amei os sabores, especialmente o Melancia. Atendimento nota 10!", cliente:"Larissa M."},
      {texto:"Site fácil de usar e atendimento excelente no WhatsApp.", cliente:"Paulo G."},
      {texto:"Podem confiar, produtos de qualidade e entrega pontual.", cliente:"Juliana T."},
      // 40 depoimentos extras, repetindo base e mudando nomes
    ];

    // Para simular 50 pods e 50 vapes com variações
    function gerarProdutos(baseProdutos, quantidade){
      const list = [];
      for(let i=1; i<=quantidade; i++){
        const base = baseProdutos[(i-1) % baseProdutos.length];
        list.push({
          nome: base.nome + " " + i,
          preco: base.preco + (i % 3)*5,
          img: base.img
        });
      }
      return list;
    }

    const podsList = gerarProdutos(pods,50);
    const vapesList = gerarProdutos(vapes,50);

    // Renderizar produtos
    function renderProdutos(lista, containerId){
      const container = document.getElementById(containerId);
      lista.forEach(prod=>{
        const aHref = `https://wa.me/5585981299573?text=Olá!%20Tenho%20interesse%20no%20${encodeURIComponent(prod.nome)}`;
        const div = document.createElement("div");
        div.className = "produto";
        div.innerHTML = `
          <img src="${prod.img}" alt="${prod.nome}" />
          <h3>${prod.nome}</h3>
          <p>R$ ${prod.preco.toFixed(2).replace('.',',')}</p>
          <a class="whatsapp-btn" href="${aHref}" target="_blank" rel="noopener">Comprar no WhatsApp</a>
        `;
        container.appendChild(div);
      });
    }

    // Renderizar depoimentos (primeiros 10)
    function renderDepoimentosIniciais(){
      const container = document.getElementById("depoimentosContainer");
      for(let i=0; i<10; i++){
        const depo = depoimentos[i % depoimentos.length];
        const div = document.createElement("div");
        div.className = "depoimento";
        div.innerHTML = `<p>${depo.texto}</p><div class="cliente">— ${depo.cliente}</div>`;
        container.appendChild(div);
      }
    }

    // Renderizar depoimentos extras (40 restantes)
    function renderDepoimentosExtras(){
      const container = document.getElementById("depoimentosExtras");
      for(let i=10; i<50; i++){
        const depo = depoimentos[i % depoimentos.length];
        const div = document.createElement("div");
        div.className = "depoimento";
        div.innerHTML = `<p>${depo.texto}</p><div class="cliente">— ${depo.cliente}</div>`;
        container.appendChild(div);
      }
    }

    // Mostrar/esconder depoimentos extras no clique
    const btnVerMais = document.getElementById("btnVerMais");
    btnVerMais.addEventListener("click", ()=>{
      const extras = document.getElementById("depoimentosExtras");
      const expanded = btnVerMais.getAttribute("aria-expanded") === "true";
      if(expanded){
        extras.style.display = "none";
        btnVerMais.textContent = "Ver mais depoimentos";
        btnVerMais.setAttribute("aria-expanded","false");
        extras.setAttribute("aria-hidden","true");
      } else {
        extras.style.display = "block";
        btnVerMais.textContent = "Ver menos depoimentos";
        btnVerMais.setAttribute("aria-expanded","true");
        extras.setAttribute("aria-hidden","false");
      }
    });

    // Inicializar tudo
    renderProdutos(podsList,"podsList");
    renderProdutos(vapesList,"vapesList");
    renderDepoimentosIniciais();
    renderDepoimentosExtras();

  </script>
</body>
</html>
