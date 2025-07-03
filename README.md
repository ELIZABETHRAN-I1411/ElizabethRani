<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Elizabeth Rani – Portfolio</title>
  <link rel="stylesheet"
        href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
  <style>
    /* Reset */
    * { margin: 0; padding: 0; box-sizing: border-box; }
    html, body { width: 100%; height: 100%; font-family: Arial, sans-serif; }
    
    /* Header with animated background and sliding name */
    @keyframes fadeColor {
      from { background-color: #0099CC; }
      to   { background-color: #66CCFF; }
    }
    @keyframes slide-in-name {
      from { transform: translateX(-100%); opacity: 0; }
      to { transform: translateX(0); opacity: 1; }
    }
    .top-box {
      position: fixed; top: 0; left: 0; width: 100vw;
      padding: 20px 0; text-align: center; color: #000;
      animation: fadeColor 3s ease-in-out infinite alternate;
    }
    .top-box h1 {
      animation: slide-in-name 1.5s ease-out forwards;
    }
    .top-box .contacts a {
      margin: 0 8px; color: #000; text-decoration: none;
    }
    .top-box .contacts i { margin-right: 4px; }
    .page-content { margin-top: 140px; padding: 20px; max-width: 800px; margin-left: auto; margin-right: auto; }
    
    /* Scroll reveal styles */
    .reveal {
      opacity: 0;
      transform: translateY(50px);
      transition: opacity 0.8s ease-out, transform 0.8s ease-out;
    }
    .reveal.active {
      opacity: 1;
      transform: translateY(0);
    }
    
    section { margin-bottom: 40px; }
    section h2 { font-size: 1.4rem; border-bottom: 2px solid #0099CC; margin-bottom: 12px; padding-bottom: 4px; }
    ul { padding-left: 20px; list-style: disc; }
  </style>
</head>
<body>
  <div class="top-box">
    <h1>Elizabeth Rani M</h1>
    <div class="contacts">
      <a href="mailto:elizabethrani1411@gmail.com">
        <i class="fa-solid fa-envelope"></i> elizabethrani1411@gmail.com
      </a> —
      <a href="https://www.linkedin.com/in/elizabeth-rani-m-898435340" target="_blank">
        <i class="fa-brands fa-linkedin"></i> LinkedIn
      </a> —
      <a href="https://github.com/elizabethrani1411" target="_blank">
        <i class="fa-brands fa-github"></i> GitHub
      </a>
    </div>
  </div>
  
  <div class="page-content">
    <section class="reveal" id="about">
      <h2>🌟 About Me</h2>
      <p>Hi! I'm <strong>Elizabeth Rani M.</strong>, a final‑year MCA student from Sarah Tucker College, Tirunelveli, Tamil Nadu. Passionate about Android development and data science.</p>
    </section>
    
    <section class="reveal" id="projects">
      <h2>📱 Projects</h2>
      <h3>LYNX Centre – Empowering Students</h3>
      <p>...</p>
      <h3>Weapon Detection System</h3>
      <p>...</p>
    </section>
    
    <section class="reveal" id="skills">
      <h2>🛠 Skills</h2>
      <ul>
        <li>Android Studio, Java, Firebase & MongoDB</li>
        <li>HTML, CSS, GitHub, UI/UX Design</li>
        <li>Python, OpenCV, TensorFlow</li>
      </ul>
    </section>
    
    <section class="reveal" id="education">
      <h2>🎓 Education</h2>
      <ul>
        <li><strong>MCA</strong> – Sarah Tucker College (2023–2025)</li>
        <li><strong>BSc Computer Science</strong> – Govt. Arts & Science College (2019–2022)</li>
      </ul>
    </section>
    
    <section class="reveal" id="contact">
      <h2>📬 Contact Me</h2>
      <p>Email: elizabethrani1411@gmail.com</p>
    </section>
  </div>
  
  <script>
    document.addEventListener("DOMContentLoaded", () => {
      const reveals = document.querySelectorAll('.reveal');
      const observer = new IntersectionObserver(entries => {
        entries.forEach(entry => {
          if (entry.isIntersecting) {
            entry.target.classList.add('active');
            observer.unobserve(entry.target);
          }
        });
      }, { threshold: 0.1 });

      reveals.forEach(el => observer.observe(el));
    });
  </script>
</body>
</html>
