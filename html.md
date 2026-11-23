<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="theme-color" content="#260d2c">
<title>Selamat Ulang Tahun ❤️</title>
<style>
*{box-sizing:border-box}
body{margin:0;min-height:100vh;font-family:Georgia,serif;color:#fff;background:radial-gradient(circle at top,#71345f 0,#351536 48%,#170d22 100%);display:flex;align-items:center;justify-content:center;overflow:hidden;text-align:center;padding:22px}
.card{position:relative;z-index:2;width:min(100%,520px);padding:38px 25px;border:1px solid #ffffff38;border-radius:28px;background:#ffffff12;backdrop-filter:blur(9px);box-shadow:0 18px 60px #0006}
.small{letter-spacing:4px;text-transform:uppercase;font:12px Arial,sans-serif;color:#ffd7e8}
h1{font-size:clamp(34px,9vw,56px);line-height:1.08;margin:18px 0 10px;color:#ffe0ed;text-shadow:0 3px 18px #ff6fa888}
.age{font-size:64px;color:#ffd0e4;margin:4px 0}
p{font-size:18px;line-height:1.7;color:#fff0f6}
button{border:0;border-radius:999px;padding:15px 25px;margin-top:15px;background:linear-gradient(135deg,#ff8fbd,#ff4f91);color:#381329;font-weight:bold;font-size:16px;box-shadow:0 8px 25px #ff4f9155}
button:active{transform:scale(.97)}
#message{display:none;animation:fade .9s ease}
#hint{font:12px Arial,sans-serif;color:#f5cddd;margin-top:16px}
.heart{position:fixed;bottom:-40px;color:#ff9fc6;opacity:.7;animation:float linear infinite;z-index:1}
@keyframes float{to{transform:translateY(-115vh) rotate(360deg);opacity:0}}
@keyframes fade{from{opacity:0;transform:translateY(15px)}to{opacity:1;transform:translateY(0)}}
</style>
</head>
<body>
<div class="card">
  <div class="small">A special day for you</div>
  <div style="font-size:42px;margin-top:16px">🎂 ✨ 🎈</div>
  <h1>Selamat<br>Ulang Tahun!</h1>
  <div class="age">22</div>
  <p>November 28</p>
  <button id="openBtn">BUKA UCAPAN ❤️</button>
  <div id="message">
    <p>Selamat ulang tahun ❤️</p>
    <p>Semoga kamu selalu diberi kebahagiaan, kesehatan, dan kekuatan untuk melewati setiap langkah kehidupan.</p>
    <p>Semoga semua hal baik yang kamu impikan satu per satu menjadi nyata. Tetap jadi seseorang yang istimewa. ✨</p>
    <div style="font-size:28px;margin-top:12px">❤️ 🌹 ❤️</div>
  </div>
  <div id="hint">Tekan tombol untuk membuka ucapan dan memutar musik</div>
</div>
<audio id="song" src="lagu-ulang-tahun.mp3" preload="auto" loop></audio>
<script>
const btn=document.getElementById('openBtn');
const msg=document.getElementById('message');
const hint=document.getElementById('hint');
const song=document.getElementById('song');
btn.addEventListener('click',async()=>{
  msg.style.display='block';
  btn.style.display='none';
  hint.textContent='Musik ulang tahun sedang diputar 🎵';
  try{await song.play();}
});
for(let i=0;i<18;i++){
  const h=document.createElement('div');h.className='heart';h.textContent=['♥','♡','❤'][i%3];
  h.style.left=Math.random()*100+'vw';
  h.style.animationDuration=(7+Math.random()*9)+'s';
  h.style.animationDelay=(-Math.random()*14)+'s';
  h.style.fontSize=(14+Math.random()*22)+'px';
  document.body.appendChild(h);
}
</script>
</body>
</html>
