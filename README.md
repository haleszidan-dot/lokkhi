<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>APRIVA ❤️ Forever</title>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  min-height: 100vh;
  min-height: 100dvh;
  overflow-x: hidden;
  overflow-y: auto;
  font-family: 'Trebuchet MS', sans-serif;
  background: radial-gradient(circle at top, #8d174e, #380020 65%, #160014);
  color: white;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  position: relative;
}

/* Romantic stickers */
.sticker {
  position: fixed;
  z-index: 1;
  font-size: clamp(35px, 9vw, 65px);
  pointer-events: none;
  filter: drop-shadow(0 0 12px rgba(255,100,180,.5));
  animation: dance 2s infinite ease-in-out;
}

.s1 { top: 7%; left: 5%; }
.s2 { top: 12%; right: 6%; animation-delay: .5s; }
.s3 { bottom: 12%; left: 5%; animation-delay: .8s; }
.s4 { bottom: 9%; right: 5%; animation-delay: .3s; }
.s5 { top: 43%; left: 3%; animation-delay: 1s; }
.s6 { top: 43%; right: 3%; animation-delay: .6s; }

@keyframes dance {
  0%, 100% {
    transform: rotate(-12deg) translateY(0);
  }
  50% {
    transform: rotate(12deg) translateY(-14px);
  }
}

.container {
  position: relative;
  z-index: 3;
  width: 90%;
  max-width: 430px;
  padding: 28px 20px;
  margin: 25px auto;
  border: 1px solid rgba(255,255,255,.2);
  border-radius: 28px;
  background: rgba(50,0,30,.65);
  backdrop-filter: blur(9px);
  box-shadow: 0 0 35px rgba(255,30,130,.3);
}

h1 {
  font-size: clamp(48px, 14vw, 75px);
  font-weight: 1000;
  letter-spacing: 5px;
  color: #ffc2df;
  text-shadow: 0 0 15px #ff168b, 0 0 35px #ff168b;
  animation: pulse 2s infinite;
}

@keyframes pulse {
  50% { transform: scale(1.05); }
}

.question {
  font-size: 22px;
  font-weight: bold;
  margin: 25px 0;
  line-height: 1.5;
}

.buttons {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 22px;
  min-height: 65px;
  margin-top: 30px;
}

button {
  border: none;
  padding: 15px 30px;
  font-size: 19px;
  font-weight: bold;
  border-radius: 40px;
  cursor: pointer;
  box-shadow: 0 0 18px #ff3b9d;
}

#yes {
  background: #ff168b;
  color: white;
}

#no {
  background: white;
  color: #b00055;
  position: relative;
  z-index: 10;
}

/* Floating hearts */
.heart {
  position: fixed;
  bottom: -40px;
  z-index: 2;
  pointer-events: none;
  animation: floatUp linear forwards;
}

@keyframes floatUp {
  to {
    transform: translateY(-115vh) rotate(360deg);
    opacity: 0;
  }
}

/* Success screen */
#success {
  display: none;
  animation: appear 1s ease;
}

@keyframes appear {
  from {
    opacity: 0;
    transform: scale(.6);
  }
  to {
    opacity: 1;
    transform: scale(1);
  }
}

.success-title {
  font-size: 29px;
  font-weight: 1000;
  color: #ffb8dc;
  text-shadow: 0 0 15px #ff168b;
  margin-bottom: 17px;
}

.gift {
  font-size: 65px;
  display: inline-block;
  animation: giftDance .7s infinite alternate;
}

@keyframes giftDance {
  from { transform: rotate(-15deg) translateY(0); }
  to { transform: rotate(15deg) translateY(-15px); }
}

/* Animated message lines */
.message-area {
  margin: 15px 0;
}

.message-line {
  display: none;
  width: 100%;
  font-size: 19px;
  font-weight: 1000;
  line-height: 1.6;
  color: #fff0f8;
  text-shadow: 0 0 12px rgba(255,22,139,.5);
  margin: 10px 0;
}

