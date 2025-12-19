<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>BTS x ARMY Universe</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;800&display=swap" rel="stylesheet">

<style>
:root{
  --bg:#0b0011;
  --card:rgba(255,255,255,.06);
  --text:#f4eaff;
  --accent:#c084fc;
}
.light{
  --bg:#f6edff;
  --card:#ffffff;
  --text:#1b0026;
}

*{margin:0;padding:0;box-sizing:border-box;font-family:Poppins,sans-serif}
body{
  background:var(--bg);
  color:var(--text);
  transition:.4s;
  overflow-x:hidden;
  scroll-behavior:smooth;
}

/* NAV */
nav{
  position:fixed;top:0;width:100%;
  padding:14px 25px;
  display:flex;justify-content:space-between;
  background:rgba(0,0,0,.6);
  backdrop-filter:blur(10px);
  z-index:1000;
}
nav h1{color:var(--accent)}
nav a{color:var(--text);margin-left:15px;text-decoration:none}
.toggle{cursor:pointer}

/* HERO */
.hero{
  height:100vh;
  display:flex;align-items:center;justify-content:center;
  text-align:center;padding:20px;
}
.hero h2{
  font-size:clamp(2.5rem,5vw,4rem);
  animation:glow 2s infinite alternate;
}
@keyframes glow{
  from{text-shadow:0 0 10px var(--accent)}
  to{text-shadow:0 0 35px #f5d0ff}
}

/* SECTIONS */
section{padding:90px 8%; opacity:0; transform:translateY(30px); transition:all 0.6s ease;}
section.visible{opacity:1; transform:translateY(0);}
section h3{text-align:center;font-size:2.3rem;margin-bottom:40px;color:var(--accent)}

/* MEMBERS */
.members{
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(180px,1fr));
  gap:25px;
}
.card{
  background:var(--card);
  padding:25px;border-radius:18px;
  text-align:center;cursor:pointer;
  transition:.4s;
}
.card:hover{
  transform:translateY(-8px) scale(1.05);
  box-shadow:0 0 25px var(--accent);
}
.card img{
  width:100px;
  height:100px;
  border-radius:50%;
  margin-bottom:10px;
  object-fit:cover;
}
.card h4{
  margin-top:10px;
  color:var(--accent);
}

/* MODAL */
.modal{
  position:fixed;inset:0;
  display:none;align-items:center;justify-content:center;
  background:rgba(0,0,0,.8);
  z-index:2000;
}
.modal-box{
  background:var(--bg);
  padding:30px;border-radius:20px;
  max-width:400px;text-align:center;
}
.modal-box img{
  width:150px;border-radius:15px;margin-bottom:15px;
}
.close{margin-top:15px;cursor:pointer;color:var(--accent)}

/* GALLERY */
.gallery{
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(200px,1fr));
  gap:15px;
}
.gallery img{
  width:100%;border-radius:15px;
  transition:.4s;
}
.gallery img:hover{
  transform:scale(1.08);
  box-shadow:0 0 20px var(--accent);
}

/* ERAS */
.timeline{
  max-width:800px;margin:auto;
}
.era{
  background:var(--card);
  padding:20px;margin:20px 0;
  border-left:4px solid var(--accent);
  border-radius:10px;
}

