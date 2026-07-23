<canvas id="fireworks"></canvas>

<script src="https://cdn.jsdelivr.net/npm/fireworks-js@2.10.7/dist/index.umd.js"></script>

<script>
const container = document.getElementById('fireworks');
const fireworks = new Fireworks.default(container,{
  autoresize:true,
  opacity:0.5,
  acceleration:1.05,
  friction:0.97,
  gravity:1.2,
  particles:120,
  explosion:8
});
fireworks.start();
</script>

<script>
setInterval(()=>{
    let heart=document.createElement("div");
    heart.innerHTML="❤️";
    heart.style.position="fixed";
    heart.style.left=Math.random()*100+"vw";
    heart.style.top="100vh";
    heart.style.fontSize=(20+Math.random()*30)+"px";
    heart.style.animation="floatUp 6s linear forwards";
    document.body.appendChild(heart);

    setTimeout(()=>heart.remove(),6000);
},300);

const style=document.createElement("style");
style.innerHTML=`
@keyframes floatUp{
0%{transform:translateY(0);opacity:1;}
100%{transform:translateY(-120vh);opacity:0;}
}
#fireworks{
position:fixed;
top:0;
left:0;
width:100%;
height:100%;
pointer-events:none;
z-index:999;
}`;
document.head.appendChild(style);
</script># birthday-surprise
