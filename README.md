<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Beginner-Friendly 🧑🏻‍💻</title>

<style>
* { box-sizing: border-box; margin:0; padding:0; }

body {
  font-family: 'Comic Sans MS','Segoe UI',Tahoma,Geneva,Verdana,sans-serif;
  color:#fff;
  min-height:100vh;
  background:linear-gradient(135deg,#2B2D42,#8D99AE);
  overflow-x:hidden;
  transition:margin-left 0.3s ease;
}

/* ================= HEADER ================= */
header {
  text-align:center;
  padding:1.5rem 1rem;
  background:#EF233C;
  border-bottom:3px solid #D90429;
  color:#fff;
  position:relative;
  z-index:1;
}

h1{font-size:2rem;margin-bottom:0.3rem;}
p{font-size:1rem;}

.container{
  max-width:1000px;
  margin:2rem auto;
  padding:0 1rem;
  position:relative;
}

/* ================= GALLERY ================= */
.gallery-container{
  position:relative;
  display:flex;
  align-items:center;
  margin-bottom:1rem;
}

.arrow{
  font-size:2rem;
  cursor:pointer;
  color:#FFD166;
  user-select:none;
  padding:0 0.5rem;
  transition:0.2s;
}
.arrow:hover{color:#06D6A0;}

.gallery-wrapper{
  overflow-x:hidden;
  display:flex;
  gap:1rem;
  scroll-behavior:smooth;
}

.gallery-item{
  flex:0 0 auto;
  width:280px;
  background:#073B4C;
  border-radius:16px;
  padding:2rem;
  text-align:center;
  cursor:pointer;
  transition:transform 0.3s, box-shadow 0.3s;
}
.gallery-item:hover{
  transform:translateY(-5px);
  box-shadow:0 10px 25px rgba(0,0,0,0.4);
}
.gallery-item img{
  width:80px;
  height:80px;
  margin-bottom:1rem;
}
.gallery-item h3{font-size:1.3rem;}

/* ================= SIDEBAR ================= */
.sidebar{
  background:rgba(43,45,66,0.95);
  padding:1rem;
  border-radius:12px;
  margin-top:1rem;
  box-shadow:0 4px 15px rgba(0,0,0,0.3);
}
.sidebar h2{
  margin-bottom:1rem;
  font-size:1.5rem;
  color:#FFD166;
}
.sidebar ul{list-style:none;}
.sidebar ul li{
  padding:0.8rem 0;
  cursor:pointer;
  border-bottom:1px solid rgba(255,255,255,0.2);
}
.sidebar ul li:hover{color:#06D6A0;}

/* ================= CONTENT ================= */
.content{
  background:rgba(255,255,255,0.05);
  padding:1.5rem;
  border-radius:12px;
  box-shadow:0 4px 20px rgba(0,0,0,0.3);
  margin-top:1rem;
  transition:0.5s;
}

pre{
  background:rgba(0,0,0,0.2);
  padding:1rem;
  border-radius:10px;
  overflow-x:auto;
}

/* ================= EDITOR ================= */
#codeEditor{
  width:100%;
  height:200px;
  background:rgba(0,0,0,0.15);
  border-radius:10px;
  color:#fff;
  padding:1rem;
  font-family:monospace;
  margin-top:1rem;
  display:none;
}

#runBtn{
  margin-top:0.8rem;
  padding:0.5rem 1rem;
  background:#FFD166;
  border:none;
  border-radius:8px;
  cursor:pointer;
  font-weight:bold;
  display:none;
}
#runBtn:hover{background:#06D6A0;}

#output{
  margin-top:1rem;
  background:rgba(0,0,0,0.2);
  border-radius:10px;
  padding:1rem;
  min-height:50px;
}

/* ================= PURPOSE ================= */
.purpose{
  background:#EF476F;
  color:#fff;
  border-radius:12px;
  padding:1.5rem;
  margin-top:2rem;
  text-align:center;
}
.purpose h2{color:#FFD166;margin-bottom:0.8rem;}

/* ================= DOWNLOAD SECTION ================= */
.download-section{
  background:rgba(0,0,0,0.15);
  border-radius:12px;
  padding:1.5rem;
  margin-top:2rem;
  text-align:center;
  box-shadow:0 4px 15px rgba(0,0,0,0.3);
}
.download-section h2{color:#FFD166;margin-bottom:0.5rem;}
.download-card{text-decoration:none;color:white;}
.download-card img{
  width:60px;
  height:60px;
  margin-bottom:0.8rem;
}

/* ================= HAMBURGER ================= */
#hamburgerBtn{
  font-size:2rem;
  cursor:pointer;
  color:#FFD166;
  position:fixed;
  top:1rem;
  left:1rem;
  z-index:1001;
}
#hamburgerBtn:hover{color:#06D6A0;}

#menuLinks{
  position:fixed;
  top:0;
  left:-250px;
  width:220px;
  height:100%;
  background:#073B4C;
  padding:2rem 1rem;
  transition:left 0.3s ease;
  z-index:1002;
}

