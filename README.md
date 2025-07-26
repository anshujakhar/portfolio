# portfolio
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Your Name | Resume</title>
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', sans-serif;
      background-color: #f5f5f5;
      color: #222;
      line-height: 1.6;
    }

    .container {
      max-width: 800px;
      margin: auto;
      padding: 2rem;
      background: #fff;
      box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05);
      border-radius: 10px;
      margin-top: 40px;
    }

    header {
      text-align: center;
      margin-bottom: 2rem;
    }

    h1 {
      margin: 0;
      font-size: 2.5rem;
    }

    .tagline {
      font-style: italic;
      color: #666;
    }

    .section {
      margin-bottom: 2rem;
      opacity: 0;
      transform: translateY(20px);
      transition: all 0.6s ease;
    }

    .section.show {
      opacity: 1;
      transform: translateY(0);
    }

    .section h2 {
      border-bottom: 2px solid #ddd;
      padding-bottom: 0.5rem;
      margin-bottom: 1rem;
      color: #333;
    }

    .entry h3 {
      margin: 0.2rem 0;
      color: #444;
    }

    .tags {
      list-style: none;
      padding: 0;
      display: flex;
      flex-wrap: wrap;
      gap: 0.5rem;
    }

    .tags li {
      background: #e0e0e0;
      padding: 0.4rem 0.8rem;
      border-radius: 5px;
      font-size: 0.9rem;
    }
  </style>
</head>
<body>
  <div class="container">
    <header>
      <h1>Your Name</h1>
      <p class="tagline">Web Developer | Problem Solver | Tech Enthusiast</p>
    </header>

    <section class="about section">
      <h2>About Me</h2>
      <p>A brief professional summary of who you are, what you specialize in, and what you're passionate about.</p>
    </section>

    <section class="education section">
      <h2>Education</h2>
      <div class="entry">
        <h3>B.Tech in Computer Science</h3>
        <p>XYZ University — 2020-2024</p>
      </div>
    </section>

    <section class="skills section">
      <h2>Skills</h2>
      <ul class="tags">
        <li>HTML</li>
        <li>CSS</li>
        <li>JavaScript</li>
        <li>Git</li>
        <li>React</li>
        <li>Node.js</li>
      </ul>
    </section>

    <section class="experience section">
      <h2>Experience</h2>
      <div class="entry">
        <h3>Frontend Developer Intern</h3>
        <p>ABC Corp — June 2023 - August 2023</p>
        <p>Worked on improving UI components, optimizing performance, and fixing bugs in live projects.</p>
      </div>
    </section>

    <section class="languages section">
      <h2>Languages</h2>
      <ul class="tags">
        <li>English - Fluent</li>
        <li>Hindi - Native</li>
        <li>French - Beginner</li>
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
