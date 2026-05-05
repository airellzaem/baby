<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>For You 🤍</title>

<style>
body {
  margin: 0;
  font-family: 'Georgia', serif;
  background: #f8f5f2;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  text-align: center;
}

.container {
  max-width: 400px;
  padding: 20px;
}

h1 {
  font-weight: normal;
  color: #5a3e36;
}

button {
  margin-top: 20px;
  padding: 10px 20px;
  border: none;
  background: #c8a97e;
  color: white;
  cursor: pointer;
  border-radius: 20px;
}

.hidden {
  display: none;
}

.fade {
  animation: fadeIn 2s ease-in-out;
}

@keyframes fadeIn {
  from {opacity: 0;}
  to {opacity: 1;}
}

img {
  width: 100%;
  border-radius: 10px;
  margin-top: 20px;
}
</style>
</head>

<body>

<div class="container">

  <!-- PAGE 1 -->
  <div id="page1">
    <h1>Hi baby 🤍</h1>
    <p>I made something for you...<br>Play till the end okay?</p>
    <button onclick="nextPage(2)">Start</button>
  </div>

  <!-- PAGE 2 -->
  <div id="page2" class="hidden">
    <h1>Let’s see… 😏</h1>
    <p>What do you always call me?</p>

    <button onclick="wrong()">Airell</button><br>
    <button onclick="wrong()">Baby</button><br>
    <button onclick="nextPage(3)">Sayang</button>
  </div>

  <!-- PAGE 3 -->
  <div id="page3" class="hidden">
    <h1>Of course you got it right…</h1>
    <p>One last step before your surprise 💌</p>
    <button onclick="nextPage(4)">Unlock</button>
  </div>

  <!-- PAGE 4 -->
  <div id="page4" class="hidden">
    <h1 class="fade">For you, baby 🤍</h1>
    <p class="fade">I hope you say yes.</p>

    <!-- REPLACE IMAGE BELOW -->
    <img src="invitation.png" class="fade">
  </div>

</div>

<script>
function nextPage(page) {
  document.querySelectorAll('.container > div').forEach(div => div.classList.add('hidden'));
  document.getElementById('page' + page).classList.remove('hidden');
}

function wrong() {
  alert("Hmm… try again baby 😜");
}
</script>

</body>
</html>
