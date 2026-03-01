<!DOCTYPE html>
<html>
<head>
<title>Zain ❤️ Ayesha | 5 Years</title>

<style>

body{
margin:0;
font-family: 'Arial';
background: linear-gradient(135deg,#ff416c,#ff4b2b);
color:white;
text-align:center;
overflow:hidden;
}

.container{
margin-top:80px;
}

button{
padding:15px 30px;
font-size:18px;
border:none;
border-radius:30px;
background:white;
color:#ff416c;
cursor:pointer;
transition:0.3s;
}

button:hover{
transform:scale(1.1);
}

.hidden{
display:none;
}

.heart{
position:fixed;
font-size:20px;
animation: float 6s linear infinite;
}

@keyframes float{
0%{transform:translateY(100vh)}
100%{transform:translateY(-10vh)}
}

.photo{
width:220px;
border-radius:15px;
margin:10px;
box-shadow:0 10px 20px rgba(0,0,0,0.3);
}

#message{
max-width:650px;
margin:auto;
font-size:20px;
line-height:1.7;
}

</style>
</head>

<body>

<div class="container" id="start">

<h1>Zain ❤️ Ayesha</h1>
<h2>Our 5 Year Love Journey</h2>

<p>2 March 2026</p>

<p id="countdown"></p>

<button onclick="start()">Begin Our Story ❤️</button>

</div>


<div class="container hidden" id="memory">

<h2>Our Beautiful Memories 📸</h2>

<img src="photo1.jpg" class="photo">
<img src="photo2.jpg" class="photo">
<img src="photo3.jpg" class="photo">

<br><br>

<button onclick="showMessage()">Open My Heart 💌</button>

</div>


<div class="container hidden" id="final">

<h1>❤️ Ayesha ❤️</h1>

<div id="message"></div>

</div>


<script>

function start(){
document.getElementById("start").style.display="none";
document.getElementById("memory").style.display="block";
}


function showMessage(){

document.getElementById("memory").style.display="none";
document.getElementById("final").style.display="block";

typeMessage()

}


let text = `For five beautiful years, you have been the most special part of my life.

Ayesha, you are not just my girlfriend,
you are my happiness, my peace, and my best friend.

Every moment with you became a memory I will always treasure.

No matter what happens in life,
I promise I will always choose you again and again.

Thank you for loving me,
thank you for staying with me.

Happy 5th Anniversary ❤️

Forever yours,
Zain`;

let i = 0;

function typeMessage(){

if(i < text.length){

document.getElementById("message").innerHTML += text.charAt(i);

i++;

setTimeout(typeMessage,40);

}

}


function createHeart(){

let heart = document.createElement("div");

heart.className="heart";

heart.innerHTML="❤️";

heart.style.left=Math.random()*100+"vw";

heart.style.fontSize=(10+Math.random()*30)+"px";

document.body.appendChild(heart);

setTimeout(()=>{heart.remove()},6000)

}

setInterval(createHeart,300);



let countDownDate = new Date("March 2, 2026 00:00:00").getTime();

let x = setInterval(function(){

let now = new Date().getTime();

let distance = countDownDate - now;

let hours = Math.floor((distance % (1000 * 60 * 60 * 24))/(1000*60*60));

let minutes = Math.floor((distance % (1000 * 60 * 60))/(1000*60));

let seconds = Math.floor((distance % (1000 * 60))/1000);

document.getElementById("countdown").innerHTML =
hours + "h " + minutes + "m " + seconds + "s until our anniversary ❤️";

},1000);

</script>

</body>
</html>
