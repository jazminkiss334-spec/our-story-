# our-story-
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>VALENTIN PUZZLE</title>
<style>
body{
    background:black;
    color:#00ff88;
    font-family:Courier New, monospace;
    text-align:center;
    overflow-x:hidden;
}
h1{
    margin-top:40px;
    text-shadow:0 0 15px #00ff88;
}
#terminal{
    margin-top:40px;
    font-size:18px;
    min-height:120px;
}
input{
    background:black;
    border:1px solid #00ff88;
    color:#00ff88;
    padding:10px;
    width:300px;
    margin-top:20px;
}
button{
    background:#001a0f;
    border:1px solid #00ff88;
    color:#00ff88;
    padding:10px 20px;
    cursor:pointer;
}
button:hover{
    background:#003322;
}
.glitch{
    animation:glitch 1s infinite;
}
@keyframes glitch{
    0%{text-shadow:2px 2px red;}
    25%{text-shadow:-2px -2px blue;}
    50%{text-shadow:2px -2px lime;}
    75%{text-shadow:-2px 2px magenta;}
    100%{text-shadow:2px 2px red;}
}
.heart{
    font-size:60px;
    animation:beat 1s infinite;
}
@keyframes beat{
    0%{transform:scale(1);}
    50%{transform:scale(1.3);}
    100%{transform:scale(1);}
}
.robot{
    font-size:70px;
    animation:float 2s infinite;
}
@keyframes float{
    0%{transform:translateY(0);}
    50%{transform:translateY(-20px);}
    100%{transform:translateY(0);}
}
.hidden{display:none;}
</style>
</head>
<body>

<h1 class="glitch">OPERATION: LOVE_PROTOCOL</h1>

<div id="terminal"></div>
<input id="answer" placeholder="TYPE ANSWER HERE">
<br>
<button onclick="checkAnswer()">EXECUTE</button>

<script>

let level = 1;
const terminal = document.getElementById("terminal");

function normalize(text){
    return text.toLowerCase().trim();
}

function nextLevel(){
    document.getElementById("answer").value="";
}

function checkAnswer(){
    let input = normalize(document.getElementById("answer").value);

    if(level===1){
        if(input.includes("ne pakolj") && input.includes("foldre")){
            terminal.innerHTML="LEVEL 1 COMPLETE ✔<br>Memory unlocked...";
            level=2;
            setTimeout(loadLevel,1500);
        }else fail();
    }

    else if(level===2){
        if(input.includes("tea") && input.includes("billy")){
            terminal.innerHTML="LEVEL 2 COMPLETE ✔<br>'Ha így folytatod talán ma egy óráig jobban szerethetsz'";
            level=3;
            setTimeout(loadLevel,2000);
        }else fail();
    }

    else if(level===3){
        if(input.includes("duna") && input.includes("vasárnap")){
            terminal.innerHTML="LEVEL 3 COMPLETE ✔<br>The kiss protocol restored...";
            level=4;
            setTimeout(loadLevel,2000);
        }else fail();
    }

    else if(level===4){
        if(input.includes("spagetti") && input.includes("egyiptomi") && input.includes("ferrero")){
            terminal.innerHTML="LEVEL 4 COMPLETE ✔<br>Deep memory synchronization...";
            level=5;
            setTimeout(loadLevel,2000);
        }else fail();
    }

    else if(level===5){
        if(input.includes("arc") || input.includes("szem")){
            terminal.innerHTML="LEVEL 5 COMPLETE ✔<br>Emotional core accessed...";
            level=6;
            setTimeout(loadLevel,2000);
        }else fail();
