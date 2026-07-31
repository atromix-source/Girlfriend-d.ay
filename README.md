# Girlfriend-d.ay
Girlfriend day 
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Happy Girlfriend Day ❤️</title>

<style>
*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:Arial,sans-serif;
}

body{
overflow:hidden;
background:linear-gradient(135deg,#ff758c,#ff7eb3,#ffc3a0);
}

.page{
position:absolute;
width:100%;
height:100vh;
display:flex;
flex-direction:column;
justify-content:center;
align-items:center;
text-align:center;
padding:30px;
color:white;
opacity:0;
transform:scale(.9);
pointer-events:none;
transition:1s;
}

.page.active{
opacity:1;
transform:scale(1);
pointer-events:auto;
animation:fade 1s;
}

@keyframes fade{
from{
opacity:0;
transform:translateY(40px);
}
to{
opacity:1;
transform:translateY(0);
}
}

h1{
font-size:45px;
margin-bottom:20px;
text-shadow:2px 2px 10px black;
}

p{
max-width:700px;
font-size:20px;
line-height:1.8;
}

button{
margin-top:40px;
padding:15px 35px;
border:none;
border-radius:50px;
font-size:18px;
background:white;
color:#ff4f81;
cursor:pointer;
font-weight:bold;
transition:.3s;
}

button:hover{
transform:scale(1.1);
}

.hearts{
position:fixed;
top:0;
left:0;
width:100%;
height:100%;
pointer-events:none;
overflow:hidden;
z-index:-1;
}

.heart{
position:absolute;
top:-30px;
color:#ff3366;
animation:fall linear forwards;
}

@keyframes fall{
0%{
transform:translateY(-10vh) rotate(0deg);
opacity:1;
}
100%{
transform:translateY(110vh) rotate(360deg);
opacity:0;
}
}
</style>

</head>

<body>

<div class="hearts"></div>

<audio autoplay loop>
<source src="a-thousand-years.mp3" type="audio/mpeg">
</audio>

<div class="page active" id="page1">
<h1>Happy Girlfriend Day ❤️</h1>

<p>
To the most beautiful girl in my life.
</p>

<button onclick="nextPage(2)">
Open My Heart ❤️
</button>

</div>

<div class="page" id="page2">

<h1>My Love ❤️</h1>

<p>
Every moment with you feels like a dream come true.
You are my happiness, my peace, and the reason I smile every day.
Thank you for always standing beside me through every joy and every challenge.
I promise to love you, respect you, and cherish every moment we spend together.
Happy Girlfriend Day, my love. ❤️
</p>

<button onclick="nextPage(3)">
Next ❤️
</button>

</div>

<div class="page" id="page3">

<h1>Thank You ❤️</h1>

<p style="font-size:30px;">
Thank you for staying with me.<br><br>
I love you soo much ❤️
</p>

</div>

<script>

function nextPage(page){

document.querySelectorAll(".page").forEach(p=>{
p.classList.remove("active");
});

document.getElementById("page"+page).classList.add("active");

}

const hearts=document.querySelector(".hearts");

function createHeart(){

const heart=document.createElement("div");

heart.classList.add("heart");

heart.innerHTML="❤️";

heart.style.left=Math.random()*100+"vw";

heart.style.fontSize=(15+Math.random()*25)+"px";

heart.style.animationDuration=(4+Math.random()*5)+"s";

hearts.appendChild(heart);

setTimeout(()=>{
heart.remove();
},9000);

}

setInterval(createHeart,250);

</script>

</body>
</html>
