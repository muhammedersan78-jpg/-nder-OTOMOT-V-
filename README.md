<!DOCTYPE html>
<html lang="tr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Şevnur İçin ❤️</title>

<link href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@600&family=Poppins:wght@300;500&display=swap" rel="stylesheet">

<style>

*{
margin:0;
padding:0;
box-sizing:border-box;
}

body{
font-family:Poppins;
background: linear-gradient(120deg,#ff5f8f,#ffb6c1,#ffc0cb);
height:100vh;
overflow-x:hidden;
color:white;
}

/* NAVBAR */

nav{
position:fixed;
top:0;
width:100%;
display:flex;
justify-content:center;
padding:20px;
background:rgba(0,0,0,0.2);
backdrop-filter:blur(10px);
}

nav h2{
font-family:"Dancing Script";
font-size:30px;
}

/* HERO */

.hero{
height:100vh;
display:flex;
flex-direction:column;
justify-content:center;
align-items:center;
text-align:center;
padding:20px;
}

.hero h1{
font-family:"Dancing Script";
font-size:70px;
margin-bottom:20px;
animation:fadeIn 3s ease;
}

.hero p{
font-size:20px;
max-width:600px;
line-height:1.7;
}

button{
margin-top:30px;
padding:15px 35px;
font-size:18px;
border:none;
border-radius:40px;
background:white;
color:#ff4d7a;
cursor:pointer;
transition:0.3s;
}

button:hover{
transform:scale(1.1);
}

/* MESSAGE */

.message{
margin-top:30px;
display:none;
font-size:22px;
font-family:"Dancing Script";
}

/* PHOTO */

.gallery{
display:flex;
justify-content:center;
margin-top:80px;
}

.photo{
width:250px;
height:300px;
background:white;
border-radius:20px;
overflow:hidden;
box-shadow:0 10px 30px rgba(0,0,0,0.3);
}

.photo img{
width:100%;
height:100%;
object-fit:cover;
}

/* HEARTS */

.heart{
position:absolute;
color:white;
font-size:20px;
animation:fall linear forwards;
}

@keyframes fall{

0%{
transform:translateY(-100px);
opacity:1;
}

100%{
transform:translateY(110vh);
opacity:0;
}

}

@keyframes fadeIn{

0%{
opacity:0;
transform:translateY(30px);
}

100%{
opacity:1;
transform:translateY(0);
}

}

footer{
margin-top:100px;
text-align:center;
padding:30px;
font-size:18px;
}

</style>

</head>

<body>

<nav>
<h2>Şevnur ❤️</h2>
</nav>

<section class="hero">

<h1>Şevnur Eren</h1>

<p>

Bilmiyorum bunu okurken ne hissedeceksin ama  
bildiğim tek şey şu...

Seni tanıdığımdan beri hayatım biraz daha güzel.  
Belki sadece bir insan için fazla romantik geliyor olabilir ama  
ben gerçekten sana karşı hissettiklerimi saklamak istemiyorum.

</p>

<button onclick="showLove()">Bir Mesajım Var</button>

<div class="message" id="loveMessage">

Şevnur...  
Eğer bir gün gökyüzüne bakıp gülümsersen  
bil ki bir yerde seni düşünen biri var.

Belki hayat uzun bir yol  
ama ben o yolda seninle yürümeyi isterdim. ❤️

</div>

</section>

<div class="gallery">

<div class="photo">
<img src="https://picsum.photos/400/500" alt="photo">
</div>

</div>

<footer>

Bu site sadece bir kişi için yapıldı...  
Şevnur için ❤️

</footer>

<script>

function showLove(){
document.getElementById("loveMessage").style.display="block";
}

function createHeart(){

const heart=document.createElement("div");

heart.className="heart";
heart.innerHTML="❤";

heart.style.left=Math.random()*100+"vw";
heart.style.fontSize=(10+Math.random()*25)+"px";

heart.style.animationDuration=(4+Math.random()*3)+"s";

document.body.appendChild(heart);

setTimeout(()=>{
heart.remove();
},7000)

}

setInterval(createHeart,300)

</script>

</body>
</html>