.message-line.active {
  display: block;
  animation: lineFadeIn 1s ease forwards;
}

.message-line.fade-out {
  display: block;
  animation: lineFadeOut .8s ease forwards;
}

/* All lines stay visible after animation */
.message-line.final-visible {
  display: block;
  opacity: 1;
  transform: none;
  filter: none;
  animation: finalAppear 1s ease both;
}

@keyframes lineFadeIn {
  from {
    opacity: 0;
    transform: translateY(18px) scale(.95);
    filter: blur(5px);
  }
  to {
    opacity: 1;
    transform: translateY(0) scale(1);
    filter: blur(0);
  }
}

@keyframes lineFadeOut {
  from {
    opacity: 1;
    transform: translateY(0);
    filter: blur(0);
  }
  to {
    opacity: 0;
    transform: translateY(-15px);
    filter: blur(5px);
  }
}

@keyframes finalAppear {
  from {
    opacity: 0;
    transform: translateY(10px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* Final love note */
.love-note {
  display: none;
  font-size: 15px;
  line-height: 1.7;
  color: #ffd5e9;
  margin-top: 17px;
  font-style: italic;
}

.love-note.show {
  display: block;
  animation: lineFadeIn 1.2s ease forwards;
}

.signature {
  display: none;
  font-size: 23px;
  font-weight: 1000;
  color: #ffacd6;
  margin-top: 15px;
}

.signature.show {
  display: block;
  animation: lineFadeIn 1.5s ease forwards;
}

.final-hearts {
  display: none;
  font-size: 32px;
  margin-top: 15px;
}

.final-hearts.show {
  display: block;
  animation: lineFadeIn 1.5s ease forwards;
}

/* Celebration stickers */
.graffiti {
  position: fixed;
  font-size: 30px;
  z-index: 1;
  pointer-events: none;
  animation: dance 1.5s infinite ease-in-out;
}

@media(max-width: 380px) {
  .container {
    padding: 22px 15px;
  }

  .message-line {
    font-size: 17px;
  }

  .love-note {
    font-size: 13px;
  }

  .success-title {
    font-size: 25px;
  }
}
</style>
</head>

<body>

<!-- Romantic stickers -->
<div class="sticker s1">💏</div>
<div class="sticker s2">💃🕺</div>
<div class="sticker s3">😘💕</div>
<div class="sticker s4">🕺💃</div>
<div class="sticker s5">💋</div>
<div class="sticker s6">🥰</div>

<!-- First screen -->
<div class="container" id="main">

  <h1>APRIVA</h1>

  <div class="question">
    Will you be mine forever? ❤️
  </div>

  <div class="buttons">
    <button id="yes" onclick="sayYes()">YES 💖</button>
    <button id="no">NO 🤷‍♂️</button>
  </div>

</div>

<!-- YES screen -->
<div class="container" id="success">

  <div class="success-title">
    I KNEW YOU LOVED ME! ❤️
  </div>

  <div class="gift">🎁💃</div>

  <!-- Animated messages -->
  <div class="message-area" id="messageArea">

    <div class="message-line">
      LET'S BEGIN A NEW CHAPTER TOGETHER. 💍
    </div>

    <div class="message-line">
      WE HAVE SUCCESSFULLY COMPLETED 5 WONDERFUL YEARS TOGETHER! ❤️
    </div>

    <div class="message-line">
      FIVE YEARS, COUNTLESS MEMORIES, LITTLE ARGUMENTS AND ENDLESS LAUGHTER. 💕
    </div>

    <div class="message-line">
      OUR LOVE KEEPS GROWING STRONGER EVERY DAY. 🥰
    </div>

    <div class="message-line">
      I DON'T JUST WANT ANOTHER FIVE YEARS WITH YOU.
    </div>

    <div class="message-line">
      I WANT EVERY CHAPTER, EVERY ADVENTURE AND EVERY BEAUTIFUL MOMENT WITH YOU. ❤️
    </div>

    <div class="message-line">
      HERE'S TO US, OUR DREAMS AND A LIFETIME OF TOGETHERNESS. 💍
    </div>

  </div>

  <!-- Final love note -->
  <div class="love-note" id="loveNote">
    You are my favourite chapter, my sweetest memory
    and the person I want beside me in every tomorrow.
    No matter what life brings, let's keep choosing each other. ❤️
  </div>

  <div class="signature" id="signature">
    Yours,<br>
    BOJJAT
  </div>

  <div class="final-hearts" id="finalHearts">
    💋 💞 🥰 💍
  </div>

</div>

<script>

// Floating hearts
const emojis = ["❤️","💗","💕","💖","💘","💋","🥰"];

function createHeart() {
  const heart = document.createElement("div");

  heart.className = "heart";
  heart.innerHTML = emojis[
    Math.floor(Math.random() * emojis.length)
  ];

  heart.style.left = Math.random() * 100 + "vw";
  heart.style.fontSize = (18 + Math.random() * 25) + "px";
  heart.style.animationDuration = (4 + Math.random() * 4) + "s";

  document.body.appendChild(heart);

  setTimeout(() => heart.remove(), 8500);
}

setInterval(createHeart, 300);


// NO button escaping
const noButton = document.getElementById("no");

function escapeNo() {
  const maxX = Math.max(5, window.innerWidth - noButton.offsetWidth - 10);
  const maxY = Math.max(5, window.innerHeight - noButton.offsetHeight - 10);

  noButton.style.position = "fixed";
  noButton.style.left = Math.max(5, Math.random() * maxX) + "px";
  noButton.style.top = Math.max(5, Math.random() * maxY) + "px";
}

noButton.addEventListener("mouseenter", escapeNo);

noButton.addEventListener("touchstart", function(e) {
  e.preventDefault();
  escapeNo();
}, { passive: false });

noButton.addEventListener("click", function(e) {
  e.preventDefault();
  escapeNo();
});


// YES celebration
let started = false;

function sayYes() {

  if (started) return;
  started = true;

  document.getElementById("main").style.display = "none";
  document.getElementById("success").style.display = "block";

  noButton.style.display = "none";

  // Romantic stickers
  const stickers = [
    "💏", "💃🕺", "💋", "💕",
    "🥰", "❤️", "😘", "💞",
    "🎀", "💍", "🫶"
  ];

  for (let i = 0; i < 22; i++) {
    const sticker = document.createElement("div");

    sticker.className = "graffiti";
    sticker.innerHTML = stickers[i % stickers.length];

    sticker.style.left = Math.random() * 90 + "vw";
    sticker.style.top = Math.random() * 95 + "vh";

    document.body.appendChild(sticker);
  }

  // Celebration hearts
  for (let i = 0; i < 60; i++) {
    setTimeout(createHeart, i * 70);
  }

  // One-by-one text animation
  const lines = Array.from(
    document.querySelectorAll(".message-line")
  );

  let currentIndex = 0;

  const displayDuration = 2400;
  const fadeDuration = 800;

  function showNextLine() {

    if (currentIndex >= lines.length) {

      // SHOW ALL MESSAGES TOGETHER
      lines.forEach((line, index) => {
        line.classList.remove("active", "fade-out");
        line.classList.add("final-visible");
        line.style.animationDelay = (index * 0.12) + "s";
      });

      // Show final love note
      document.getElementById("loveNote").classList.add("show");

      setTimeout(() => {
        document.getElementById("signature").classList.add("show");
      }, 800);

      setTimeout(() => {
        document.getElementById("finalHearts").classList.add("show");
      }, 1500);

      return;
    }

    const currentLine = lines[currentIndex];

    currentLine.classList.add("active");

    setTimeout(() => {

      currentLine.classList.remove("active");
      currentLine.classList.add("fade-out");

      setTimeout(() => {

        currentLine.classList.remove("fade-out");

        currentIndex++;
        showNextLine();

      }, fadeDuration);

    }, displayDuration);
  }

  // Start animation
  setTimeout(showNextLine, 1000);
}

</script>

</body>
</html>
