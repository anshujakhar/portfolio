<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Anshu Kumar | Resume</title>
  <style>
    /* Base Reset */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(135deg, #e0f7fa, #f9fbe7);
      color: #222;
      line-height: 1.6;
    }

    .container {
      max-width: 850px;
      margin: 3rem auto;
      padding: 2rem;
      background: #ffffff;
      box-shadow: 0 10px 40px rgba(0, 0, 0, 0.07);
      border-radius: 16px;
      transition: all 0.3s ease;
    }

    header {
      text-align: center;
      margin-bottom: 2.5rem;
    }

    h1 {
      font-size: 3rem;
      color: #333;
    }

    .tagline {
      font-size: 1.1rem;
      font-style: italic;
      color: #666;
      margin-top: 0.5rem;
    }

    .section {
      margin-bottom: 2.5rem;
      opacity: 0;
      transform: translateY(30px);
      transition: all 0.6s ease-out;
      border-left: 4px solid #c8e6c9;
      padding-left: 1.2rem;
    }

    .section.show {
      opacity: 1;
      transform: translateY(0);
    }

    .section h2 {
      font-size: 1.5rem;
      margin-bottom: 1rem;
      color: #2e7d32;
      position: relative;
    }

    .entry h3 {
      color: #444;
      margin-bottom: 0.2rem;
    }

    .entry p {
      color: #555;
      font-size: 0.95rem;
    }

    .tags {
      list-style: none;
      display: flex;
      flex-wrap: wrap;
      gap: 0.6rem;
      margin-top: 0.5rem;
    }

    .tags li {
      background: #e0f2f1;
      color: #004d40;
      padding: 0.4rem 0.9rem;
      border-radius: 20px;
      font-size: 0.85rem;
      transition: background 0.3s ease;
      cursor: default;
    }

    .tags li:hover {
      background: #b2dfdb;
    }

    @media (max-width: 600px) {
      h1 {
        font-size: 2.2rem;
      }

      .container {
        padding: 1.2rem;
      }
    }
  </style>
</head>
<body>
  <div class="container">
    <header>
      <h1>Anshu Kumar</h1>
      <p class="tagline">Data Analyst | Problem Solver | ML Engineer</p>
    </header>

    <section class="about section">
      <h2>About Me</h2>
      <p>
        I am a third-year student at MDU pursuing B.Tech in CSE (AI/ML). With an ever-growing curiosity in tech and hands-on building,
        I focus on blending embedded systems with AI/ML to solve real-world challenges.
        I've worked on drones, Li-Fi, and healthcare tools aimed at improving lives through innovation.
      </p>
    </section>

    <section class="education section">
      <h2>Education</h2>
      <div class="entry">
        <h3>B.Tech in Computer Science (AI/ML)</h3>
        <p>MDU University — 2023–2027</p>
      </div>
    </section>

    <section class="skills section">
      <h2>Skills</h2>
      <ul class="tags">
        <li>OOP</li>
        <li>DBMS</li>
        <li>Scikit-learn</li>
        <li>JavaScript</li>
        <li>Git</li>
        <li>Python</li>
        <li>Power BI</li>
        <li>TensorFlow</li>
      </ul>
    </section>

    <section class="languages section">
      <h2>Languages</h2>
      <ul class="tags">
        <li>C</li>
        <li>C++</li>
        <li>Python</li>
        <li>Java</li>
      </ul>
    </section>
  </div>

  <script>
    const sections = document.querySelectorAll('.section');

    const reveal = () => {
      sections.forEach(section => {
        const top = section.getBoundingClientRect().top;
        if (top < window.innerHeight - 50) {
          section.classList.add('show');
        }
      });
    };

    window.addEventListener('scroll', reveal);
    window.addEventListener('load', reveal);
  </script>
</body>
</html>
