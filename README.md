<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Surprise 💖</title>


<link href="https://fonts.googleapis.com/css2?family=Playwrite+NZ+Basic:wght@100..400&display=swap" rel="stylesheet">

<style>
*{margin:0;padding:0;box-sizing:border-box}

body{
  font-family:'Playwrite NZ Basic',cursive;
  background:radial-gradient(circle at top,#3a0d1f,#0b0509);
  min-height:100vh;
  display:flex;
  justify-content:center;
  align-items:center;
  overflow:hidden;
}

.card{
  width:360px;
  background:#fff7f9;
  border-radius:20px;
  padding:25px;
  text-align:center;
  box-shadow:0 20px 50px rgba(0,0,0,.4);
  animation:fade .6s ease;
}

@keyframes fade{
  from{opacity:0;transform:scale(.95)}
  to{opacity:1;transform:scale(1)}
}

h1{
  font-family:'Great Vibes',cursive;
  color:#d6336c;
  font-size:2.4rem;
  margin:15px 0;
}

p{
  color:#555;
  font-size:.95rem;
  line-height:1.6;
}

img{
  width:120px;
  margin:auto;
}

.btn{
  margin-top:20px;
  padding:12px 26px;
  border:none;
  border-radius:25px;
  background:#e64980;
  color:white;
  font-size:1rem;
  cursor:pointer;
  box-shadow:0 6px 15px rgba(230,73,128,.4);
}

.btn.alt{
  background:#f1c6d4;
  color:#333;
}

.options{
  display:grid;
  grid-template-columns:1fr 1fr;
  gap:10px;
  margin-top:20px;
}

.hidden{
  display:none;
}
</style>
</head>

<body>


<div class="card" id="s1">
  <img src="eye blinking.webp" alt="cute">
  <h1>Hey!</h1>
  <p>I want to ask you something?<br>Can I?</p>
  <div class="options">
    <button class="btn" onclick="go(2)">YES</button>
    <button class="btn alt" onclick="go(3)">NO</button>
  </div>
</div>

<!-- Screen 2 -->
<div class="card hidden" id="s2">
  <img src="eye hiding.webp">
  <h1>Good My Cutiepie 😍</h1>
  <p>Most important question : are you ready?</p>
  <button class="btn" onclick="go(4)">Yes!!</button>
</div>

<!-- Screen 3 -->
<div class="card hidden" id="s3">
  <img src="pan in hand.webp">
  <h1>How Dare You!</h1>
  <p>Go back to say YES!</p>
  <button class="btn" onclick="go(1)">Go Back</button>
</div>

<!-- Screen 4 -->
<div class="card hidden" id="s4">
  <img src="bear rose.webp">
  <h1>Will you be Mine Forever? 💕</h1>
  <div class="options">
    <button class="btn" onclick="go(5)">(A) Yes</button>
    <button class="btn" onclick="go(5)">(B) D</button>
    <button class="btn" onclick="go(5)">(C) A</button>
    <button class="btn" onclick="go(5)">(D) Obviously Yes</button>
  </div>
</div>

<!-- Screen 5 -->
<div class="card hidden" id="s5">
  <img src="yes.gif">
  <h1>I Knew That You Would Say Yes! 😍</h1>
  <button class="btn" onclick="go(6)">A Shayari for you 💌</button>
</div>

<!-- Screen 6 -->
<div class="card hidden" id="s6">
  <h1>My Dearest Loved one 💞</h1><br>
  <p>
    तुम्हारे आंखों को समंदर और चेहरे को गुलाब लिख देता... 🌊👀<br>
    अगर सवाल हुस्न का होता तो तुम्हें मेरा जवाब लिख देता... 🌹🫠<br>
    और मेरा यक़ीन करो अगर में एक सच्चा शायर होता,<br>
    तो तुम्हारी खूबसूरती के ऊपर एक किताब लिख देता... 👀❤️
  </p>
  <p style="margin-top:50px;font-weight:800;color:#d6336c">
    Forever Yours 💖
  </p>
</div>


<script>
function go(n){
  document.querySelectorAll('.card').forEach(card=>{
    card.classList.add('hidden');
  });
  document.getElementById('s'+n).classList.remove('hidden');
}
</script>

</body>
</html>
