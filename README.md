# Pubg-Mobile-tourment
<!DOCTYPE html><html lang="uz">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>PUBG MOBILE TOURMENT UZBEKISTAN</title>
  <style>
    body{font-family:Arial,sans-serif;margin:0;background:#0f172a;color:#fff}
    header{background:#111827;padding:15px;text-align:center;font-size:22px;font-weight:bold}
    nav{display:flex;justify-content:center;gap:10px;background:#1f2937;padding:10px}
    nav button{padding:8px 12px;border:none;cursor:pointer;border-radius:6px}
    section{display:none;padding:20px}
    .active{display:block}
    .card{background:#1e293b;padding:15px;margin:10px 0;border-radius:10px}
    input,button{padding:10px;margin:5px;width:100%;border-radius:6px;border:none}
    button{background:#2563eb;color:white;cursor:pointer}
    button:hover{background:#1d4ed8}
    .admin-box{max-width:400px;margin:auto}
  </style>
</head>
<body><header>PUBG MOBILE TOURMENT UZBEKISTAN</header><nav>
  <button onclick="show('home')">Bosh sahifa</button>
  <button onclick="show('tournaments')">Turnirlar</button>
  <button onclick="show('register')">Ro'yxatdan o'tish</button>
  <button onclick="show('admin')">Admin</button>
</nav><section id="home" class="active">
  <h2>Xush kelibsiz!</h2>
  <p>Bu PUBG MOBILE turnir sayti.</p>
</section><section id="tournaments">
  <h2>Turnirlar</h2>
  <div id="list"></div>
</section><section id="register">
  <h2>Ro'yxatdan o'tish</h2>
  <input id="name" placeholder="Ismingiz" />
  <input id="id" placeholder="PUBG ID" />
  <button onclick="register()">Yuborish</button>
  <p id="msg"></p>
</section><section id="admin">
  <div class="admin-box">
    <h2>Admin Panel</h2>
    <input type="password" id="pass" placeholder="Parol" />
    <button onclick="login()">Kirish</button>
    <div id="panel" style="display:none">
      <h3>Yangi turnir qo'shish</h3>
      <input id="tname" placeholder="Turnir nomi" />
      <input id="tdate" placeholder="Sana" />
      <button onclick="addTournament()">Qo'shish</button>
      <div id="adminList"></div>
    </div>
  </div>
</section><script>
let tournaments = [];

function show(id){
  document.querySelectorAll('section').forEach(s=>s.classList.remove('active'));
  document.getElementById(id).classList.add('active');
}

function render(){
  let list = document.getElementById('list');
  list.innerHTML = '';
  tournaments.forEach((t,i)=>{
    list.innerHTML += `<div class='card'><h3>${t.name}</h3><p>${t.date}</p></div>`;
  });
}

function register(){
  document.getElementById('msg').innerText = "Ro'yxatdan o'tildi!";
}

function login(){
  let p = document.getElementById('pass').value;
  if(p === "1769"){
    document.getElementById('panel').style.display='block';
    alert("Admin kirdingiz");
  } else {
    alert("Parol noto'g'ri");
  }
}

function addTournament(){
  let n = document.getElementById('tname').value;
  let d = document.getElementById('tdate').value;
  tournaments.push({name:n,date:d});
  render();
  renderAdmin();
}

function renderAdmin(){
  let a = document.getElementById('adminList');
  a.innerHTML = tournaments.map(t=>`<div class='card'>${t.name} - ${t.date}</div>`).join('');
}

render();
</script></body>
</html><!DOCTYPE html><html lang="uz">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>PUBG MOBILE TOURMENT UZBEKISTAN</title>
  <style>
    body{font-family:Arial,sans-serif;margin:0;background:#0f172a;color:#fff}
    header{background:#111827;padding:15px;text-align:center;font-size:22px;font-weight:bold}
    nav{display:flex;justify-content:center;gap:10px;background:#1f2937;padding:10px}
    nav button{padding:8px 12px;border:none;cursor:pointer;border-radius:6px}
    section{display:none;padding:20px}
    .active{display:block}
    .card{background:#1e293b;padding:15px;margin:10px 0;border-radius:10px}
    input,button{padding:10px;margin:5px;width:100%;border-radius:6px;border:none}
    button{background:#2563eb;color:white;cursor:pointer}
    button:hover{background:#1d4ed8}
    .admin-box{max-width:400px;margin:auto}
  </style>
</head>
<body><header>PUBG MOBILE TOURMENT UZBEKISTAN</header><nav>
  <button onclick="show('home')">Bosh sahifa</button>
  <button onclick="show('tournaments')">Turnirlar</button>
  <button onclick="show('register')">Ro'yxatdan o'tish</button>
  <button onclick="show('admin')">Admin</button>
</nav><section id="home" class="active">
  <h2>Xush kelibsiz!</h2>
  <p>Bu PUBG MOBILE turnir sayti.</p>
</section><section id="tournaments">
  <h2>Turnirlar</h2>
  <div id="list"></div>
</section><section id="register">
  <h2>Ro'yxatdan o'tish</h2>
  <input id="name" placeholder="Ismingiz" />
  <input id="id" placeholder="PUBG ID" />
  <button onclick="register()">Yuborish</button>
  <p id="msg"></p>
</section><section id="admin">
  <div class="admin-box">
    <h2>Admin Panel</h2>
    <input type="password" id="pass" placeholder="Parol" />
    <button onclick="login()">Kirish</button>
    <div id="panel" style="display:none">
      <h3>Yangi turnir qo'shish</h3>
      <input id="tname" placeholder="Turnir nomi" />
      <input id="tdate" placeholder="Sana" />
      <button onclick="addTournament()">Qo'shish</button>
      <div id="adminList"></div>
    </div>
  </div>
</section><script>
let tournaments = [];

function show(id){
  document.querySelectorAll('section').forEach(s=>s.classList.remove('active'));
  document.getElementById(id).classList.add('active');
}

function render(){
  let list = document.getElementById('list');
  list.innerHTML = '';
  tournaments.forEach((t,i)=>{
    list.innerHTML += `<div class='card'><h3>${t.name}</h3><p>${t.date}</p></div>`;
  });
}

function register(){
  document.getElementById('msg').innerText = "Ro'yxatdan o'tildi!";
}

function login(){
  let p = document.getElementById('pass').value;
  if(p === "1769"){
    document.getElementById('panel').style.display='block';
    alert("Admin kirdingiz");
  } else {
    alert("Parol noto'g'ri");
  }
}

function addTournament(){
  let n = document.getElementById('tname').value;
  let d = document.getElementById('tdate').value;
  tournaments.push({name:n,date:d});
  render();
  renderAdmin();
}

function renderAdmin(){
  let a = document.getElementById('adminList');
  a.innerHTML = tournaments.map(t=>`<div class='card'>${t.name} - ${t.date}</div>`).join('');
}

render();
</script></body>
</html>
<!DOCTYPE html>
<html lang="uz">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>PUBG MOBILE TOURNAMENT</title>

<style>
body{
  margin:0;
  font-family:Arial;
  background:#050505;
  color:white;
}

/* HERO */
.hero{
  height:100vh;
  background:url("https://images.unsplash.com/photo-1542751371-adc38448a05e") center/cover;
  position:relative;
  display:flex;
  justify-content:center;
  align-items:center;
  text-align:center;
}

.hero::after{
  content:"";
  position:absolute;
  top:0; left:0;
  width:100%; height:100%;
  background:rgba(0,0,0,0.7);
}

.hero-content{
  position:relative;
  z-index:1;
}

.hero h1{
  font-size:45px;
  color:#ffcc00;
  text-shadow:0 0 20px black;
}

.hero p{
  font-size:18px;
  color:#ddd;
}

.btn{
  margin-top:20px;
  padding:15px 30px;
  border:none;
  background:#ffcc00;
  font-weight:bold;
  cursor:pointer;
  border-radius:8px;
}

.btn:hover{
  background:#ff9900;
}

/* SECTIONS */
.section{
  padding:50px 20px;
  text-align:center;
}

.card{
  background:#111;
  margin:20px auto;
  width:85%;
  max-width:700px;
  padding:20px;
  border-radius:12px;
  box-shadow:0 0 20px #ffcc00;
}

/* GALLERY */
.gallery{
  display:flex;
  flex-wrap:wrap;
  justify-content:center;
  gap:10px;
}

.gallery img{
  width:220px;
  height:140px;
  object-fit:cover;
  border-radius:10px;
  border:2px solid #ffcc00;
}

/* FOOTER */
footer{
  padding:20px;
  background:black;
  text-align:center;
  color:#aaa;
}
</style>

</head>

<body>

<div class="hero">
  <div class="hero-content">
    <h1>🔥 PUBG MOBILE TOURNAMENT 🔥</h1>
    <p>UZBEKISTAN OFFICIAL ONLINE TURNIR</p>
    <button class="btn">RO‘YXATDAN O‘TISH</button>
  </div>
</div>

<div class="section">

  <div class="card">
    <h2>🎮 O‘yin Rasmlari</h2>
    <div class="gallery">
      <img src="https://images.unsplash.com/photo-1612287230202-1ff1d8b2f9b7">
      <img src="https://images.unsplash.com/photo-1606813902916-0a6c3c2b0a7a">
      <img src="https://images.unsplash.com/photo-1593305841991-05c297ba4575">
    </div>
  </div>

  <div class="card">
    <h2>💰 Prize Pool</h2>
    <p>🥇 1-O‘rin: $200</p>
    <p>🥈 2-O‘rin: $100</p>
    <p>🥉 3-O‘rin: $50</p>
  </div>

  <div class="card">
    <h2>📅 Turnir vaqti</h2>
    <p>Har yakshanba 20:00</p>
  </div>

</div>

<footer>
© PUBG MOBILE TOURNAMENT UZBEKISTAN
</footer>

</body>
</html>
