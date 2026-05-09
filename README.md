<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Anime Birthday Surprise</title>

<style>

body{
    margin:0;
    padding:0;
    overflow:hidden;
    background:linear-gradient(to bottom,#000428,#004e92);
    font-family:Arial,sans-serif;
    color:white;
    text-align:center;
}

/* Thunder Flash */

.flash{
    position:fixed;
    top:0;
    left:0;
    width:100%;
    height:100%;
    background:white;
    opacity:0;
    pointer-events:none;
    z-index:999;
}

.flash.active{
    animation:thunderFlash 0.7s ease;
}

@keyframes thunderFlash{

    0%{opacity:0;}

    20%{opacity:1;}

    40%{opacity:0.2;}

    60%{opacity:1;}

    100%{opacity:0;}
}

/* Birthday Background */

.party-bg{
    position:fixed;
    top:0;
    left:0;
    width:100%;
    height:100%;
    overflow:hidden;
    z-index:-1;
}

.party{
    position:absolute;
    bottom:-120px;
    font-size:40px;
    animation:partyUp linear infinite;
    opacity:0.9;
}

@keyframes partyUp{

    0%{
        transform:translateY(0) rotate(0deg);
        opacity:1;
    }

    100%{
        transform:translateY(-120vh) rotate(360deg);
        opacity:0;
    }
}

.container{
    min-height:100vh;
    padding:30px;
}

h1{
    font-size:45px;
    margin-top:100px;
    animation:glow 2s infinite alternate;
}

.hidden{
    display:none;
}

button{
    padding:15px 35px;
    font-size:22px;
    border:none;
    border-radius:15px;
    background:gold;
    cursor:pointer;
    margin-top:20px;
    transition:0.3s;
    font-weight:bold;
}

button:hover{
    transform:scale(1.08);
}

.invitation{
    background:rgba(255,255,255,0.12);
    padding:25px;
    border-radius:20px;
    backdrop-filter:blur(5px);
    animation:popup 1s ease;
    margin-top:20px;
}

.character-card{
    background:rgba(255,255,255,0.12);
    border-radius:20px;
    padding:20px;
    margin:25px auto;
    width:90%;
    max-width:500px;
    animation:popup 1.5s ease;
    box-shadow:0 0 20px rgba(255,255,255,0.2);
}

.quote{
    margin-top:15px;
    font-size:20px;
    color:gold;
    font-style:italic;
}

.cake{
    font-size:120px;
    animation:bounce 1s infinite alternate;
}

.balloon{
    position:absolute;
    font-size:60px;
    animation:float 6s linear infinite;
}

@keyframes glow{

    from{
        text-shadow:0 0 10px cyan;
    }

    to{
        text-shadow:0 0 30px yellow;
    }
}

@keyframes popup{

    from{
        opacity:0;
        transform:scale(0);
    }

    to{
        opacity:1;
        transform:scale(1);
    }
}

@keyframes bounce{

    from{
        transform:translateY(0px);
    }

    to{
        transform:translateY(-20px);
    }
}

@keyframes float{

    from{
        transform:translateY(100vh);
    }

    to{
        transform:translateY(-120vh);
    }
}

</style>
</head>

<body>

<div class="flash" id="flash"></div>

<div class="party-bg" id="partyBg"></div>

<div class="container">

<h1 id="mainText">
    ⚡ Touch Anywhere For Birthday Surprise ⚡
</h1>

<div id="surpriseSection" class="hidden">

    <div class="cake">🎂</div>

    <div class="invitation">

        <h2>💌 Birthday Invitation 💌</h2>

        <p>
            Happy Birthday Bro ❤️
            <br><br>
            Welcome to your Anime Birthday Celebration!
        </p>

        <button onclick="showGift()">
            🎁 Open Surprise Gift
        </button>

    </div>

    <div id="giftSection" class="hidden">

        <!-- Akaza -->
        <div class="character-card">
            <h2>🔥 Akaza</h2>
            <div class="quote">
                “Become stronger.”
            </div>
        </div>

        <!-- Rengoku -->
        <div class="character-card">
            <h2>🔥 Rengoku</h2>
            <div class="quote">
                “Set your heart ablaze!”
            </div>
        </div>

        <!-- Kira -->
        <div class="character-card">
            <h2>✨ Kira</h2>
            <div class="quote">
                “Silence reveals true power.”
            </div>
        </div>

        <!-- Licht -->
        <div class="character-card">
            <h2>⚡ Licht</h2>
            <div class="quote">
                “Hope will never disappear.”
            </div>
        </div>

        <!-- William -->
        <div class="character-card">
            <h2>🌳 William Vangeance</h2>
            <div class="quote">
                “Hatred only gives birth to more hatred.”
            </div>
        </div>

        <!-- Detective L -->
        <div class="character-card">
            <h2>🕵️ Detective L</h2>
            <div class="quote">
                “There are many types of monsters in this world.”
            </div>
        </div>

        <!-- Yami -->
        <div class="character-card">
            <h2>⚔️ Yami Sukehiro</h2>
            <div class="quote">
                “Surpass your limits. Right here. Right now.”
            </div>
        </div>

        <!-- Obanai -->
        <div class="character-card">
            <h2>🐍 Obanai Iguro</h2>
            <div class="quote">
                “Those who are weak have no rights.”
            </div>
        </div>

        <!-- Shinobu -->
        <div class="character-card">
            <h2>🦋 Shinobu Kocho</h2>
            <div class="quote">
                “Humans should help each other.”
            </div>
        </div>

        <!-- Giyu -->
        <div class="character-card">
            <h2>🌊 Giyu Tomioka</h2>
            <div class="quote">
                “Do not cry. Do not despair.”
            </div>
        </div>

        <!-- Hinata -->
        <div class="character-card">
            <h2>🏐 Hinata Shoyo</h2>
            <div class="quote">
                “The future belongs to those who believe in themselves.”
            </div>
        </div>

        <div class="invitation">

            <h2>🎉 Final Birthday Message 🎉</h2>

            <p>
                Your sibling prepared this special anime surprise just for you ❤️
                <br><br>
                Wishing you happiness, strength,
                success and unlimited anime power ⚔️🔥
            </p>

        </div>

    </div>

</div>

</div>

<script>

/* Thunder Transition */

document.body.addEventListener("click", function(){

    const flash =
        document.getElementById("flash");

    flash.classList.add("active");

    setTimeout(() => {

        document.getElementById("mainText")
            .style.display = "none";

        document.getElementById("surpriseSection")
            .classList.remove("hidden");

        createBalloons();

    }, 700);

}, {once:true});

/* Show Gift */

function showGift(){

    document.getElementById("giftSection")
        .classList.remove("hidden");
}

/* Balloons */

function createBalloons(){

    for(let i=0;i<25;i++){

        let balloon = document.createElement("div");

        balloon.classList.add("balloon");

        balloon.innerHTML = "🎈";

        balloon.style.left =
            Math.random()*100 + "vw";

        balloon.style.animationDuration =
            (3 + Math.random()*5) + "s";

        balloon.style.fontSize =
            (40 + Math.random()*40) + "px";

        document.body.appendChild(balloon);
    }
}

/* Birthday Particles */

createParty();

function createParty(){

    const partyBg =
        document.getElementById("partyBg");

    for(let i=0;i<50;i++){

        let party = document.createElement("div");

        party.classList.add("party");

        party.innerHTML = "🎉";

        party.style.left =
            Math.random()*100 + "vw";

        party.style.animationDuration =
            (3 + Math.random()*4) + "s";

        party.style.animationDelay =
            Math.random()*5 + "s";

        party.style.fontSize =
            (25 + Math.random()*40) + "px";

        partyBg.appendChild(party);
    }
}

</script>

</body>
</html>
