<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Leena ❤️</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<style>
body {
    margin: 0;
    font-family: 'Segoe UI', sans-serif;
    background: linear-gradient(120deg, #ff758c, #ff7eb3);
    color: white;
    text-align: center;
    overflow-x: hidden;
}

.container {
    padding: 40px 20px;
}

h1 {
    font-size: 3rem;
    margin-bottom: 5px;
}

.photo {
    width: 260px;
    height: 260px;
    margin: 25px auto;
    border-radius: 50%;
    overflow: hidden;
    border: 4px solid white;
    box-shadow: 0 15px 35px rgba(0,0,0,0.4);
}

.photo img {
    width: 100%;
    height: 100%;
    object-fit: cover;
}

.heart {
    font-size: 3.5rem;
    animation: beat 1s infinite;
}

@keyframes beat {
    0%,100% { transform: scale(1); }
    50% { transform: scale(1.25); }
}

.letter {
    background: rgba(255,255,255,0.2);
    padding: 25px;
    border-radius: 20px;
    max-width: 700px;
    margin: 30px auto;
    line-height: 1.8;
    font-size: 1.1rem;
}

.counter {
    margin-top: 20px;
    font-size: 1.1rem;
}

.falling-heart {
    position: fixed;
    top: -10px;
    font-size: 20px;
    animation: fall linear infinite;
}

@keyframes fall {
    to { transform: translateY(110vh); }
}

footer {
    margin: 40px 0;
    font-size: 0.9rem;
}
</style>
</head>

<body>

<script>
// PASSWORD PROTECTION
let pass = prompt("Enter the secret password ❤️");
if (pass !== "leena") {
    document.body.innerHTML = "<h2>Access denied 💔</h2>";
}
</script>

<div class="container">
    <h1>Leena ❤️</h1>
    <p>From Daksh, with endless love</p>

    <div class="photo">
        <img src="leena.jpg" alt="Leena">
    </div>

    <div class="heart">💖</div>

    <div class="letter">
        My Leena,<br><br>
        Distance may keep us apart, but it can never weaken what I feel for you.
        Every night I miss you, and every morning I choose you again.
        <br><br>
        You are my calm, my warmth, my safe place — even from miles away.
        Loving you has shown me that true love doesn’t need touch,
        it needs two hearts that never stop choosing each other.
        <br><br>
        Until distance becomes closeness,
        <br><br>
        <strong>My heart is already yours.</strong>
        <br><br>
        — Daksh 🤍
    </div>

    <div class="counter" id="days"></div>

    <!-- Background music: Tum Ho - Mohit Chauhan -->
    <iframe width="280" height="158"
        src="https://www.youtube.com/embed/IaD6z6JXJZc?autoplay=1&loop=1&playlist=IaD6z6JXJZc"
        allow="autoplay"
        frameborder="0">
    </iframe>

    <footer>
        Made only for you ❤️
    </footer>
</div>

<script>
// LOVE DAYS COUNTER (change date if you want)
const startDate = new Date("2024-01-01");
const today = new Date();
const days = Math.floor((today - startDate) / (1000 * 60 * 60 * 24));
document.getElementById("days").innerHTML =
    "Daksh has been loving you for <b>" + days + "</b> days 💞";

// Falling hearts
setInterval(() => {
    const heart = document.createElement("div");
    heart.className = "falling-heart";
    heart.innerHTML = "❤️";
    heart.style.left = Math.random() * 100 + "vw";
    heart.style.animationDuration = (3 + Math.random() * 3) + "s";
    document.body.appendChild(heart);
    setTimeout(() => heart.remove(), 6000);
}, 300);
</script>

</body>
</html>
