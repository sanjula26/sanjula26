<div align="center">
  <!-- 🔥 ULTIMATE 3D CYBERPUNK HEADER 🔥 -->
  <div style="
    background: linear-gradient(45deg, #000428 0%, #004e92 25%, #00FFAA 50%, #16213e 75%, #0c0c0c 100%);
    background-size: 400% 400%;
    animation: gradientShift 8s ease infinite;
    padding: 50px 30px;
    border-radius: 30px;
    box-shadow: 
      0 0 60px rgba(0, 255, 170, 0.6),
      0 0 120px rgba(0, 255, 170, 0.3),
      inset 0 0 60px rgba(0, 255, 170, 0.15),
      0 25px 50px rgba(0, 0, 0, 0.7);
    position: relative;
    overflow: hidden;
    backdrop-filter: blur(15px);
    border: 2px solid rgba(0, 255, 170, 0.3);
  ">
    
    <!-- Matrix Rain Effect -->
    <canvas id="matrix" style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; opacity: 0.1; z-index: 1;"></canvas>

    <!-- Advanced Floating Particles -->
    <div class="particles" style="
      position: absolute;
      top: 0; left: 0; right: 0; bottom: 0;
      pointer-events: none;
      z-index: 2;
    ">
      <div class="particle" style="--delay: 0s; --size: 6px; --x: 10%; --y: 15%;"></div>
      <div class="particle" style="--delay: 2s; --size: 4px; --x: 85%; --y: 25%;"></div>
      <div class="particle" style="--delay: 4s; --size: 5px; --x: 20%; --y: 70%;"></div>
      <div class="particle" style="--delay: 1s; --size: 3px; --x: 70%; --y: 40%;"></div>
      <div class="particle" style="--delay: 3s; --size: 7px; --x: 40%; --y: 85%;"></div>
    </div>

    <!-- Holographic Typing Effect -->
    <div class="holo-container" style="position: relative; z-index: 4;">
      <img 
        src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&weight=900&size=36&duration=3500&pause=2000&color=00FFAA&center=true&vCenter=true&width=950&lines=🌌+CYBER+TECH+MASTER;Hemantha+Sanjula+%F0%9F%92%BB;🔧+Chip+Level+Repair+God;💻+Full+Stack+Developer+%7C+SL;⚡+Dehiattakandiya+Cyber+Hero"
        alt="ULTIMATE 3D Holographic Header"
        class="holo-text"
        style="
          filter: 
            drop-shadow(0 0 25px #00FFAA) 
            drop-shadow(0 0 50px #00FFAA)
            drop-shadow(0 0 75px #00D4AA)
            hue-rotate(120deg);
          transform: perspective(1000px) rotateX(10deg) scale(1.1);
          transition: all 0.3s ease;
        "
        onmouseover="this.style.transform='perspective(1000px) rotateX(5deg) scale(1.15) translateZ(50px)'"
        onmouseout="this.style.transform='perspective(1000px) rotateX(10deg) scale(1.1)'"
      />
    </div>

    <!-- Multi-Layer Glow Base -->
    <div class="glow-base" style="
      position: absolute;
      bottom: -25px;
      left: 50%;
      transform: translateX(-50%);
      width: 250px;
      height: 12px;
      background: linear-gradient(90deg, transparent, #00FFAA, #00D4AA, #00FFAA, transparent);
      border-radius: 50px;
      animation: megaPulse 1.5s infinite;
      box-shadow: 0 0 30px #00FFAA;
      z-index: 3;
    "></div>

    <!-- Tech Badge -->
    <div class="tech-badge" style="
      position: absolute;
      top: 15px;
      right: 20px;
      background: rgba(0, 255, 170, 0.2);
      padding: 8px 16px;
      border-radius: 20px;
      border: 1px solid rgba(0, 255, 170, 0.5);
      font-family: 'Fira Code', monospace;
      font-size: 12px;
      color: #00FFAA;
      backdrop-filter: blur(10px);
      animation: badgeFloat 3s infinite;
    ">
      🚀 TECH LEVEL: MAX
    </div>
  </div>
</div>

<style>
  @keyframes gradientShift {
    0% { background-position: 0% 50%; }
    50% { background-position: 100% 50%; }
    100% { background-position: 0% 50%; }
  }

  @keyframes megaPulse {
    0%, 100% { 
      opacity: 0.7; 
      transform: translateX(-50%) scale(1) translateY(0px);
      box-shadow: 0 0 30px #00FFAA;
    }
    50% { 
      opacity: 1; 
      transform: translateX(-50%) scale(1.3) translateY(-5px);
      box-shadow: 0 0 60px #00FFAA, 0 0 90px #00D4AA;
    }
  }

  @keyframes badgeFloat {
    0%, 100% { transform: translateY(0px); }
    50% { transform: translateY(-8px); }
  }

  .particle {
    position: absolute;
    width: var(--size);
    height: var(--size);
    background: radial-gradient(circle, #00FFAA, transparent);
    border-radius: 50%;
    left: var(--x);
    top: var(--y);
    animation: particleFloat calc(6s + var(--delay)) infinite ease-in-out;
    box-shadow: 0 0 15px #00FFAA;
  }

  @keyframes particleFloat {
    0%, 100% { 
      transform: translateY(0px) scale(1) rotate(0deg); 
      opacity: 0.6; 
    }
    33% { 
      transform: translateY(-25px) scale(1.3) rotate(120deg); 
      opacity: 1; 
    }
    66% { 
      transform: translateY(-10px) scale(0.8) rotate(240deg); 
      opacity: 0.8; 
    }
  }

  /* Matrix Rain Canvas */
  #matrix {
    z-index: 1 !important;
  }
</style>

<script>
  // Matrix Rain Effect
  const canvas = document.getElementById('matrix');
  const ctx = canvas.getContext('2d');
  
  canvas.width = canvas.offsetWidth;
  canvas.height = canvas.offsetHeight;
  
  const matrix = "අයුබෝවන්01චිප්10ලැප්ටොප්01හේමන්ත01සංජුල01TECH01";
  const matrixArray = matrix.split("");
  
  const fontSize = 14;
  const columns = canvas.width / fontSize;
  const drops = [];
  
  for(let x = 0; x < columns; x++) drops[x] = 1;
  
  function drawMatrix() {
    ctx.fillStyle = 'rgba(0, 4, 40, 0.05)';
    ctx.fillRect(0, 0, canvas.width, canvas.height);
    
    ctx.fillStyle = '#00FFAA';
    ctx.font = fontSize + 'px monospace';
    
    for(let i = 0; i < drops.length; i++) {
      const text = matrixArray[Math.floor(Math.random()*matrixArray.length)];
      ctx.fillText(text, i*fontSize, drops[i]*fontSize);
      
      if(drops[i]*fontSize > canvas.height && Math.random() > 0.975)
        drops[i] = 0;
      drops[i]++;
    }
  }
  
  setInterval(drawMatrix, 50);
  
  // Responsive canvas
  window.addEventListener('resize', () => {
    canvas.width = canvas.offsetWidth;
    canvas.height = canvas.offsetHeight;
  });
</script>

<br><br>

<!-- ULTIMATE 3D SHIELDS -->
<div align="center">
  <a href="https://maps.google.com/?q=Dehiattakandiya">
    <img src="https://img.shields.io/badge/🌍_දෙහිඅට්ටකන්ඩිය-FF6B35?style=for-the-badge&logo=googlemaps&logoColor=white&labelColor=0c0c0c&color=1a1a2e" alt="Location" />
  </a>
  <a href="https://github.com/sanjula26">
    <img src="https://img.shields.io/badge/🔧_චිප්+ලෙවල්+ගොඩ්-00D4AA?style=for-the-badge&logo=tools&logoColor=black&labelColor=16213e&color=004e92" alt="Chip Master" />
  </a>
  <a href="mailto:sanjulahemantha743@gmail.com">
    <img src="https://img.shields.io/badge/💻_Full+Stack-00FFAA?style=for-the-badge&logo=javascript&logoColor=black&labelColor=0c0c0c&color=1a1a2e" alt="Full Stack" />
  </a>
  <a href="https://wa.me/+94773123456">
    <img src="https://img.shields.io/badge/WhatsApp-25D366?style=for-the-badge&logo=whatsapp&logoColor=white&labelColor=128C7E" alt="WhatsApp" />
  </a>
</div>

<div align="center" style="
  margin-top: 25px; 
  font-family: 'Fira Code', monospace; 
  background: rgba(0,255,170,0.1);
  padding: 15px 30px;
  border-radius: 20px;
  border: 1px solid rgba(0,255,170,0.3);
  color: #00FFAA; 
  font-size: 16px;
  box-shadow: 0 0 20px rgba(0,255,170,0.2);
">
  <b>🚀 ULTIMATE 3D CYBERPUNK MODE ACTIVATED! ✨</b><br>
  <small>Powered by Blackbox AI | සිංහල + English Cyber Tech Hero 🇱🇰</small>
</div>
