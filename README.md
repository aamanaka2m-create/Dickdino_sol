<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>DICKDINO - Small Dino. Big Gains. 🚀</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;800&display=swap" rel="stylesheet">
<link rel="icon" href="https://via.placeholder.com/32/ff7b00/000000?text=🦕">

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Poppins', sans-serif;
}

body {
  background: radial-gradient(circle at top, #0f2027, #000);
  color: white;
  overflow-x: hidden;
  line-height: 1.6;
}

/* Background Stars */
body::before {
  content: "";
  position: fixed;
  top: 0;
  left: 0;
  width: 100vw;
  height: 100vh;
  background: url('https://www.transparenttextures.com/patterns/stardust.png');
  animation: moveStars 80s linear infinite;
  opacity: 0.15;
  z-index: -1;
}

@keyframes moveStars {
  0% { transform: translate(0, 0); }
  100% { transform: translate(-100px, -100px); }
}

/* Navbar */
nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1.5rem 5%;
  backdrop-filter: blur(10px);
  background: rgba(0,0,0,0.3);
  position: sticky;
  top: 0;
  z-index: 100;
}

.logo {
  font-weight: 800;
  font-size: clamp(1.5rem, 4vw, 2rem);
  background: linear-gradient(45deg, #2EC4F6, #FFA62B);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

/* Hero Section */
.hero {
  text-align: center;
  padding: clamp(80px, 15vh, 150px) 5%;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.hero img {
  width: clamp(180px, 25vw, 280px);
  height: auto;
  animation: float 3s ease-in-out infinite;
  filter: drop-shadow(0 0 30px #2EC4F6);
  margin-bottom: 2rem;
}

@keyframes float {
  0%, 100% { transform: translateY(0) rotate(0deg); }
  50% { transform: translateY(-20px) rotate(2deg); }
}

.hero h1 {
  font-size: clamp(3rem, 8vw, 6rem);
  font-weight: 800;
  margin-bottom: 1.5rem;
  background: linear-gradient(45deg, #2EC4F6, #FFA62B, #ff7b00);
  -webkit-background-clip: text;
  background-clip: text;
  -webkit-text-fill-color: transparent;
}

.hero p {
  font-size: clamp(1.1rem, 3vw, 1.4rem);
  max-width: 600px;
  margin: 0 auto 2.5rem;
  opacity: 0.9;
}

/* Buttons */
.btn-group {
  display: flex;
  flex-wrap: wrap;
  gap: 1rem;
  justify-content: center;
}

.btn {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  padding: 1rem 2rem;
  border-radius: 50px;
  text-decoration: none;
  font-weight: 600;
  font-size: 1.1rem;
  transition: all 0.3s ease;
  backdrop-filter: blur(10px);
  position: relative;
  overflow: hidden;
}

.btn::before {
  content: '';
  position: absolute;
  top: 0;
  left: -100%;
  width: 100%;
  height: 100%;
  background: linear-gradient(90deg, transparent, rgba(255,255,255,0.2), transparent);
  transition: 0.5s;
}

.btn:hover::before {
  left: 100%;
}

.buy {
  background: linear-gradient(45deg, #ff7b00, #ffb347);
  box-shadow: 0 10px 30px rgba(255,123,0,0.4);
  border: none;
  color: white;
}

.buy:hover {
  transform: translateY(-3px) scale(1.05);
  box-shadow: 0 15px 40px rgba(255,123,0,0.6);
}

.social {
  background: rgba(255,255,255,0.1);
  border: 2px solid #2EC4F6;
  color: #2EC4F6;
}

.social:hover {
  background: rgba(46,196,246,0.2);
  transform: translateY(-3px);
}

/* Sections */
.section {
  padding: 100px 5%;
  max-width: 1400px;
  margin: 0 auto;
}

.section h2 {
  font-size: clamp(2rem, 5vw, 3rem);
  text-align: center;
  margin-bottom: 3rem;
  background: linear-gradient(45deg, #2EC4F6, #FFA62B);
  -webkit-background-clip: text;
  background-clip: text;
  -webkit-text-fill-color: transparent;
}

.section p {
  max-width: 800px;
  margin: 0 auto 3rem;
  text-align: center;
  font-size: 1.2rem;
  opacity: 0.9;
}

/* Cards */
.cards {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 2rem;
  max-width: 1200px;
  margin: 0 auto;
}

.card {
  background: rgba(255,255,255,0.08);
  padding: 2rem;
  border-radius: 20px;
  text-align: center;
  backdrop-filter: blur(15px);
  border: 1px solid rgba(255,255,255,0.1);
  transition: all 0.4s ease;
  position: relative;
  overflow: hidden;
}

.card::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 2px;
  background: linear-gradient(90deg, #2EC4F6, #FFA62B);
}

.card:hover {
  transform: translateY(-15px) scale(1.02);
  box-shadow: 0 25px 50px rgba(46,196,246,0.3);
  background: rgba(255,255,255,0.12);
}

.card strong {
  display: block;
  font-size: 1.3rem;
  margin-top: 0.5rem;
  color: #FFA62B;
}

/* Footer */
footer {
  text-align: center;
  padding: 3rem 5%;
  border-top: 1px solid rgba(255,255,255,0.1);
  margin-top: 5rem;
  opacity: 0.7;
}

footer p {
  font-size: 1rem;
}

/* Responsive */
@media (max-width: 768px) {
  nav {
    padding: 1rem 5%;
  }
  
  .btn-group {
    flex-direction: column;
    align-items: center;
  }
  
  .btn {
    width: 100%;
    max-width: 300px;
    justify-content: center;
  }
}

/* Scroll animations */
@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(30px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.section {
  animation: fadeInUp 0.8s ease-out;
}
</style>

</head>

<body>
<nav>
  <div class="logo">🦕 DICKDINO</div>
</nav>

<section class="hero" role="main">
  <!-- Replace with your actual logo -->
  <img src="https://via.placeholder.com/300x300/ff7b00/2EC4F6?text=🦕" alt="DickDino Logo - Cute dinosaur meme token" loading="lazy">

  <h1>DICKDINO</h1>
  <p>Small Dino. Big Gains. Ready to Moon 🚀</p>

  <div class="btn-group">
    <a href="#" class="btn buy" aria-label="Buy DICKDINO token">
      💰 BUY NOW
    </a>
    <a href="#" class="btn social" aria-label="Join DICKDINO Telegram">📱 TELEGRAM</a>
    <a href="#" class="btn social" aria-label="Follow DICKDINO on X">🐦 X</a>
  </div>
</section>

<section class="section" id="about">
  <h2>About DickDino</h2>
  <p>
    DickDino is the ultimate meme token combining adorable dinosaur vibes, 
    unstoppable community energy, and moonshot potential. Get in early 
    before we roar to the stars! 🦕🚀
  </p>
</section>

<section class="section" id="tokenomics">
  <h2>Tokenomics</h2>
  <div class="cards">
    <div class="card">
      <span style="font-size: 2.5rem;">1B</span>
      <strong>Total Supply</strong>
    </div>
    <div class="card">
      <span style="font-size: 2.5rem; color: #00ff88;">0%</span>
      <strong>Tax Free</strong>
    </div>
    <div class="card">
      <span>🔒</span>
      <strong>Liquidity Locked</strong>
    </div>
    <div class="card">
      <span>✅</span>
      <strong>Ownership Renounced</strong>
    </div>
  </div>
</section>

<section class="section" id="roadmap">
  <h2>Roadmap</h2>
  <div class="cards">
    <div class="card">
      <span>🚀</span>
      <strong>Phase 1<br>Launch & Community</strong>
    </div>
    <div class="card">
      <span>📈</span>
      <strong>Phase 2<br>Marketing Push</strong>
    </div>
    <div class="card">
      <span>🏪</span>
      <strong>Phase 3<br>Exchange Listings</strong>
    </div>
    <div class="card">
      <span>🌙</span>
      <strong>Phase 4<br>TO THE MOON!</strong>
    </div>
  </div>
</section>

<section class="section" id="why">
  <h2>Why DickDino?</h2>
  <div class="cards">
    <div class="card">
      <span>🦕</span>
      <strong>Unique Character</strong>
    </div>
    <div class="card">
      <span>🔥</span>
      <strong>Viral Potential</strong>
    </div>
    <div class="card">
      <span>💎</span>
      <strong>Early Entry</strong>
    </div>
    <div class="card">
      <span>🚀</span>
      <strong>Explosive Growth</strong>
    </div>
  </div>
</section>

<footer>
  <p>© 2026 DICKDINO — To The Moon 🚀 | Not financial advice</p>
</footer>

<script>
  // Smooth scrolling for anchor links
  document.querySelectorAll('a[href^="#"]').forEach(anchor => {
    anchor.addEventListener('click', function (e) {
      e.preventDefault();
      const target = document.querySelector(this.getAttribute('href'));
      if (target) {
        target.scrollIntoView({ behavior: 'smooth', block: 'start' });
      }
    });
  });

  // Add scroll-triggered animations
  const observer = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
      if (entry.isIntersecting) {
        entry.target.style.animationPlayState = 'running';
      }
    });
  });

  document.querySelectorAll('.card').forEach(card => {
    observer.observe(card);
  });
</script>

</body>
</html>