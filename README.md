<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ayhem | Full Stack Developer</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary-color: #00f2fe;
            --secondary-color: #4facfe;
            --bg-color: #0a192f;
            --text-color: #8892b0;
            --heading-color: #ccd6f6;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html, body {
            overflow-x: hidden;
            font-family: 'Poppins', sans-serif;
            background-color: var(--bg-color);
            color: var(--text-color);
            line-height: 1.7;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1rem 0;
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            background-color: rgba(10, 25, 47, 0.85);
            backdrop-filter: blur(10px);
            z-index: 1000;
        }

        nav .container {
            width: 100%;
        }

        .nav-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        nav .logo {
            font-size: 1.5rem;
            font-weight: 700;
            color: var(--primary-color);
        }

        nav ul {
            display: flex;
            list-style: none;
            margin: 0;
            padding: 0;
        }

        nav ul li {
            margin-left: 2rem;
        }

        nav ul li a {
            color: var(--heading-color);
            text-decoration: none;
            font-size: 0.9rem;
            transition: color 0.3s ease;
        }

        nav ul li a:hover {
            color: var(--primary-color);
        }

        section {
            min-height: 100vh;
            display: flex;
            align-items: center;
            padding: 4rem 0;
        }

        h1, h2, h3 {
            color: var(--heading-color);
        }

        .hero h1 {
            font-size: 4rem;
            margin-bottom: 1rem;
        }

        .hero p {
            font-size: 1.2rem;
            max-width: 600px;
            margin-bottom: 2rem;
        }

        .btn {
            display: inline-block;
            background: linear-gradient(45deg, var(--primary-color), var(--secondary-color));
            color: var(--bg-color);
            padding: 0.8rem 1.5rem;
            border-radius: 5px;
            text-decoration: none;
            font-weight: 600;
            transition: transform 0.3s ease;
        }

        .btn:hover {
            transform: translateY(-3px);
        }

        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 2rem;
            margin-top: 2rem;
        }

        .skill {
            text-align: center;
            padding: 2rem;
            background-color: rgba(255, 255, 255, 0.05);
            border-radius: 10px;
            transition: transform 0.3s ease;
        }

        .skill:hover {
            transform: translateY(-5px);
        }

        .skill i {
            font-size: 3rem;
            margin-bottom: 1rem;
            color: var(--primary-color);
        }

        .timeline {
            position: relative;
            max-width: 800px;
            margin: 0 auto;
        }

        .timeline::after {
            content: '';
            position: absolute;
            width: 2px;
            background-color: var(--primary-color);
            top: 0;
            bottom: 0;
            left: 50%;
            margin-left: -1px;
        }

        .timeline-item {
            padding: 10px 40px;
            position: relative;
            background-color: inherit;
            width: 50%;
        }

        .timeline-item::after {
            content: '';
            position: absolute;
            width: 20px;
            height: 20px;
            right: -10px;
            background-color: var(--bg-color);
            border: 4px solid var(--primary-color);
            top: 15px;
            border-radius: 50%;
            z-index: 1;
        }

        .left {
            left: 0;
        }

        .right {
            left: 50%;
        }

        .right::after {
            left: -10px;
        }

        .language-switcher, .theme-toggle {
            position: fixed;
            top: 20px;
            z-index: 1000;
        }

        .language-switcher {
            right: 20px;
        }

        .theme-toggle {
            left: 20px;
        }

        .micro-interaction {
            transition: transform 0.3s ease;
        }

        .micro-interaction:hover {
            transform: scale(1.05);
        }

        #particles-js {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
        }

        #live-demo .container {
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        #editor {
            width: 100%;
            height: 300px;
            margin-bottom: 1rem;
        }

        #demoCanvas {
            width: 100%;
            max-width: 800px;
            height: 400px;
            border: 1px solid #000;
            margin-top: 1rem;
        }

        .contact-form {
            display: flex;
            flex-direction: column;
            max-width: 500px;
            margin: 2rem auto 0;
        }

        .contact-form input,
        .contact-form textarea {
            margin-bottom: 1rem;
            padding: 0.8rem;
            border: none;
            border-radius: 5px;
            background-color: rgba(255, 255, 255, 0.1);
            color: var(--text-color);
        }

        .contact-form textarea {
            min-height: 150px;
            resize: vertical;
        }

        .contact-form .btn {
            align-self: center;
        }

        .modern-footer {
            background-color: var(--bg-color);
            color: var(--text-color);
            padding: 2rem 0;
        }

        .footer-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
        }

        .footer-logo {
            font-size: 2rem;
            font-weight: bold;
            color: var(--primary-color);
        }

        .footer-links a {
            color: var(--text-color);
            text-decoration: none;
            margin: 0 1rem;
            transition: color 0.3s ease;
        }

        .footer-links a:hover {
            color: var(--primary-color);
        }

        .footer-social a {
            color: var(--text-color);
            font-size: 1.5rem;
            margin: 0 0.5rem;
            transition: color 0.3s ease;
        }

        .footer-social a:hover {
            color: var(--primary-color);
        }

        .footer-bottom {
            margin-top: 1rem;
            text-align: center;
            font-size: 0.9rem;
        }

        .floating-controls {
            position: fixed;
            bottom: 20px;
            right: 20px;
            display: flex;
            flex-direction: column;
            gap: 10px;
        }

        .floating-controls button {
            background-color: var(--primary-color);
            color: var(--bg-color);
            border: none;
            padding: 10px 15px;
            border-radius: 5px;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .floating-controls button:hover {
            background-color: var(--secondary-color);
        }

        .dark-mode {
            --bg-color: #1a1a1a;
            --text-color: #f0f0f0;
            --heading-color: #ffffff;
        }
    </style>
</head>
<body>
    <div id="particles-js"></div>

    <div class="language-switcher">
        <button onclick="switchLanguage('en')">EN</button>
        <button onclick="switchLanguage('ja')">JP</button>
    </div>

    <div class="theme-toggle">
        <button onclick="toggleTheme()">Toggle Theme</button>
    </div>

    <nav>
        <div class="container">
            <div class="nav-content">
                <div class="logo">AYHEM</div>
                <ul>
                    <li><a href="#home">Home</a></li>
                    <li><a href="#about">About</a></li>
                    <li><a href="#experience">Experience</a></li>
                    <li><a href="#skills">Skills</a></li>
                    <li><a href="#projects">Projects</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </div>
        </div>
    </nav>

    <main>
        <section id="home" class="hero">
            <div class="container">
                <p class="lang-en">Versatile Full Stack Developer with expertise in WordPress, React Native, and e-commerce solutions.</p>
                <p class="lang-jp" style="display: none;">WordPressやReact Native、Eコマースソリューションに精通した多才なフルスタック開発者。</p>
                <h2>About Me</h2>
                <p class="lang-en">I'm a passionate developer with a diverse skill set, ranging from frontend technologies to e-commerce solutions. With experience working in various roles across Japan, I bring a unique perspective to every project I undertake.</p>
                <p class="lang-jp" style="display: none;">私は、フロントエンド技術からEコマースソリューションまで、多様なスキルセットを持つ情熱的な開発者です。日本全国で様々な役割を経験してきたことで、各プロジェクトに独自の視点をもたらします。</p>
                <a href="#contact" class="btn lang-en">Get in Touch</a>
                <a href="#contact" class="btn lang-jp" style="display: none;">お問い合わせ</a>


            </div>
        </section>

        <section id="skills">
            <div class="container">
                <h2>Skills</h2>
                <div class="skills-grid">
                    <div class="skill">
                        <i class="fab fa-react"></i>
                        <h3>React</h3>
                    </div>
                    <div class="skill">
                        <i class="fab fa-node-js"></i>
                        <h3>Node.js</h3>
                    </div>
                    <div class="skill">
                        <i class="fab fa-wordpress"></i>
                        <h3>WordPress</h3>
                    </div>
                    <div class="skill">
                        <i class="fas fa-shopping-cart"></i>
                        <h3>E-commerce</h3>
                    </div>
                </div>
            </div>
        </section>

        <section id="timeline">
            <div class="container">
                <h2>Career Timeline</h2>
                <div class="timeline">
                    <div class="timeline-item left">
                        <div class="content">
                            <h3>2024</h3>
                            <p>WordPress Developer at Mobius.tokyo</p>
                        </div>
                    </div>
                    <div class="timeline-item right">
                        <div class="content">
                            <h3>2023</h3>
                            <p>Frontend Developer at Coca-Cola Bottlers Japan Inc.</p>
                        </div>
                    </div>
                    <div class="timeline-item left">
                        <div class="content">
                            <h3>2023</h3>
                            <p>Software Engineer at Kairos Trading</p>
                        </div>
                    </div>
                    <div class="timeline-item right">
                        <div class="content">
                            <h3>2023</h3>
                            <p>Frontend Developer at ekei labs</p>
                        </div>
                    </div>
                    <div class="timeline-item left">
                        <div class="content">
                            <h3>2022-2023</h3>
                            <p>E-commerce Entrepreneur at MARCHANDIGUE LTD</p>
                        </div>
                    </div>
                </div>
            </div>
        </section>
        <section id="live-demo">
            <div class="container">
                <h2 class="lang-en">Interactive Particle System</h2>
                <h2 class="lang-jp" style="display: none;">インタラクティブな粒子システム</h2>
                <canvas id="demoCanvas"></canvas>
                <div class="controls">
                    <button onclick="toggleAnimation()" class="btn lang-en">Toggle Animation</button>
                    <button onclick="toggleAnimation()" class="btn lang-jp" style="display: none;">アニメーション切替</button>
                    <input type="color" id="colorPicker" onchange="changeColor(this.value)">
                    <input type="range" id="particleCount" min="50" max="500" value="150" onchange="updateParticleCount(this.value)">
                    <span id="particleCountValue">150</span>
                </div>
            </div>
        </section>

        <section id="contact">
            <div class="container">
                <h2>Get in Touch</h2>
                <p>I'm always open to new opportunities and collaborations. Feel free to reach out!</p>
                <form class="contact-form">
                    <input type="text" placeholder="Your Name" required>
                    <input type="email" placeholder="Your Email" required>
                    <textarea placeholder="Your Message" required></textarea>
                    <button type="submit" class="btn">Send Message</button>
                </form>
            </div>
        </section>
    </main>

    <footer class="modern-footer">
        <div class="container">
            <div class="footer-content">
                <div class="footer-logo">AY</div>
                <div class="footer-links">
                    <a href="#home">Home</a>
                    <a href="#about">About</a>
                    <a href="#skills">Skills</a>
                    <a href="#projects">Projects</a>
                    <a href="#contact">Contact</a>
                </div>
                <div class="footer-social">
                    <a href="#"><i class="fab fa-github"></i></a>
                    <a href="#"><i class="fab fa-linkedin"></i></a>
                    <a href="#"><i class="fab fa-twitter"></i></a>
                </div>
            </div>
            <div class="footer-bottom">
                <p>&copy; 2024 Ayhem. All rights reserved.</p>
            </div>
        </div>
    </footer>

    <div class="floating-controls">
        <button id="langToggle" onclick="toggleLanguage()">EN | JP</button>
        <button id="themeToggle" onclick="toggleTheme()">
            <i class="fas fa-sun"></i>
            <i class="fas fa-moon" style="display: none;"></i>
        </button>
    </div>

    <script>
        // ... existing script ...

        let isJapanese = false;
        let isDarkMode = false;

        function toggleLanguage() {
            isJapanese = !isJapanese;
            document.querySelectorAll('.lang-en, .lang-jp').forEach(el => {
                el.style.display = el.classList.contains(isJapanese ? 'lang-jp' : 'lang-en') ? 'block' : 'none';
            });
            document.getElementById('langToggle').textContent = isJapanese ? 'JP | EN' : 'EN | JP';
            document.getElementById('langToggle').style.transform = `translateX(${isJapanese ? '20px' : '0'})`;
        }

        function toggleTheme() {
            isDarkMode = !isDarkMode;
            document.body.classList.toggle('dark-mode', isDarkMode);
            document.querySelector('#themeToggle .fa-sun').style.display = isDarkMode ? 'none' : 'inline-block';
            document.querySelector('#themeToggle .fa-moon').style.display = isDarkMode ? 'inline-block' : 'none';
            document.getElementById('themeToggle').style.transform = `translateX(${isDarkMode ? '20px' : '0'})`;
        }
    </script>

    <script>
        const canvas = document.getElementById('demoCanvas');
        const ctx = canvas.getContext('2d');
        canvas.width = canvas.offsetWidth;
        canvas.height = canvas.offsetHeight;

        let particles = [];
        let animationId;
        let isAnimating = true;
        let particleColor = '#ffffff';

        class Particle {
            constructor(x, y) {
                this.x = x;
                this.y = y;
                this.size = Math.random() * 5 + 1;
                this.speedX = Math.random() * 3 - 1.5;
                this.speedY = Math.random() * 3 - 1.5;
            }

            update() {
                this.x += this.speedX;
                this.y += this.speedY;

                if (this.size > 0.2) this.size -= 0.1;
            }

            draw() {
                ctx.fillStyle = particleColor;
                ctx.beginPath();
                ctx.arc(this.x, this.y, this.size, 0, Math.PI * 2);
                ctx.fill();
            }
        }

        function createParticles() {
            particles = [];
            const particleCount = parseInt(document.getElementById('particleCount').value);
            for (let i = 0; i < particleCount; i++) {
                particles.push(new Particle(Math.random() * canvas.width, Math.random() * canvas.height));
            }
        }

        function animate() {
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            for (let i = 0; i < particles.length; i++) {
                particles[i].update();
                particles[i].draw();
                
                for (let j = i; j < particles.length; j++) {
                    const dx = particles[i].x - particles[j].x;
                    const dy = particles[i].y - particles[j].y;
                    const distance = Math.sqrt(dx * dx + dy * dy);
                    
                    if (distance < 100) {
                        ctx.beginPath();
                        ctx.strokeStyle = particleColor;
                        ctx.lineWidth = 0.2;
                        ctx.moveTo(particles[i].x, particles[i].y);
                        ctx.lineTo(particles[j].x, particles[j].y);
                        ctx.stroke();
                    }
                }
                
                if (particles[i].size <= 0.2) {
                    particles.splice(i, 1);
                    i--;
                }
            }
            
            if (isAnimating) {
                animationId = requestAnimationFrame(animate);
            }
        }

        function toggleAnimation() {
            isAnimating = !isAnimating;
            if (isAnimating) {
                animate();
            } else {
                cancelAnimationFrame(animationId);
            }
        }

        function changeColor(color) {
            particleColor = color;
        }

        function updateParticleCount(count) {
            document.getElementById('particleCountValue').textContent = count;
            createParticles();
        }

        canvas.addEventListener('click', (event) => {
            const rect = canvas.getBoundingClientRect();
            const x = event.clientX - rect.left;
            const y = event.clientY - rect.top;
            for (let i = 0; i < 5; i++) {
                particles.push(new Particle(x, y));
            }
        });

        createParticles();
        animate();
    </script>

    <style>
        #live-demo .container {
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        #demoCanvas {
            width: 100%;
            max-width: 800px;
            height: 400px;
            background-color: #000;
            margin-top: 1rem;
        }

        .controls {
            margin-top: 1rem;
            display: flex;
            gap: 1rem;
            align-items: center;
        }
    </style>
</body>
</html>
