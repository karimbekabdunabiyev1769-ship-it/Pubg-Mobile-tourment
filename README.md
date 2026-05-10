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