/* LIGHTSTICK */
.orb{
  width:150px;height:150px;margin:auto;
  border-radius:50%;
  background:radial-gradient(circle,#fff,var(--accent));
  animation:pulse 1.8s infinite;
}
@keyframes pulse{
  0%{box-shadow:0 0 20px var(--accent)}
  50%{box-shadow:0 0 80px #f5d0ff}
  100%{box-shadow:0 0 20px var(--accent)}
}

/* VISUALIZER */
.bars{display:flex;justify-content:center;gap:6px;margin-top:30px}
.bar{
  width:10px;height:25px;
  background:var(--accent);
  animation:beat .6s infinite alternate;
}
.bar:nth-child(odd){animation-delay:.2s}
@keyframes beat{to{height:80px}}

/* FOOTER */
footer{text-align:center;padding:40px;opacity:.85}

/* STARS */
.star{
  position:fixed;width:3px;height:3px;
  background:white;border-radius:50%;
  animation:float 10s linear infinite;
}
@keyframes float{
  from{transform:translateY(110vh)}
  to{transform:translateY(-10vh)}
}
#musicIcon{font-size:50px;cursor:pointer;margin-top:20px;}
</style>
</head>

<body>

<nav>
<h1>BTS 💜 ARMY</h1>
<div>
<a href="#members">Members</a>
<a href="#gallery">Gallery</a>
<a href="#eras">Eras</a>
<a href="#army">ARMY</a>
<a href="#music">Music</a>
<span class="toggle" onclick="toggleTheme()">🌓</span>
</div>
</nav>

<div class="hero">
<div>
<h2>Welcome to the BTS Universe</h2>
<p>A fan-made space celebrating BTS & ARMY</p>
</div>
</div>

<section id="members">
<h3>The 7 Members</h3>
<div class="members">
<div class="card" onclick="openModal('RM','Leader · Lyricist · Thinker','https://via.placeholder.com/150?text=RM')">
  <img src="https://via.placeholder.com/150?text=RM" alt="RM">
  <h4>RM</h4>
</div>
<div class="card" onclick="openModal('Jin','Vocal · Worldwide Handsome','https://via.placeholder.com/150?text=Jin')">
  <img src="https://via.placeholder.com/150?text=Jin" alt="Jin">
  <h4>Jin</h4>
</div>
<div class="card" onclick="openModal('SUGA','Rapper · Producer','https://via.placeholder.com/150?text=SUGA')">
  <img src="https://via.placeholder.com/150?text=SUGA" alt="SUGA">
  <h4>SUGA</h4>
</div>
<div class="card" onclick="openModal('j-hope','Dance · Sunshine','https://via.placeholder.com/150?text=j-hope')">
  <img src="https://via.placeholder.com/150?text=j-hope" alt="j-hope">
  <h4>j-hope</h4>
</div>
<div class="card" onclick="openModal('Jimin','Grace · Performance','https://via.placeholder.com/150?text=Jimin')">
  <img src="https://via.placeholder.com/150?text=Jimin" alt="Jimin">
  <h4>Jimin</h4>
</div>
<div class="card" onclick="openModal('V','Artist · Soul','https://via.placeholder.com/150?text=V')">
  <img src="https://via.placeholder.com/150?text=V" alt="V">
  <h4>V</h4>
</div>
<div class="card" onclick="openModal('Jungkook','Golden Maknae','https://via.placeholder.com/150?text=Jungkook')">
  <img src="https://via.placeholder.com/150?text=Jungkook" alt="Jungkook">
  <h4>Jungkook</h4>
</div>
</div>
</section>

<section id="gallery">
<h3>Gallery</h3>
<div class="gallery">
<img src="https://via.placeholder.com/400x300?text=BTS">
<img src="https://via.placeholder.com/400x300?text=ARMY">
<img src="https://via.placeholder.com/400x300?text=Purple">
<img src="https://via.placeholder.com/400x300?text=Universe">
</div>
</section>

<section id="eras">
<h3>BTS Eras</h3>
<div class="timeline">
<div class="era"><strong>School Trilogy</strong> – Youth & dreams</div>
<div class="era"><strong>HYYH</strong> – Growth & uncertainty</div>
<div class="era"><strong>Wings</strong> – Temptation & self</div>
<div class="era"><strong>Love Yourself</strong> – Self-love</div>
<div class="era"><strong>Map of the Soul</strong> – Identity</div>
<div class="era"><strong>BE</strong> – Comfort & healing</div>
</div>
</section>

<section id="army" style="text-align:center">
<h3>ARMY Bomb</h3>
<div class="orb"></div>
<div class="bars">
<div class="bar"></div><div class="bar"></div><div class="bar"></div>
<div class="bar"></div><div class="bar"></div>
</div>
</section>

<section id="music" style="text-align:center">
<h3>BTS Vibes</h3>
<div id="musicIcon">⏸️</div>
<audio id="song" src="bts.mp3" autoplay></audio>
<div class="bars" id="visualizer">
<div class="bar"></div><div class="bar"></div><div class="bar"></div>
<div class="bar"></div><div class="bar"></div>
</div>
</section>

<footer>
💜 Fan-made BTS Website · Made with love by ARMY 💜
</footer>

<div class="modal" id="modal">
<div class="modal-box">
<h3 id="mTitle"></h3>
<p id="mText"></p>
<div class="close" onclick="closeModal()">Close</div>
</div>
</div>

<script>
const modal = document.getElementById("modal");
const mTitle = document.getElementById("mTitle");
const mText = document.getElementById("mText");

function openModal(name, text, img){
  modal.style.display="flex";
  mTitle.innerText=name;
  mText.innerHTML = `<img src="${img}" alt="${name}"><p>${text}</p>`;
}
function closeModal(){modal.style.display="none";}
function toggleTheme(){document.body.classList.toggle("light");}

// Stars
for(let i=0;i<70;i++){
  let s=document.createElement("div");
  s.className="star";
  s.style.left=Math.random()*100+"vw";
  s.style.animationDuration=6+Math.random()*8+"s";
  document.body.appendChild(s);
}

// Section reveal on scroll
const sections = document.querySelectorAll('section');
window.addEventListener('scroll', () => {
  sections.forEach(sec => {
    const top = sec.getBoundingClientRect().top;
    if(top < window.innerHeight - 100){
      sec.classList.add('visible');
    }
  });
});

// Fake visualizer animation
const bars = document.querySelectorAll('#visualizer .bar');
setInterval(()=>{
  bars.forEach(bar=>{
    bar.style.height = (20 + Math.random()*60) + 'px';
  });
}, 300);

// Music play/pause toggle
const musicIcon = document.getElementById("musicIcon");
const song = document.getElementById("song");

// Set icon to pause initially
musicIcon.textContent = "⏸️";

musicIcon.addEventListener("click", () => {
  if(song.paused){
    song.play();
    musicIcon.textContent = "⏸️";
  } else {
    song.pause();
    musicIcon.textContent = "🎵";
  }
});
</script>

</body>
</html>