#menuLinks a{
  display:block;
  padding:0.8rem 0;
  color:#FFD166;
  text-decoration:none;
  font-weight:bold;
}
#menuLinks a:hover{color:#06D6A0;}

#overlay{
  position:fixed;
  inset:0;
  background:rgba(0,0,0,0.5);
  display:none;
  z-index:1000;
}

@media(max-width:600px){
  .gallery-item{width:200px;padding:1.5rem;}
}
</style>
</head>

<body>

<!-- HAMBURGER -->
<div id="hamburgerBtn">&#9776;</div>
<div id="menuLinks">
  <a href="https://www.youtube.com/results?search_query=html+tutorial" target="_blank" onclick="closeMenu()">HTML Tutorial Link</a>
  <a href="https://www.youtube.com/results?search_query=css+tutorial" target="_blank" onclick="closeMenu()">CSS Tutorial Link</a>
  <a href="https://www.youtube.com/results?search_query=c%23+tutorial" target="_blank" onclick="closeMenu()">C# Tutorial Link</a>
  <a href="https://www.youtube.com/results?search_query=javascript+tutorial" target="_blank" onclick="closeMenu()">JavaScript Tutorial Link</a>
</div>
<div id="overlay" onclick="closeMenu()"></div>

<header>
  <h1>Beginner-Friendly 🧑🏻‍💻</h1>
  <p>Click the arrows to choose a coding language</p>
</header>

<audio id="clickSound" src="https://www.myinstants.com/media/sounds/click.mp3"></audio>

<div class="container">

<!-- LANGUAGE GALLERY -->
<div class="gallery-container">
  <span class="arrow" onclick="playClickSound(); scrollGallery(-1)">&#8592;</span>
  <div class="gallery-wrapper" id="galleryWrapper">
    <div class="gallery-item" onclick="playClickSound(); showCode('html')">
      <img src="https://cdn-icons-png.flaticon.com/512/732/732212.png">
      <h3>HTML</h3>
    </div>
    <div class="gallery-item" onclick="playClickSound(); showCode('css')">
      <img src="https://cdn-icons-png.flaticon.com/512/732/732190.png">
      <h3>CSS</h3>
    </div>
    <div class="gallery-item" onclick="playClickSound(); showCode('csharp')">
      <img src="https://cdn-icons-png.flaticon.com/512/6132/6132222.png">
      <h3>C#</h3>
    </div>
    <div class="gallery-item" onclick="playClickSound(); showCode('javascript')">
      <img src="https://cdn-icons-png.flaticon.com/512/5968/5968292.png">
      <h3>JavaScript</h3>
    </div>
  </div>
  <span class="arrow" onclick="playClickSound(); scrollGallery(1)">&#8594;</span>
</div>

<div class="content" id="content">
  <h2>Welcome!</h2>
  <p>Select a language from the gallery above to start learning.</p>
</div>

<div class="sidebar">
  <h2>Tutorials</h2>
  <ul id="tutorialList"><li>Select a language first!</li></ul>
</div>

<textarea id="codeEditor"></textarea>
<button id="runBtn" onclick="playClickSound(); runCode()">Run Code</button>
<div id="output"></div>

<!-- PURPOSE -->
<div class="purpose">
  <h2>Purpose of This Tool</h2>
  <p>
    This interactive coding school is designed for Grade 11 ICT students of
    Silangan National High School to learn HTML, CSS, C#, and JavaScript before
    Grade 12.
  </p>
</div>

