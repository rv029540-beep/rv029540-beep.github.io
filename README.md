<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Birthday Note</title>

<style>
    body {
        margin: 0;
        height: 100vh;
        font-family: Arial;
        background-color: #f9f9f9;
        text-align: center;
        overflow: hidden;
    }

    .center {
        position: relative;
        top: 20%;
        padding: 20px;
    }

    .heart {
        position: fixed;
        bottom: -40px;
        font-size: 28px;
        animation: floatUp linear forwards;
        text-shadow: 0 0 10px currentColor,
                     0 0 20px currentColor,
                     0 0 30px currentColor;
    }

    .pink { color: #ff4d6d; }
    .blue { color: #4dabf7; }

    @keyframes floatUp {
        from {
            transform: translateY(0);
            opacity: 1;
        }
        to {
            transform: translateY(-120vh);
            opacity: 0;
        }
    }
</style>
</head>

<body>

<div class="center">
    <h1 style="color:#ff4081;">🎉 Happy Birthday 🎉</h1>

    <p>
        <strong>Dear Best Friend</strong> 💛
    </p>

    <p>
        Tum meri life ki sabse special best friend ho.  
        Tum bina bole sab samajh leti ho aur har situation mein mere saath khadi rehti ho.
    </p>

    <p>
        Tumhari wajah se meri life mein smiles aayi hain,  
        aur main hamesha thankful hoon ki tum meri best friend ho.
    </p>

    <p>
        Dua karta hoon ki tumhari life hamesha khushiyon se bhari rahe,  
        tumhare saare dreams poore ho,  
        aur tum hamesha aise hi strong, kind aur amazing raho ✨
    </p>

    <p>
        Aaj ka din pura enjoy karo,  
        cake zyada khana 😄🎂
    </p>

    <h3 style="color:#4caf50;">With lots of love 💛</h3>
    <h4>— Your Best Friend</h4>
</div>

<script>
function createHeart() {
    const heart = document.createElement("div");
    heart.className = "heart";

    if (Math.random() > 0.5) {
        heart.classList.add("pink");
        heart.innerText = "💗";
    } else {
        heart.classList.add("blue");
        heart.innerText = "💙";
    }

    heart.style.left = Math.random() * window.innerWidth + "px";
    heart.style.fontSize = (22 + Math.random() * 25) + "px";
    heart.style.animationDuration = (4 + Math.random() * 4) + "s";

    document.body.appendChild(heart);

    setTimeout(() => {
        heart.remove();
    }, 9000);
}

setInterval(createHeart, 150);
</script>

</body>
</html>
