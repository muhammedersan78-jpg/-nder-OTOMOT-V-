<!DOCTYPE html>
<html lang="tr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Şevnur İçin</title>

<style>
body{
    margin:0;
    font-family: Arial, sans-serif;
    background: linear-gradient(135deg,#ff4e8a,#ff9ecf);
    height:100vh;
    display:flex;
    justify-content:center;
    align-items:center;
    text-align:center;
    color:white;
    overflow:hidden;
}

.container{
    background: rgba(0,0,0,0.3);
    padding:40px;
    border-radius:20px;
    backdrop-filter: blur(10px);
}

h1{
    font-size:40px;
}

p{
    font-size:20px;
}

button{
    margin-top:20px;
    padding:15px 30px;
    font-size:18px;
    border:none;
    border-radius:30px;
    background:white;
    color:#ff4e8a;
    cursor:pointer;
    transition:0.3s;
}

button:hover{
    transform:scale(1.1);
}

.heart{
    position:absolute;
    color:white;
    font-size:20px;
    animation: fall 6s linear infinite;
}

@keyframes fall{
    0%{
        transform:translateY(-100px);
        opacity:1;
    }
    100%{
        transform:translateY(100vh);
        opacity:0;
    }
}

#message{
    margin-top:20px;
    font-size:22px;
    display:none;
}
</style>
</head>

<body>

<div class="container">
<h1>Şevnur ❤️</h1>

<p>
Şevnur Eren...  
Bu site sadece senin için yapıldı.
</p>

<button onclick="showMessage()">Tıkla</button>

<p id="message">
Seni tanıdığım günden beri dünyam daha güzel.  
Belki bilmiyorsun ama sen benim için çok özelsin. ❤️
</p>

</div>

<script>

function showMessage(){
document.getElementById("message").style.display="block";
}

function createHeart(){
const heart=document.createElement("div");
heart.classList.add("heart");
heart.innerHTML="❤";
heart.style.left=Math.random()*100+"vw";
heart.style.fontSize=(10+Math.random()*20)+"px";
heart.style.animationDuration=(3+Math.random()*3)+"s";
document.body.appendChild(heart);

setTimeout(()=>{
heart.remove();
},6000);
}

setInterval(createHeart,300);

</script>

</body>
</html>
