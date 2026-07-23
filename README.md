<!DOCTYPE html>
<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Happy Birthday Maryam</title>

<style>
body{
  margin:0;
  height:100vh;
  overflow:hidden;
  display:flex;
  justify-content:center;
  align-items:center;
  text-align:center;
  font-family:Arial, sans-serif;
  background:linear-gradient(135deg,#ff9a9e,#fad0c4,#a18cd1);
  color:white;
}

.container{
  z-index:2;
}

h1{
  font-size:45px;
  text-shadow:0 0 15px white;
  animation:pulse 2s infinite;
}

h2{
  font-size:25px;
}

button{
  padding:15px 30px;
  border:none;
  border-radius:30px;
  font-size:18px;
  cursor:pointer;
  background:white;
  color:#ff6b81;
}

.heart{
 position:absolute;
 bottom:-20px;
 font-size:30px;
 animation:up 6s linear infinite;
}

@keyframes up{
 from{
  transform:translateY(0);
  opacity:1;
 }
 to{
  transform:translateY(-110vh);
  opacity:0;
 }
}

@keyframes pulse{
 50%{
  transform:scale(1.1);
 }
}

.fire{
 position:absolute;
 font-size:35px;
 animation:fall 3s linear infinite;
}

@keyframes fall{
 from{top:-50px;}
 to{top:100vh;}
}

</style>
</head>

<body>

<div class="container">
<h1>🎂 Happy Birthday Maryam 🎂</h1>
<h2>✨ Born in 2009 ✨</h2>
<p>Wishing you a wonderful birthday full of happiness and beautiful moments 🎉</p>
<button onclick="celebrate()">🎁 Celebrate</button>
</div>


<script>

function celebrate(){
 alert("🎉 Happy Birthday Maryam! 🎉");
}

setInterval(()=>{
 let h=document.createElement("div");
 h.className="heart";
 h.innerHTML="❤️";
 h.style.left=Math.random()*100+"%";
 h.style.animationDuration=(3+Math.random()*4)+"s";
 document.body.appendChild(h);

 setTimeout(()=>h.remove(),6000);
},300);


setInterval(()=>{
 let f=document.createElement("div");
 f.className="fire";
 f.innerHTML="🎆";
 f.style.left=Math.random()*100+"%";
 f.style.animationDuration=(2+Math.random()*3)+"s";
 document.body.appendChild(f);

 setTimeout(()=>f.remove(),5000);
},500);

</script>

</body>
</html>
