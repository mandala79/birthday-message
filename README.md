<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Happy Birthday, Sayang ✨</title>

<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,400;0,500;0,600;1,400;1,500&family=Plus+Jakarta+Sans:wght@400;500;600;700&display=swap" rel="stylesheet">

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: #fdfbfb;
  background-image:
    radial-gradient(at 15% 15%, #ffdde1 0px, transparent 50%),
    radial-gradient(at 85% 85%, #ee9ca7 0px, transparent 50%),
    radial-gradient(at 50% 50%, #e0c3fc 0px, transparent 65%);
  font-family: 'Plus Jakarta Sans', sans-serif;
  overflow-x: hidden;
  padding: 45px 18px;
  position: relative;
}
#welcome-screen {
  position: fixed;
  inset: 0;
  width: 100%;
  height: 100%;
  z-index: 99999;
  background: rgba(255, 245, 247, 0.97);
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
  padding: 20px;
  transition: opacity 0.5s ease;
}
.welcome-title {
  font-family: 'Cormorant Garamond', serif;
  font-size: 32px;
  color: #3d2c3e;
  margin-bottom: 10px;
}
.welcome-sub {
  font-size: 14px;
  color: #6d5965;
  margin-bottom: 26px;
}
.slide {
  display: none;
  opacity: 0;
  width: 100%;
  max-width: 460px;
}

.slide.active {
  display: block;
  animation: fadeIn 0.7s ease forwards;
}
.card {
  position: relative;
  z-index: 10;
  max-width: 460px;
  width: 100%;
  background: rgba(255, 255, 255, 0.72);
  backdrop-filter: blur(18px);
  -webkit-backdrop-filter: blur(18px);
  border: 1px solid rgba(255, 255, 255, 0.9);
  border-radius: 30px;
  padding: 40px 26px;
  text-align: center;
  box-shadow: 0 20px 45px rgba(61, 44, 62, 0.08);
}
.floral-corner {
  position: absolute;
  font-size: 34px;
  pointer-events: none;
  filter: drop-shadow(0 4px 8px rgba(181, 101, 118, 0.2));
  animation: sway 4s ease-in-out infinite alternate;
  z-index: 15;
}

.fc-top-left {
  top: -18px;
  left: -14px;
}

.fc-top-right {
  top: -18px;
  right: -14px;
  animation-delay: 1s;
}

.fc-bottom-left {
  bottom: -18px;
  left: -14px;
  animation-delay: 1.5s;
}

.fc-bottom-right {
  bottom: -18px;
  right: -14px;
  animation-delay: 0.5s;
}

@keyframes sway {
  0% {
    transform: rotate(-6deg) scale(1);
  }
  100% {
    transform: rotate(8deg) scale(1.06);
  }
}
.tag {
  display: inline-block;
  font-size: 11px;
  letter-spacing: 2px;
  text-transform: uppercase;
  color: #8e6c88;
  background: rgba(255, 255, 255, 0.8);
  padding: 6px 14px;
  border-radius: 20px;
  margin-bottom: 14px;
}

h1 {
  font-family: 'Cormorant Garamond', serif;
  font-size: 36px;
  color: #3d2c3e;
  line-height: 1.2;
  margin-bottom: 18px;
}

h1 span {
  font-style: italic;
  color: #b56576;
}
.message-section {
  position: relative;
  margin: 18px 0;
  padding: 16px;
  background: rgba(255, 255, 255, 0.55);
  border-radius: 20px;
  border: 1px solid rgba(255, 255, 255, 0.8);
}

.message-text {
  font-size: 14px;
  line-height: 1.75;
  color: #4f3e45;
  font-weight: 400;
}
.inline-photos {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 14px;
  margin: 18px 0 8px 0;
  position: relative;
}

.mini-polaroid {
  position: relative;
  background: #fff;
  padding: 7px 7px 20px 7px;
  border-radius: 6px;
  box-shadow: 0 10px 22px rgba(61, 44, 62, 0.12);
  width: 135px;
  transition: transform 0.35s ease;
}

.mini-polaroid img {
  width: 100%;
  height: 135px;
  object-fit: cover;
  border-radius: 3px;
  display: block;
  background: #f3e6e8;
}

.mini-polaroid span {
  display: block;
  font-family: 'Cormorant Garamond', serif;
  font-style: italic;
  font-size: 12.5px;
  color: #6d5965;
  margin-top: 6px;
}

.rot-left {
  transform: rotate(-5deg);
}

.rot-right {
  transform: rotate(5deg);
}

.mini-polaroid:hover {
  transform: scale(1.08) rotate(0deg);
  z-index: 20;
}
.photo-flower {
  position: absolute;
  font-size: 20px;
  z-index: 12;
  pointer-events: none;
}
.pf-1 {
  top: -10px;
  left: -10px;
}
.pf-2 {
  bottom: 12px;
  right: -10px;
}
.btn {
  background: #b56576;
  color: #fff;
  border: none;
  padding: 14px 25px;
  border-radius: 50px;
  font-size: 13px;
  font-family: 'Plus Jakarta Sans', sans-serif;
  cursor: pointer;
  transition: all 0.2s ease;
  box-shadow: 0 8px 20px rgba(181, 101, 118, 0.3);
  margin: 8px 4px 0;
  position: relative;
  z-index: 100;
}

.btn:hover {
  background: #3d2c3e;
  transform: scale(1.04);
}
.btn-back {
  background: rgba(255, 255, 255, 0.9);
  color: #8e5263;
  border: 1px solid #e9c4cb;
  box-shadow: none;
}

.btn-back:hover {
  background: #f5e1e5;
  color: #3d2c3e;
}
.button-row {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-wrap: wrap;
  gap: 8px;
  margin-top: 14px;
}
.secret-message {
  margin-top: 20px;
  padding: 18px 16px;
  background: rgba(255, 255, 255, 0.65);
  border-radius: 20px;
  border: 1px dashed rgba(181, 101, 118, 0.4);
}
@keyframes fadeIn {
  from {
    opacity: 0;
    transform: translateY(10px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}
.petal {
  position: fixed;
  top: -10vh;
  background: rgba(255, 255, 255, 0.85);
  border-radius: 150% 0 150% 0;
  animation: fall linear infinite;
  pointer-events: none;
  z-index: 1;
}

@keyframes fall {
  0% {
    transform: translateY(0) rotate(0deg);
    opacity: 0;
  }
  10% {
    opacity: 1;
  }
  90% {
    opacity: 1;
  }
  100% {
    transform: translateY(115vh) rotate(360deg);
    opacity: 0;
  }
}
@media (max-width: 480px) {
  body {
    padding: 35px 14px;
  }

  .card {
    padding: 35px 18px;
  }

  .mini-polaroid {
    width: min(125px, 42vw);
  }

  .mini-polaroid img {
    height: 125px;
  }

  h1 {
    font-size: 32px;
  }

  .btn {
    padding: 13px 20px;
  }
}
</style>
</head>

<body>
<audio id="bgMusic" src="musik.mp3"
       autoplay loop preload="auto"></audio>
<div id="welcome-screen">

  <div class="welcome-title">
    Ada pesan kecil untuk si cantik🌸
  </div>

  <div class="welcome-sub">
    Ketuk tombol di bawah &amp; nikmati pesannya
  </div>

  <button type="button" class="btn"
          onclick="bukaKartu()">
    Open 🤍
  </button>
</div>
<div class="card slide" id="slide2">

  <div class="floral-corner fc-top-left">🌸</div>
  <div class="floral-corner fc-top-right">🌷</div>
  <div class="floral-corner fc-bottom-left">🌺</div>
  <div class="floral-corner fc-bottom-right">🌸</div>

  <div class="tag">
    Special Day ✨
  </div>

  <h1>
    Happy Birthday, <br>
    <span>sayang</span>
  </h1>

  <div class="message-section">
    <p class="message-text">
      Selamat bertambah usia, cantik kuu. Semoga di bab baru ini,
      setiap langkahmu selalu dipenuhi ketenangan, hal-hal baik
      yang tak terduga, dan kebahagiaan yang sederhana.
    </p>
    <div class="inline-photos">
      <div class="mini-polaroid rot-left">
        <span class="photo-flower pf-1">🌷</span>
        <img src="file photo"
             alt="Foto 1">
        <span>sweet smile</span>
      </div>
      <div class="mini-polaroid rot-right">
        <span class="photo-flower pf-2">🌸</span>
        <img src="file photo"
             alt="Foto 2">
        <span>always shining</span>
      </div>
    </div>
  </div>
  <div class="button-row">
    <button type="button"
            class="btn btn-back"
            onclick="kembaliSlide(1)">
      ← Kembali
    </button>
    <button type="button"
            class="btn"
            onclick="pindahSlide(3)">
      Baca Pesan Selanjutnya 🌷
    </button>
  </div>
</div>
<div class="card slide" id="slide3">

  <div class="floral-corner fc-top-left">🌸</div>
  <div class="floral-corner fc-top-right">🌷</div>
  <div class="floral-corner fc-bottom-left">🌺</div>
  <div class="floral-corner fc-bottom-right">🌸</div>

  <div class="tag">
    A Little Note 🤍
  </div>

  <h1>
    A Special Message <br>
    <span>For my world</span>
  </h1>
  
  <div class="secret-message">
   <p class="message-text">
      "Terima kasih sudah bertahan sejauh ini dan selalu
      membawa energi hangat di sekitar. Semoga semua impian
      dan doa baikmu pelan-pelan terwujud tahun ini!" 🤍
    </p>
 <div class="inline-photos">
      <div class="mini-polaroid rot-right">
        <span class="photo-flower pf-1">🌺</span>
        <img src="file photo" alt="Foto 3">
        <span>cherished day</span>
      </div>
      <div class="mini-polaroid rot-left">
        <span class="photo-flower pf-2">🌷</span>
        <img src="file photo" alt="Foto 4">
        <span>best wishes</span>
      </div>
    </div>
  </div>
  <div class="button-row">
    <button type="button"
            class="btn btn-back"
            onclick="kembaliSlide(2)">
      ← Kembali
    </button>
  </div>
</div>
<script>
const bgMusic = document.getElementById("bgMusic");
bgMusic.volume = 0.5;
async function startMusic() {
  try {
    await bgMusic.play();
  } catch (error) {
  }
}
window.addEventListener("load", function() {
  startMusic();
});

function bukaKartu() {
  startMusic();

  const welcome =
    document.getElementById("welcome-screen");

  const slide2 =
    document.getElementById("slide2");
  
  welcome.style.opacity = "0";
  setTimeout(function() {
    welcome.style.display = "none";
    slide2.classList.add("active");
   window.scrollTo({
      top: 0,
      behavior: "smooth"
    });
  }, 500);
}
function pindahSlide(target) {
  const slides =
    document.querySelectorAll(".slide");
  slides.forEach(function(slide) {
    slide.classList.remove("active");
  });
  const nextSlide =
    document.getElementById("slide" + target);
  if (nextSlide) {
    nextSlide.classList.add("active");
  }
  window.scrollTo({
    top: 0,
    behavior: "smooth"
  });
}

function kembaliSlide(target) {
  if (target === 1) {
    const welcome =
      document.getElementById("welcome-screen");
    const slides =
      document.querySelectorAll(".slide");
    slides.forEach(function(slide) {
      slide.classList.remove("active");
    });
    welcome.style.display = "flex";
    requestAnimationFrame(function() {
      welcome.style.opacity = "1";
    });
  }
  else {
    pindahSlide(target);
  }
  window.scrollTo({
    top: 0,
    behavior: "smooth"
  });
}
</script>
</body>
</html>
