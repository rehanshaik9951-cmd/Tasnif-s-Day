# Tasnif-s-Day
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Happy Birthday Tasnif 🩷</title>

<!-- Google Fonts -->
<link href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@700&family=Roboto:wght@400;500&display=swap" rel="stylesheet">

<style>
body {
  margin: 0;
  height: 100vh;
  background: linear-gradient(120deg, #ffd1dc, #fbc2eb);
  display: flex;
  justify-content: center;
  align-items: center;
  font-family: 'Roboto', sans-serif;
  overflow: hidden;
}

/* Floating hearts */
.heart {
  position: absolute;
  font-size: 20px;
  animation: float 6s infinite ease-in-out;
  filter: drop-shadow(0 0 6px #ff5e78);
}
@keyframes float {
  0% {transform: translateY(100vh) rotate(0deg); opacity: 0;}
  50% {opacity: 1;}
  100% {transform: translateY(-10vh) rotate(360deg); opacity: 0;}
}

/* Card style */
.card {
  background: rgba(255,255,255,0.95);
  padding: 50px;
  border-radius: 25px;
  text-align: center;
  box-shadow: 0 20px 40px rgba(0,0,0,0.25);
  animation: fadeIn 2.5s ease;
  max-width: 450px;
}

/* Heading style */
h1 {
  font-family: 'Dancing Script', cursive;
  color: #e75480;
  font-size: 3em;
  animation: glow 2s infinite alternate;
  margin-bottom: 15px;
}

/* Paragraphs */
p {
  font-size: 1.15em;
  color: #444;
  line-height: 1.7;
}

/* Click-to-reveal text */
.click-text {
  margin-top: 25px;
  font-size: 1.1em;
  color: #e75480;
  cursor: pointer;
  animation: pulse 1.5s infinite;
  font-weight: 500;
}

/* Hidden love lines */
.love-line {
  display: none;
  font-size: 1.3em;
  color: #e75480;
  font-style: italic;
  margin-top: 15px;
  font-family: 'Dancing Script', cursive;
}

/* Animations */
@keyframes fadeIn {
  from {opacity: 0; transform: translateY(40px);}
  to {opacity: 1; transform: translateY(0);}
}
@keyframes glow {
  from {text-shadow: 0 0 10px #ff9aa2;}
  to {text-shadow: 0 0 25px #ff5e78;}
}
@keyframes pulse {
  0% {opacity: 0.5;}
  50% {opacity: 1;}
  100% {opacity: 0.5;}
}
</style>
</head>

<body>

<!-- Background Music -->
<audio autoplay loop>
  <source src="https://cdn.pixabay.com/download/audio/2023/03/07/audio_2bdb1f0c67.mp3?filename=romantic-soft-piano-11219.mp3" type="audio/mp3">
</audio>

<script>
// Create floating hearts
for(let i=0;i<25;i++){
  let heart=document.createElement("div");
  heart.innerHTML="🩷";
  heart.className="heart";
  heart.style.left=Math.random()*100+"vw";
  heart.style.animationDuration=(4+Math.random()*4)+"s";
  heart.style.fontSize=(18+Math.random()*25)+"px";
  document.body.appendChild(heart);
}

// Show hidden message lines one by one
function revealMessage(){
  const lines = document.querySelectorAll(".love-line");
  let delay = 0;
  lines.forEach(line => {
    line.style.opacity = 0;
    setTimeout(() => {
      line.style.display = "block";
      line.style.transition = "opacity 1.5s";
      line.style.opacity = 1;
    }, delay);
    delay += 1800; // 1.8s between each line
  });
}
</script>

<div class="card">
  <h1>Happy Birthday Tasnif 🩷</h1>

  <p>
    At this quiet midnight hour 🌙<br>
    I hope this little surprise reaches your heart gently ✨
  </p>

  <p>
    You bring a softness that words often fail to explain,<br>
    yet the heart always understands 💖
  </p>

  <p>
    May this year hold warmth, calm happiness,<br>
    and moments that feel like home 🌸
  </p>

  <div class="click-text" onclick="revealMessage()">
    Click here… a secret just for you 🩷
  </div>

  <div id="hidden" class="hidden-message">
    <p class="love-line">Tum woh roshni ho jis ke baghair raat adhuri hai 🌙</p>
    <p class="love-line">Tum woh khwab ho jo har din haqeeqat ban jaye ✨</p>
    <p class="love-line">Tum woh khushboo ho jo baharon mein bhi bas tumhari rehti hai 🌹</p>
    <p class="love-line">Meri dhadkan tumhare naam ke baghair mukammal nahi ❤️</p>
    <p class="love-line">Meri har saans tumhare ishq se roshan hai 🩷</p>
    <p class="love-line">Meri mohabbat tumhare liye la-zawal aur hamesha ke liye hai 💫</p>
  </div>
</div>

</body>
</html>
