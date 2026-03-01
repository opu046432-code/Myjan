<!DOCTYPE html>
<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Happy Birthday My Love 💖</title>

<style>
body{
    margin:0;
    font-family:'Segoe UI', sans-serif;
    text-align:center;
    background: linear-gradient(135deg,#ff4e88,#ff004f,#ff6fa5);
    background-size:400% 400%;
    animation:bgMove 8s ease infinite;
    color:white;
    overflow:hidden;
}

@keyframes bgMove{
    0%{background-position:0% 50%;}
    50%{background-position:100% 50%;}
    100%{background-position:0% 50%;}
}

.page{
    display:none;
    padding:20px;
    min-height:100vh;
    animation:fadePage 1s;
}

.active{display:block;}

@keyframes fadePage{
    from{opacity:0;}
    to{opacity:1;}
}

h1,h2{
    text-shadow:0 0 15px rgba(255,255,255,0.8);
}

button{
    padding:12px 25px;
    border:none;
    border-radius:30px;
    font-size:18px;
    margin:10px;
    cursor:pointer;
    transition:0.3s;
    box-shadow:0 0 15px rgba(255,255,255,0.5);
}

button:hover{
    transform:scale(1.1);
}

.yes{background:white;color:#ff004f;}
.no{background:black;color:white;position:absolute;}

.typing{
    text-align:left;
    max-width:500px;
    margin:auto;
    line-height:1.6;
}

.slider{
    position:relative;
    max-width:300px;
    margin:auto;
}

.slide{
    width:100%;
    border-radius:15px;
    display:none;
    box-shadow:0 0 20px rgba(255,255,255,0.7);
}

.activeSlide{
    display:block;
    animation:fadePage 1.5s;
}

img{
    width:90%;
    max-width:300px;
    border-radius:15px;
    margin:10px;
}

.giftImg{
    animation:bounce 1.5s infinite alternate;
    box-shadow:0 0 25px gold;
}

@keyframes bounce{
    from{transform:translateY(0);}
    to{transform:translateY(-20px);}
}

.heart{
    position:fixed;
    bottom:-10px;
    font-size:20px;
    animation:floatUp 5s linear infinite;
}

@keyframes floatUp{
    from{transform:translateY(0);opacity:1;}
    to{transform:translateY(-800px);opacity:0;}
}
</style>
</head>

<body>

<!-- 🎵 Background Music -->
<audio id="bgMusic" autoplay loop>
    <source src="love.mp3" type="audio/mpeg">
</audio>

<!-- Page 1 -->
<div class="page active" id="page1">
    <h1>Do You Love Me? ❤️</h1>
    <button class="yes" onclick="nextPage(2)">Yes</button>
    <button class="no" id="noBtn">No</button>
</div>

<!-- Page 2 -->
<div class="page" id="page2">
    <h2>Happy Birthday My Love 🎂</h2>

    <div class="typing">
        <p><b>প্রিয় জান,</b></p>
        <p>শুভ জন্মদিন আমার ভালোবাসা। 🎂💖</p>
        <p>
        আজকের এই বিশেষ দিনে আমি শুধু একটা কথাই বলতে চাই — তুমি আমার জীবনের সবচেয়ে সুন্দর প্রাপ্তি।
        তিন বছরেরও বেশি সময় ধরে আমরা একসাথে আছি। এই সময়টায় রাগ ছিল, অভিমান ছিল, ভুল বোঝাবুঝি ছিল…
        কিন্তু সব কিছুর মাঝেও আমাদের ভালোবাসাটা কখনো কমে যায়নি। বরং আরও গভীর হয়েছে।
        </p>
        <p>
        আমি জানি, এতদিনে তোমাকে ঠিকভাবে বড় কোনো গিফট দিতে পারিনি।
        তোমার প্রাপ্যটা সবসময় দিতে পারিনি। কিন্তু বিশ্বাস করো,
        আমার মন থেকে তোমার জন্য ভালোবাসা আর সম্মান কখনো কম ছিল না।
        </p>
        <p>
        আমাদের সম্পর্কটা শুধু আজকের না — এটা আমাদের ভবিষ্যতেরও।
        আমরা একসাথে পূর্ণতা পাবো, রাগ করবো, অভিমান করবো, আবার জড়িয়ে ধরবো।
        </p>
        <p>
        আল্লাহর কাছে শুধু এই দোয়া করি — তোমার জীবন সুখে, স্বাস্থ্যে আর সফলতায় ভরে উঠুক।
        </p>
        <p><b>শুভ জন্মদিন আমার জান ❤️</b></p>
        <p><b>— তোমার জামাই 💍❤️</b></p>
    </div>

    <br>
    <button onclick="nextPage(3)">Next</button>
</div>

<!-- Page 3 -->
<div class="page" id="page3">
    <h2>Choose One 💕</h2>
    <button onclick="nextPage(4)">Memories</button>
    <button onclick="nextPage(5)">Gift</button>
</div>

<!-- Page 4 -->
<div class="page" id="page4">
    <h2>Our Memories 📸</h2>
    <div class="slider">
        <img class="slide activeSlide" src="photo1.jpg">
        <img class="slide" src="photo2.jpg">
        <img class="slide" src="photo3.jpg">
    </div>
    <button onclick="nextPage(3)">Back</button>
</div>

<!-- Page 5 -->
<div class="page" id="page5">
    <h2>Your Special Gift 🎁</h2>
    <img class="giftImg" src="gift.jpg">
    <button onclick="nextPage(3)">Back</button>
</div>

<script>
function nextPage(page){
    document.querySelectorAll(".page").forEach(p=>p.classList.remove("active"));
    document.getElementById("page"+page).classList.add("active");
}

/* No Button Move */
let noBtn=document.getElementById("noBtn");
function moveButton(){
    let x=Math.random()*(window.innerWidth-100);
    let y=Math.random()*(window.innerHeight-50);
    noBtn.style.left=x+"px";
    noBtn.style.top=y+"px";
}
noBtn.addEventListener("mouseover",moveButton);
noBtn.addEventListener("click",moveButton);

/* Floating Hearts */
setInterval(()=>{
    let heart=document.createElement("div");
    heart.className="heart";
    heart.innerHTML="❤️";
    heart.style.left=Math.random()*100+"vw";
    heart.style.fontSize=(Math.random()*20+10)+"px";
    document.body.appendChild(heart);
    setTimeout(()=>heart.remove(),5000);
},500);

/* Auto Slider */
let slides=document.querySelectorAll(".slide");
let current=0;
setInterval(()=>{
    slides[current].classList.remove("activeSlide");
    current=(current+1)%slides.length;
    slides[current].classList.add("activeSlide");
},2500);
</script>

</body>
</html>
