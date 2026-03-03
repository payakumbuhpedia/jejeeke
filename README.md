<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Kenzodistaananta | Ultra Premium Cyber</title>

<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">

<style>

:root{
--bg:#0b0f19;
--card:rgba(255,255,255,0.05);
--accent:#4da3ff;
--accent2:#7c4dff;
--text:#ffffff;
--muted:#9aa4b2;
--border:rgba(255,255,255,0.08);
}

*{margin:0;padding:0;box-sizing:border-box;}

body{
font-family:'Inter',sans-serif;
background:linear-gradient(-45deg,#0b0f19,#111827,#0f172a,#0b0f19);
background-size:400% 400%;
animation:bgMove 15s ease infinite;
color:var(--text);
scroll-behavior:smooth;
overflow-x:hidden;
}

@keyframes bgMove{
0%{background-position:0% 50%;}
50%{background-position:100% 50%;}
100%{background-position:0% 50%;}
}

/* NAVBAR */

header{
position:fixed;
top:0;
width:100%;
background:rgba(11,15,25,0.7);
backdrop-filter:blur(10px);
border-bottom:1px solid var(--border);
z-index:999;
}

.nav{
display:flex;
justify-content:space-between;
align-items:center;
padding:15px 20px;
max-width:1200px;
margin:auto;
}

.logo{
font-weight:700;
font-size:1rem;
letter-spacing:1px;
}

.logo span{
color:var(--accent);
}

.menu{
display:flex;
gap:25px;
}

.menu a{
color:var(--muted);
font-size:.9rem;
transition:.3s;
}

.menu a:hover{
color:var(--accent);
}

.hamburger{
display:none;
font-size:1.4rem;
cursor:pointer;
}

@media(max-width:768px){
.menu{
position:absolute;
top:60px;
left:0;
width:100%;
background:#111827;
flex-direction:column;
text-align:center;
padding:20px 0;
display:none;
}
.menu.active{display:flex;}
.hamburger{display:block;}
}

/* HERO */

.hero{
padding-top:120px;
text-align:center;
padding-bottom:120px;
max-width:800px;
margin:auto;
}

.hero h1{
font-size:2.7rem;
}

.hero span{
color:var(--accent);
}

.typing{
margin-top:15px;
color:var(--muted);
height:24px;
}

.btn{
display:inline-block;
margin-top:30px;
padding:12px 25px;
border-radius:8px;
background:linear-gradient(90deg,var(--accent),var(--accent2));
color:white;
font-size:.9rem;
transition:.3s;
}

.btn:hover{
opacity:0.8;
}

/* SECTIONS */

.section{
padding:80px 20px;
max-width:1200px;
margin:auto;
}

.section h2{
margin-bottom:40px;
font-size:1.5rem;
border-left:4px solid var(--accent);
padding-left:10px;
}

/* BLOG GRID */

.grid{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(280px,1fr));
gap:30px;
}

.card{
background:var(--card);
padding:25px;
border-radius:15px;
backdrop-filter:blur(10px);
border:1px solid var(--border);
transition:.4s;
position:relative;
overflow:hidden;
}

.card::before{
content:'';
position:absolute;
top:0;
left:-100%;
width:100%;
height:3px;
background:linear-gradient(90deg,var(--accent),var(--accent2));
transition:.4s;
}

.card:hover::before{
left:0;
}

.card:hover{
transform:translateY(-10px);
box-shadow:0 15px 40px rgba(0,0,0,0.4);
}

.card h3{
margin-bottom:10px;
color:var(--accent);
}

.card p{
font-size:.9rem;
color:var(--muted);
}

.meta{
font-size:.8rem;
margin-top:15px;
color:#6b7280;
}

/* FOOTER */

footer{
padding:40px 20px;
text-align:center;
font-size:.8rem;
color:var(--muted);
border-top:1px solid var(--border);
}

/* RESPONSIVE */

@media(max-width:480px){
.hero h1{font-size:1.8rem;}
}

</style>
</head>

<body>

<header>
<div class="nav">
<div class="logo">KENZODISTA<span>ANANTA</span></div>

<div class="hamburger" onclick="toggleMenu()">
<i class="fas fa-bars"></i>
</div>

<div class="menu" id="menu">
<a href="#blog">Blog</a>
<a href="#projects">Projects</a>
<a href="#contact">Contact</a>
</div>
</div>
</header>

<section class="hero">
<h1>Cyber Security & <span>Ethical Research</span></h1>
<div class="typing" id="typing"></div>
<a href="#blog" class="btn">Lihat Artikel</a>
</section>

<section id="blog" class="section">
<h2>Artikel & Research</h2>
<div class="grid">

<div class="card">
<h3>Advanced Web Vulnerability</h3>
<p>Analisis kerentanan aplikasi web modern berdasarkan standar OWASP Top 10.</p>
<div class="meta">12 Juni 2026 • 8 min read</div>
</div>

<div class="card">
<h3>Red Team Simulation</h3>
<p>Simulasi pengujian penetrasi untuk meningkatkan defensive security.</p>
<div class="meta">5 Juni 2026 • 10 min read</div>
</div>

<div class="card">
<h3>Malware Static Analysis</h3>
<p>Metode analisis malware tanpa eksekusi langsung pada sistem target.</p>
<div class="meta">28 Mei 2026 • 7 min read</div>
</div>

</div>
</section>

<section id="contact" class="section">
<h2>Contact</h2>
<p style="color:var(--muted);">
Email: payakumbuhpediastoreid@gmail.com<br>
Instagram: @kenzodistaananta
</p>
</section>

<footer>
© 2026 Kenzodistaananta. Seluruh Hak Cipta Dilindungi.  
Unauthorized duplication or reproduction is prohibited.
</footer>

<script>

function toggleMenu(){
document.getElementById("menu").classList.toggle("active");
}

/* TYPING EFFECT */

const text = ["Ethical Hacking","Penetration Testing","Cyber Defense Specialist"];
let count = 0;
let index = 0;
let currentText = "";
let letter = "";

(function type(){
if(count === text.length){
count = 0;
}
currentText = text[count];
letter = currentText.slice(0, ++index);

document.getElementById("typing").textContent = letter;

if(letter.length === currentText.length){
count++;
index = 0;
setTimeout(type,1000);
}else{
setTimeout(type,80);
}
})();

</script>

</body>
</html>
