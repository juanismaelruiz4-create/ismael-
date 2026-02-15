<!DOCTYPE html><html lang="es">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Nuestra Historia</title>
<style>
body{
  margin:0;
  font-family:Arial, sans-serif;
  background:#0b0b0f;
  color:white;
  text-align:center;
}
.section{
  min-height:100vh;
  display:flex;
  flex-direction:column;
  justify-content:center;
  align-items:center;
  padding:20px;
}
.hero{
  background:linear-gradient(to bottom, rgba(0,0,0,.6), rgba(0,0,0,.9)),
             url('https://images.unsplash.com/photo-1516589178581-6cd7833ae3b2?auto=format&fit=crop&w=800&q=80');
  background-size:cover;
  background-position:center;
}
.heart{
  font-size:60px;
  color:#ff2d55;
}
.title{
  font-size:42px;
  font-weight:bold;
}
.subtitle{
  opacity:.8;
  margin:15px 0;
}
.counter{
  background:rgba(255,255,255,.1);
  padding:15px 25px;
  border-radius:30px;
  margin-top:20px;
}
.card{
  background:linear-gradient(135deg,#7b2ff7,#f107a3);
  padding:20px;
  border-radius:15px;
  margin:10px;
  width:90%;
  max-width:400px;
}
.cert{
  border:3px solid gold;
  padding:40px 20px;
  border-radius:20px;
  max-width:500px;
}
button{
  margin-top:30px;
  padding:12px 25px;
  border:none;
  border-radius:25px;
  background:#ff2d55;
  color:white;
  font-size:16px;
  cursor:pointer;
}
</style>
</head>
<body><section class="section hero">
  <div class="heart">❤</div>
  <div class="title">Ismael & Brisa</div>
  <div class="subtitle">Una historia de amor infinito</div>
  <div class="counter" id="counter">Juntos desde hace ...</div>
  <button onclick="scrollToSection('fechas')">Desliza</button>
</section><section class="section" id="fechas">
  <h2>Fechas que nos marcan</h2>
  <div class="card">
    <h3>Nos conocimos</h3>
    <p>El día que todo empezó</p>
    <small>14 de junio de 2023</small>
  </div>
  <div class="card">
    <h3>Primera cita</h3>
    <p>Nuestra primera salida juntos</p>
    <small>19 de julio de 2023</small>
  </div>
</section><section class="section">
  <div class="cert">
    <h2 style="color:gold">CERTIFICADO</h2>
    <h3>DE AMOR ETERNO</h3>
    <p>Se otorga el presente reconocimiento a</p>
    <h2>Ismael & Brisa</h2>
    <p>Por compartir juntos <span id="days"></span> días de amor.</p>
  </div>
</section><script>
const startDate = new Date('2023-06-14');
const today = new Date();
const diffTime = today - startDate;
const diffDays = Math.floor(diffTime / (1000 * 60 * 60 * 24));

document.getElementById('counter').innerText =
  `Juntos desde hace ${diffDays} días`;

document.getElementById('days').innerText = diffDays;

function scrollToSection(id){
  document.getElementById(id).scrollIntoView({behavior:'smooth'});
}
</script></body>
</html>