<!-- DOWNLOAD GALLERY -->
<div class="download-section">
  <h2>Recommended Coding Apps 📱</h2>
  <p>Compatible Android apps for practicing code</p>

  <div class="gallery-container">
    <span class="arrow" onclick="playClickSound(); scrollDownload(-1)">&#8592;</span>
    <div class="gallery-wrapper" id="downloadGallery">

      <a class="gallery-item download-card" href="https://play.google.com/store/apps/details?id=com.rhmsoft.code" target="_blank" onclick="playClickSound()">
        <img src="https://cdn-icons-png.flaticon.com/512/732/732212.png">
        <h3>HTML Editor</h3>
      </a>

      <a class="gallery-item download-card" href="https://play.google.com/store/apps/details?id=com.qamar.ide.web" target="_blank" onclick="playClickSound()">
        <img src="https://cdn-icons-png.flaticon.com/512/732/732190.png">
        <h3>HTML / CSS IDE</h3>
      </a>

      <a class="gallery-item download-card" href="https://play.google.com/store/apps/details?id=com.radinc.csharpshell" target="_blank" onclick="playClickSound()">
        <img src="https://cdn-icons-png.flaticon.com/512/6132/6132222.png">
        <h3>C# Shell</h3>
      </a>

      <a class="gallery-item download-card" href="https://play.google.com/store/apps/details?id=com.qamar.ide.java" target="_blank" onclick="playClickSound()">
        <img src="https://cdn-icons-png.flaticon.com/512/226/226777.png">
        <h3>Java IDE</h3>
      </a>

      <a class="gallery-item download-card" href="https://play.google.com/store/apps/details?id=ru.iiec.jvdroid" target="_blank" onclick="playClickSound()">
        <img src="https://cdn-icons-png.flaticon.com/512/226/226777.png">
        <h3>JVDroid</h3>
      </a>

    </div>
    <span class="arrow" onclick="playClickSound(); scrollDownload(1)">&#8594;</span>
  </div>
</div>

</div>

<script>
let currentLang='';
let menuOpen=false;

/* CLICK SOUND */
function playClickSound(){
  const sound=document.getElementById('clickSound');
  sound.currentTime=0;
  sound.play();
}

/* CODE DATA */
const codeData = {
  html:{description:"HTML is used to structure content on the web.",example:`<h1>Hello World</h1>`,tutorials:[
    {title:"HTML Basics",code:`<h1>Hello HTML!</h1>`,description:"Create headings"},
    {title:"HTML Paragraphs",code:`<p>This is a paragraph.</p>`,description:"Learn paragraphs"}
  ]},
  css:{description:"CSS styles HTML elements.",example:`h1{color:red;}`,tutorials:[
    {title:"CSS Colors",code:`h1{color:blue;}`,description:"Change color"}
  ]},
  csharp:{description:"C# simulated output.",example:`Console.WriteLine("Hi");`,tutorials:[
    {title:"C# Variables",code:`int x=10; Console.WriteLine(x);`,description:"Variables"}
  ]},
  javascript:{description:"JavaScript adds interactivity.",example:`console.log("Hi");`,tutorials:[
    {title:"JS Variables",code:`let x=5; console.log(x);`,description:"Variables"}
  ]}
};

function showCode(lang){
  currentLang=lang;
  const data=codeData[lang];
  document.getElementById('content').innerHTML=
    `<h2>${lang.toUpperCase()}</h2><p>${data.description}</p><pre>${data.example}</pre>`;
  const list=document.getElementById('tutorialList');
  list.innerHTML='';
  data.tutorials.forEach(t=>{
    const li=document.createElement('li');
    li.innerHTML=`<strong>${t.title}</strong><br><small>${t.description}</small>`;
    li.onclick=()=>document.getElementById('codeEditor').value=t.code;
    list.appendChild(li);
  });
  document.getElementById('codeEditor').style.display='block';
  document.getElementById('runBtn').style.display='block';
  document.getElementById('codeEditor').value=data.example;
}

function runCode(){
  const code=document.getElementById('codeEditor').value;
  const out=document.getElementById('output');
  if(currentLang==='html') out.innerHTML=code;
  else if(currentLang==='css') out.innerHTML=`<style>${code}</style><p>CSS applied!</p>`;
  else if(currentLang==='javascript'){
    try{eval(code);}catch(e){out.innerText=e;}
  } else out.innerText="C# simulated:\n"+code;
}

function scrollGallery(dir){
  document.getElementById('galleryWrapper')
    .scrollBy({left:dir*300,behavior:'smooth'});
}
function scrollDownload(dir){
  document.getElementById('downloadGallery')
    .scrollBy({left:dir*300,behavior:'smooth'});
}

/* MENU */
document.getElementById('hamburgerBtn').onclick=()=>{
  playClickSound();
  if(!menuOpen){
    menuLinks.style.left='0';
    overlay.style.display='block';
    menuOpen=true;
  } else closeMenu();
};

function closeMenu(){
  menuLinks.style.left='-250px';
  overlay.style.display='none';
  menuOpen=false;
}
</script>

</body>
</html>
