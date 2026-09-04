<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>EUROPA CARDS</title>

<style>
:root{
    --blue:#159cff;
    --dark:#050814;
    --panel:#0b1020;
    --green:#38e56d;
    --gold:#ffc928;
    --purple:#a84dff;
    --orange:#ff861c;
}

*{
    box-sizing:border-box;
}

body{
    margin:0;
    font-family:Arial,Helvetica,sans-serif;
    background:
        radial-gradient(circle at top,#102b55 0%,#050814 45%,#02030a 100%);
    color:white;
    min-height:100vh;
}

button{
    font:inherit;
    cursor:pointer;
}

.hidden{
    display:none !important;
}

/* ================= HEADER ================= */

header{
    padding:18px;
    text-align:center;
    border-bottom:1px solid #17345c;
    background:rgba(4,8,20,.9);
    position:sticky;
    top:0;
    z-index:50;
}

.logo{
    font-size:clamp(35px,8vw,75px);
    font-weight:900;
    letter-spacing:3px;
    margin:0;
    background:linear-gradient(#fff,#a7c9ff);
    color:transparent;
    background-clip:text;
    -webkit-background-clip:text;
    text-shadow:0 0 30px rgba(21,156,255,.35);
}

.subtitle{
    color:#75bfff;
    letter-spacing:4px;
    margin-top:-5px;
    font-weight:bold;
}

.stats{
    margin-top:15px;
    display:flex;
    justify-content:center;
    gap:10px;
    flex-wrap:wrap;
}

.stat{
    background:#101a30;
    border:1px solid #244e82;
    padding:9px 15px;
    border-radius:12px;
    font-weight:bold;
}

/* ================= NAV ================= */

nav{
    display:flex;
    justify-content:center;
    gap:8px;
    flex-wrap:wrap;
    padding:15px;
    background:#07101f;
}

.nav-btn{
    background:#101d35;
    border:1px solid #234a7b;
    color:white;
    padding:10px 14px;
    border-radius:10px;
}

.nav-btn:hover{
    background:#16365f;
}

/* ================= MAIN ================= */

main{
    max-width:1250px;
    margin:auto;
    padding:20px;
}

.page{
    display:none;
}

.page.active{
    display:block;
}

.title{
    text-align:center;
    color:#7cc6ff;
    margin-bottom:25px;
}

/* ================= BUTTON ================= */

.big-btn{
    padding:14px 22px;
    border:none;
    border-radius:12px;
    font-weight:bold;
    color:white;
    background:linear-gradient(135deg,#167de0,#36b6ff);
    box-shadow:0 0 20px rgba(21,156,255,.3);
}

.big-btn:hover{
    transform:scale(1.03);
}

.green-btn{
    background:linear-gradient(135deg,#159e4b,#46e87a);
}

.gold-btn{
    background:linear-gradient(135deg,#b77900,#ffd84a);
    color:#161000;
}

.danger-btn{
    background:#b32626;
}

/* ================= HOME ================= */

.home-grid{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(230px,1fr));
    gap:16px;
}

.home-card{
    background:linear-gradient(145deg,#0d1830,#080d1b);
    border:1px solid #1b4c80;
    border-radius:18px;
    padding:25px;
    text-align:center;
    transition:.2s;
}

.home-card:hover{
    transform:translateY(-5px);
    border-color:#40b5ff;
}

.home-icon{
    font-size:50px;
}

.home-card h2{
    color:#75c7ff;
}

/* ================= CARDS ================= */

.cards-grid{
    display:grid;
    grid-template-columns:repeat(auto-fill,minmax(150px,1fr));
    gap:16px;
}

.card{
    min-height:240px;
    padding:10px;
    border-radius:14px;
    position:relative;
    display:flex;
    flex-direction:column;
    justify-content:space-between;
    overflow:hidden;
    border:3px solid #777;
    background:linear-gradient(145deg,#20242e,#090b11);
    box-shadow:0 10px 25px rgba(0,0,0,.5);
}

.card.common{
    border-color:#8c929b;
}

.card.rare{
    border-color:#289cff;
    box-shadow:0 0 20px rgba(40,156,255,.35);
}

.card.epic{
    border-color:#a84dff;
    box-shadow:0 0 20px rgba(168,77,255,.35);
}

.card.legendary{
    border-color:#ff9b22;
    box-shadow:0 0 25px rgba(255,155,34,.4);
}

.card.goat{
    border-color:#ffd43d;
    box-shadow:0 0 30px rgba(255,212,61,.6);
    background:linear-gradient(145deg,#362b08,#100d02);
}

.card-rarity{
    text-align:center;
    font-size:12px;
    font-weight:bold;
    letter-spacing:1px;
}

.card-art{
    height:120px;
    border-radius:10px;
    display:flex;
    align-items:center;
    justify-content:center;
    font-size:65px;
    background:rgba(0,0,0,.3);
}

.card-name{
    text-align:center;
    font-weight:bold;
    font-size:18px;
}

.card-stats{
    display:flex;
    justify-content:space-around;
    font-size:13px;
    margin-top:8px;
}

.card-actions{
    margin-top:8px;
}

.card-actions button{
    width:100%;
    padding:7px;
    background:#123762;
    border:1px solid #329fff;
    color:white;
    border-radius:7px;
}

/* ================= PACKS ================= */

.pack-grid{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(210px,1fr));
    gap:20px;
}

.pack{
    border-radius:18px;
    padding:18px;
    text-align:center;
    border:1px solid #285c95;
    background:#0b1325;
}

.pack-art{
    height:220px;
    display:flex;
    align-items:center;
    justify-content:center;
    font-size:80px;
    border-radius:15px;
    margin-bottom:15px;
}

.classic{background:linear-gradient(135deg,#094d89,#1da9ff);}
.halloween{background:linear-gradient(135deg,#2b0b47,#8c24e8);}
.christmas{background:linear-gradient(135deg,#a01818,#f5f5f5);}
.summer{background:linear-gradient(135deg,#ffb300,#ffe763);}

/* ================= OPEN PACK ================= */

.open-area{
    text-align:center;
}

.opened-cards{
    display:flex;
    gap:15px;
    justify-content:center;
    flex-wrap:wrap;
    margin-top:25px;
}

.pack-opening{
    animation:openPack 1s infinite alternate;
}

@keyframes openPack{
    from{transform:scale(1) rotate(-2deg);}
    to{transform:scale(1.08) rotate(2deg);}
}

/* ================= BATTLE ================= */

.battle-board{
    display:grid;
    grid-template-columns:1fr auto 1fr;
    gap:20px;
    align-items:center;
    text-align:center;
}

.fighter{
    background:#0c1528;
    border:1px solid #24588d;
    padding:20px;
    border-radius:16px;
}

.hp-bar{
    width:100%;
    height:20px;
    background:#2a1010;
    border-radius:10px;
    overflow:hidden;
    margin:10px 0;
}

.hp-fill{
    height:100%;
    background:linear-gradient(90deg,#ef3131,#ff7b7b);
    width:100%;
    transition:.4s;
}

.battle-log{
    margin-top:20px;
    background:#080d18;
    border:1px solid #203b5c;
    border-radius:12px;
    padding:15px;
    min-height:100px;
}

/* ================= DECK ================= */

.deck-slots{
    display:grid;
    grid-template-columns:repeat(5,1fr);
    gap:10px;
    margin-bottom:20px;
}

.slot{
    min-height:120px;
    background:#070b14;
    border:2px dashed #28496e;
    border-radius:10px;
    display:flex;
    align-items:center;
    justify-content:center;
    text-align:center;
    padding:5px;
}

.slot.filled{
    border-style:solid;
    border-color:#35a8ff;
}

/* ================= MODAL ================= */

.modal{
    position:fixed;
    inset:0;
    background:rgba(0,0,0,.82);
    z-index:100;
    display:flex;
    justify-content:center;
    align-items:center;
    padding:20px;
}

.modal-box{
    max-width:650px;
    width:100%;
    max-height:90vh;
    overflow:auto;
    background:#091120;
    border:1px solid #319eff;
    border-radius:20px;
    padding:25px;
    text-align:center;
}

/* ================= TUTORIAL ================= */

.tutorial-step{
    display:none;
}

.tutorial-step.active{
    display:block;
}

.tutorial-icon{
    font-size:80px;
}

/* ================= SUCCESS ================= */

.success{
    background:#0b1425;
    border:1px solid #26496d;
    border-radius:12px;
    padding:15px;
    margin:10px 0;
}

.success.unlocked{
    border-color:#ffd43d;
    box-shadow:0 0 15px rgba(255,212,61,.25);
}

/* ================= BOSS ================= */

.boss-box{
    background:linear-gradient(145deg,#320707,#120305);
    border:2px solid #b51e1e;
    border-radius:20px;
    padding:25px;
    text-align:center;
}

.boss-icon{
    font-size:90px;
}

/* ================= TOAST ================= */

#toast{
    position:fixed;
    bottom:20px;
    left:50%;
    transform:translateX(-50%);
    background:#10243e;
    border:1px solid #38a9ff;
    padding:12px 20px;
    border-radius:12px;
    display:none;
    z-index:300;
}

/* MOBILE */

@media(max-width:700px){
    .battle-board{
        grid-template-columns:1fr;
    }

    .deck-slots{
        grid-template-columns:repeat(2,1fr);
    }
}
</style>
</head>

<body>

<header>

<h1 class="logo">EUROPA</h1>
<div class="subtitle">CARDS</div>

<div class="stats">
    <div class="stat">🟢 <span id="coins">1000</span> EURO Coins</div>
    <div class="stat">⭐ Niveau <span id="level">1</span></div>
    <div class="stat">🎴 <span id="collectionCount">0</span> cartes</div>
</div>

</header>

<nav>
    <button class="nav-btn" onclick="showPage('home')">🏠 Accueil</button>
    <button class="nav-btn" onclick="showPage('packs')">📦 Boosters</button>
    <button class="nav-btn" onclick="showPage('collection')">🎴 Collection</button>
    <button class="nav-btn" onclick="showPage('deck')">🃏 Deck</button>
    <button class="nav-btn" onclick="showPage('battle')">⚔️ Combat</button>
    <button class="nav-btn" onclick="showPage('boss')">😈 Boss</button>
    <button class="nav-btn" onclick="showPage('success')">🏆 Succès</button>
</nav>

<main>

<!-- HOME -->

<section id="home" class="page active">

<h1 class="title">BIENVENUE DANS EUROPA CARDS</h1>

<div class="home-grid">

<div class="home-card">
<div class="home-icon">📦</div>
<h2>BOOSTERS</h2>
<p>Ouvre des packs et découvre de nouvelles cartes.</p>
<button class="big-btn" onclick="showPage('packs')">VOIR LES PACKS</button>
</div>

<div class="home-card">
<div class="home-icon">🎴</div>
<h2>COLLECTION</h2>
<p>Collectionne les cartes EUROPA et complète ta collection.</p>
<button class="big-btn" onclick="showPage('collection')">MA COLLECTION</button>
</div>

<div class="home-card">
<div class="home-icon">🃏</div>
<h2>MON DECK</h2>
<p>Choisis jusqu'à 10 cartes pour combattre.</p>
<button class="big-btn" onclick="showPage('deck')">CRÉER MON DECK</button>
</div>

<div class="home-card">
<div class="home-icon">⚔️</div>
<h2>COMBAT IA</h2>
<p>Affronte une intelligence artificielle.</p>
<button class="big-btn" onclick="showPage('battle')">COMBATTRE</button>
</div>

<div class="home-card">
<div class="home-icon">😈</div>
<h2>LE BOSS</h2>
<p>Affronte des Boss puissants pour gagner des récompenses.</p>
<button class="big-btn danger-btn" onclick="showPage('boss')">AFFRONTER</button>
</div>

<div class="home-card">
<div class="home-icon">🏆</div>
<h2>SUCCÈS</h2>
<p>Débloque des récompenses et deviens une légende.</p>
<button class="big-btn gold-btn" onclick="showPage('success')">MES SUCCÈS</button>
</div>

</div>

</section>

<!-- PACKS -->

<section id="packs" class="page">

<h1 class="title">📦 BOOSTERS EUROPA</h1>

<div class="pack-grid">

<div class="pack">
<div class="pack-art classic">📦</div>
<h2>BOOSTER CLASSIQUE</h2>
<p>5 cartes</p>
<p>💰 250 EURO Coins</p>
<button class="big-btn" onclick="buyPack('classic',250)">ACHETER</button>
</div>

<div class="pack">
<div class="pack-art halloween">🎃</div>
<h2>PACK HALLOWEEN</h2>
<p>5 cartes événement</p>
<p>💰 400 EURO Coins</p>
<button class="big-btn" onclick="buyPack('halloween',400)">ACHETER</button>
</div>

<div class="pack">
<div class="pack-art christmas">🎄</div>
<h2>PACK NOËL</h2>
<p>5 cartes exclusives</p>
<p>💰 400 EURO Coins</p>
<button class="big-btn" onclick="buyPack('christmas',400)">ACHETER</button>
</div>

<div class="pack">
<div class="pack-art summer">☀️</div>
<h2>PACK ÉTÉ</h2>
<p>5 cartes exclusives</p>
<p>💰 400 EURO Coins</p>
<button class="big-btn" onclick="buyPack('summer',400)">ACHETER</button>
</div>

</div>

<div id="openingArea" class="open-area hidden">
<h2 id="openingTitle">OUVERTURE DU BOOSTER</h2>
<div id="openedCards" class="opened-cards"></div>
<br>
<button class="big-btn" onclick="closeOpening()">CONTINUER</button>
</div>

</section>

<!-- COLLECTION -->

<section id="collection" class="page">

<h1 class="title">📚 MA COLLECTION</h1>

<p id="collectionStats" style="text-align:center"></p>

<div id="collectionGrid" class="cards-grid"></div>

</section>

<!-- DECK -->

<section id="deck" class="page">

<h1 class="title">🃏 MON DECK</h1>

<p style="text-align:center">
Choisis maximum 10 cartes.
</p>

<div class="deck-slots" id="deckSlots"></div>

<h2 class="title">MES CARTES</h2>

<div id="deckCards" class="cards-grid"></div>

</section>

<!-- BATTLE -->

<section id="battle" class="page">

<h1 class="title">⚔️ COMBAT CONTRE L'IA</h1>

<div id="battleStart">

<p style="text-align:center">
Ton deck doit contenir au moins une carte.
</p>

<div style="text-align:center">
<button class="big-btn" onclick="startBattle()">COMMENCER LE COMBAT</button>
</div>

</div>

<div id="battleGame" class="hidden">

<div class="battle-board">

<div class="fighter">
<h2>👤 TOI</h2>
<div>❤️ PV : <span id="playerHP">500</span></div>
<div class="hp-bar">
<div id="playerHPBar" class="hp-fill"></div>
</div>
<div id="playerCardName">Aucune carte</div>
</div>

<div>
<h1>VS</h1>
</div>

<div class="fighter">
<h2>🤖 IA EUROPA</h2>
<div>❤️ PV : <span id="enemyHP">500</span></div>
<div class="hp-bar">
<div id="enemyHPBar" class="hp-fill"></div>
</div>
<div>🤖 IA Niveau <span id="aiLevel">1</span></div>
</div>

</div>

<div style="text-align:center;margin-top:20px">
<button class="big-btn" onclick="attack()">⚔️ ATTAQUER</button>
</div>

<div id="battleLog" class="battle-log">
Le combat va commencer...
</div>

</div>

</section>

<!-- BOSS -->

<section id="boss" class="page">

<h1 class="title">😈 MODE BOSS</h1>

<div class="boss-box">

<div class="boss-icon">😈</div>

<h2>LE BOSS EUROPA</h2>

<p>Un adversaire puissant attend les plus grands joueurs.</p>

<div class="stats">
<div class="stat">🟢 FACILE — 500 PV</div>
<div class="stat">🟣 DIFFICILE — 1500 PV</div>
<div class="stat">👑 GOAT — 5000 PV</div>
</div>

<br>

<button class="big-btn green-btn" onclick="startBoss(500,100)">
BOSS FACILE
</button>

<button class="big-btn" onclick="startBoss(1500,300)">
BOSS DIFFICILE
</button>

<button class="big-btn gold-btn" onclick="startBoss(5000,1000)">
BOSS GOAT
</button>

</div>

</section>

<!-- SUCCESS -->

<section id="success" class="page">

<h1 class="title">🏆 MES SUCCÈS</h1>

<div id="successList"></div>

</section>

</main>

<!-- TUTORIAL -->

<div id="tutorial" class="modal hidden">

<div class="modal-box">

<div class="tutorial-step active">

<div class="tutorial-icon">👋</div>

<h1>BIENVENUE !</h1>

<p>
Bienvenue dans EUROPA CARDS !
Tu vas collectionner des cartes, créer ton deck
et devenir une légende.
</p>

<button class="big-btn" onclick="nextTutorial()">SUIVANT</button>

</div>

<div class="tutorial-step">

<div class="tutorial-icon">🎴</div>

<h1>LES CARTES</h1>

<p>
Tu peux obtenir des cartes de différentes raretés :
Commun, Rare, Épique, Légendaire et GOAT.
</p>

<button class="big-btn" onclick="nextTutorial()">SUIVANT</button>

</div>

<div class="tutorial-step">

<div class="tutorial-icon">📦</div>

<h1>LES BOOSTERS</h1>

<p>
Ouvre des boosters pour agrandir ta collection.
</p>

<button class="big-btn" onclick="nextTutorial()">SUIVANT</button>

</div>

<div class="tutorial-step">

<div class="tutorial-icon">⚔️</div>

<h1>LES COMBATS</h1>

<p>
Crée ton deck puis affronte l'IA EUROPA.
</p>

<button class="big-btn" onclick="nextTutorial()">SUIVANT</button>

</div>

<div class="tutorial-step">

<div class="tutorial-icon">🎁</div>

<h1>TON BOOSTER GRATUIT !</h1>

<p>
Pour commencer ton aventure, EUROPA t'offre
ton premier booster !
</p>

<button class="big-btn gold-btn" onclick="finishTutorial()">
OUVRIR MON BOOSTER 🎁
</button>

</div>

</div>

</div>

<div id="toast"></div>

<script>

/* =====================================================
   EUROPA CARDS
   VERSION 1
===================================================== */

const cards = [

/* JOUEURS */

{
id:"mzo_common",
name:"MZO",
rarity:"common",
icon:"👤",
attack:50,
defense:30,
hp:80,
type:"player"
},

{
id:"mzo_rare",
name:"MZO",
rarity:"rare",
icon:"🔥",
attack:75,
defense:50,
hp:110,
type:"player"
},

{
id:"mzo_goat",
name:"MZO GOAT",
rarity:"goat",
icon:"👑",
attack:150,
defense:100,
hp:200,
type:"player"
},

{
id:"z3rk_common",
name:"Z3RK",
rarity:"common",
icon:"👤",
attack:55,
defense:25,
hp:85,
type:"player"
},

{
id:"z3rk_rare",
name:"Z3RK",
rarity:"rare",
icon:"⚡",
attack:80,
defense:45,
hp:100,
type:"player"
},

{
id:"z3rk_epic",
name:"Z3RK ÉPIQUE",
rarity:"epic",
icon:"💜",
attack:110,
defense:70,
hp:150,
type:"player"
},

{
id:"raphael_common",
name:"RAPHAËL",
rarity:"common",
icon:"👤",
attack:50,
defense:40,
hp:90,
type:"player"
},

{
id:"raphael_legendary",
name:"RAPHAËL LÉGENDE",
rarity:"legendary",
icon:"🏆",
attack:135,
defense:90,
hp:180,
type:"player"
},

{
id:"baptistoss_common",
name:"BAPTISTOSS",
rarity:"common",
icon:"👤",
attack:60,
defense:30,
hp:85,
type:"player"
},

{
id:"baptistoss_epic",
name:"BAPTISTOSS ÉPIQUE",
rarity:"epic",
icon:"🔥",
attack:115,
defense:75,
hp:150,
type:"player"
},

{
id:"ying_common",
name:"YING",
rarity:"common",
icon:"👤",
attack:45,
defense:50,
hp:100,
type:"player"
},

{
id:"ying_rare",
name:"YING",
rarity:"rare",
icon:"💎",
attack:80,
defense:65,
hp:130,
type:"player"
},

{
id:"ying_goat",
name:"YING GOAT",
rarity:"goat",
icon:"👑",
attack:155,
defense:110,
hp:210,
type:"player"
},

/* AUTRES CARTES */

{
id:"mascot",
name:"LA MASCOTTE",
rarity:"rare",
icon:"🦁",
attack:70,
defense:70,
hp:120,
type:"special"
},

{
id:"trophy",
name:"LE TROPHÉE",
rarity:"legendary",
icon:"🏆",
attack:120,
defense:80,
hp:100,
type:"special"
},

{
id:"arena",
name:"L'ARÈNE",
rarity:"rare",
icon:"🏟️",
attack:40,
defense:100,
hp:150,
type:"special"
},

{
id:"mode_goat",
name:"MODE GOAT",
rarity:"legendary",
icon:"👑",
attack:140,
defense:90,
hp:170,
type:"special"
},

{
id:"training",
name:"BOOST D'ENTRAÎNEMENT",
rarity:"common",
icon:"⚡",
attack:60,
defense:30,
hp:70,
type:"special"
},

{
id:"shield",
name:"BOUCLIER EUROPA",
rarity:"epic",
icon:"🛡️",
attack:50,
defense:140,
hp:180,
type:"special"
},

{
id:"perfect_shot",
name:"TIR PARFAIT",
rarity:"epic",
icon:"🎯",
attack:130,
defense:30,
hp:90,
type:"special"
},

{
id:"europa_universe",
name:"EUROPA UNIVERSE",
rarity:"goat",
icon:"🌌",
attack:180,
defense:150,
hp:250,
type:"special"
},

{
id:"europa_ship",
name:"VAISSEAU EUROPA",
rarity:"legendary",
icon:"🚀",
attack:130,
defense:100,
hp:160,
type:"special"
}

];

/* ================= GAME DATA ================= */

let game = JSON.parse(localStorage.getItem("europaCardsSave")) || {

coins:1000,
level:1,
xp:0,
collection:[],
deck:[],
tutorial:false,
wins:0,
bossWins:0,
packsOpened:0,
lastDaily:null,
successes:[]

};

let battleData = null;

/* ================= SAVE ================= */

function saveGame(){

localStorage.setItem(
"europaCardsSave",
JSON.stringify(game)
);

updateStats();

}

function updateStats(){

document.getElementById("coins").textContent = game.coins;
document.getElementById("level").textContent = game.level;
document.getElementById("collectionCount").textContent =
game.collection.length;

}

/* ================= PAGES ================= */

function showPage(page){

document.querySelectorAll(".page").forEach(p=>{
p.classList.remove("active");
});

document.getElementById(page).classList.add("active");

if(page==="collection") renderCollection();

if(page==="deck") renderDeck();

if(page==="success") renderSuccess();

}

/* ================= RARITY ================= */

function rarityName(rarity){

const names = {

common:"⚪ COMMUN",
rare:"🔵 RARE",
epic:"🟣 ÉPIQUE",
legendary:"🟠 LÉGENDAIRE",
goat:"👑 GOAT"

};

return names[rarity];

}

/* ================= CARD HTML ================= */

function cardHTML(card,button=""){

return `

<div class="card ${card.rarity}">

<div clas
