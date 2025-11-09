<!doctype html>
<html lang="pt">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>RiquezaFutura VIP</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <header class="header">
    <div class="brand">RiquezaFutura VIP</div>
    <a class="tg" href="https://t.me/fortunariq" target="_blank">@fortunariq</a>
  </header>

  <nav class="nav">
    <button onclick="show('home')">Home</button>
    <button onclick="show('register')">Registrar</button>
    <button onclick="show('login')">Login</button>
    <button onclick="show('panel')">Painel</button>
  </nav>

  <main id="app">
    <section id="home" class="page">
      <h2>Bem-vindo ao RiquezaFutura VIP</h2>
      <p>Invista e compre produtos VIP. Depósito mínimo: <strong>100 MZN</strong>. ID de transação obrigatório para confirmação.</p>
      <p>Atendimento: <a href="https://t.me/fortunariq" target="_blank">@fortunariq</a></p>
    </section>

    <section id="register" class="page hidden">
      <h3>Registrar</h3>
      <input id="rname" placeholder="Nome completo">
      <input id="rphone" placeholder="Telefone (ex: 848... )">
      <input id="rpass" type="password" placeholder="Senha">
      <button onclick="register()">Registrar</button>
    </section>

    <section id="login" class="page hidden">
      <h3>Login</h3>
      <input id="lphone" placeholder="Telefone">
      <input id="lpass" type="password" placeholder="Senha">
      <button onclick="login()">Login</button>
    </section>

    <section id="panel" class="page hidden">
      <h3>Painel</h3>
      <div id="userinfo" class="card"></div>

      <div class="card">
        <h4>Depósito</h4>
        <p>M-Pesa: <strong>848519239</strong> – Locatia Avelino</p>
        <p>e-Mola: <strong>862491110</strong> – Locatia Avelino</p>
        <input id="depAmount" placeholder="Valor (mín 100 MZN)">
        <input id="depTx" placeholder="ID da transação (ex: #12345)">
        <button onclick="deposit()">Enviar Depósito (Pendente)</button>
      </div>

      <div class="card">
        <h4>Levantamento</h4>
        <input id="wdAmount" placeholder="Valor (100 a 25000)">
        <input id="wdTx" placeholder="ID da conta para receber (opcional)">
        <button onclick="withdraw()">Solicitar Levantamento (Pendente)</button>
      </div>

      <div class="card">
        <h4>Loja VIP</h4>
        <div id="products" class="products-grid"></div>
      </div>

      <div class="card">
        <button onclick="logout()" class="danger">Sair</button>
      </div>
    </section>

    <section id="admin" class="page hidden">
      <h3>Painel Admin (apenas para admin)</h3>
      <p>Usuário Admin / Senha: 197200</p>
      <input id="adminPass" type="password" placeholder="Senha admin">
      <button onclick="loginAdmin()">Entrar Admin</button>

      <div id="adminPanel" class="hidden">
        <h4>Adicionar Produto</h4>
        <input id="pName" placeholder="Nome do produto">
        <input id="pPrice" placeholder="Preço (MZN)">
        <input id="pImg" placeholder="URL da imagem">
        <button onclick="addProduct()">Adicionar</button>

        <h4>Produtos</h4>
        <div id="adminProducts"></div>

        <h4>Depósitos Pendentes</h4>
        <div id="pendingDeposits"></div>

        <h4>Levantamentos Pendentes</h4>
        <div id="pendingWithdrawals"></div>
      </div>
    </section>
  </main>

  <footer class="footer">
    <small>© RiquezaFutura VIP</small>
  </footer>

  <script src="app.js"></script>
</body>
</html>
