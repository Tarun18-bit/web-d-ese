<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Freelance Hub – Find Your Perfect Freelancer</title>
  <style>
    /* ===== BASIC RESET ===== */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: Arial, Helvetica, sans-serif;
    }

    body {
      background: #f5f5f5;
      color: #222;
      line-height: 1.6;
    }

    a {
      text-decoration: none;
      color: inherit;
    }

    /* ===== NAVBAR ===== */
    header {
      background: #222;
      color: #fff;
      padding: 15px 40px;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    .logo {
      font-size: 24px;
      font-weight: bold;
    }

    nav ul {
      list-style: none;
      display: flex;
      gap: 20px;
    }

    nav li {
      font-size: 14px;
    }

    nav a:hover {
      text-decoration: underline;
    }

    /* ===== HERO SECTION ===== */
    .hero {
      background: linear-gradient(135deg, #5c6bc0, #3949ab);
      color: #fff;
      padding: 60px 40px;
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      align-items: center;
    }

    .hero-text {
      max-width: 500px;
      margin-bottom: 20px;
    }

    .hero-text h1 {
      font-size: 36px;
      margin-bottom: 15px;
    }

    .hero-text p {
      font-size: 16px;
      margin-bottom: 20px;
    }

    .hero-buttons {
      display: flex;
      gap: 15px;
      flex-wrap: wrap;
    }

    .btn {
      padding: 10px 20px;
      border-radius: 4px;
      border: none;
      cursor: pointer;
      font-weight: bold;
      font-size: 14px;
      display: inline-block;
    }

    .btn-primary {
      background: #ffca28;
      color: #222;
    }

    .btn-secondary {
      background: transparent;
      border: 1px solid #fff;
      color: #fff;
    }

    .hero-image {
      min-width: 260px;
      max-width: 380px;
      background: rgba(255, 255, 255, 0.08);
      border-radius: 8px;
      padding: 20px;
    }

    .hero-image h3 {
      margin-bottom: 10px;
      font-size: 18px;
    }

    .hero-image p {
      font-size: 14px;
      margin-bottom: 8px;
    }

    /* ===== MAIN LAYOUT ===== */
    main {
      padding: 40px;
      max-width: 1100px;
      margin: 0 auto;
    }

    section {
      margin-bottom: 50px;
    }

    h2.section-title {
      font-size: 24px;
      margin-bottom: 10px;
    }

    .section-subtitle {
      font-size: 14px;
      color: #666;
      margin-bottom: 20px;
    }

    /* ===== CATEGORY TABS (STATIC) ===== */
    .categories {
      display: flex;
      gap: 10px;
      flex-wrap: wrap;
      margin-bottom: 20px;
    }

    .category-pill {
      padding: 8px 14px;
      background: #e0e0e0;
      border-radius: 20px;
      font-size: 13px;
      cursor: pointer;
    }

    .category-pill.active {
      background: #3949ab;
      color: #fff;
      font-weight: bold;
    }

    /* ===== FREELANCER CARDS ===== */
    .freelancer-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
      gap: 20px;
    }

    .freelancer-card {
      background: #fff;
      border-radius: 6px;
      padding: 15px;
      box-shadow: 0 2px 5px rgba(0,0,0,0.08);
      display: flex;
      flex-direction: column;
      justify-content: space-between;
    }

    .freelancer-card h3 {
      font-size: 18px;
      margin-bottom: 4px;
    }

    .freelancer-role {
      font-size: 13px;
      color: #3949ab;
      margin-bottom: 8px;
      font-weight: bold;
    }

    .freelancer-desc {
      font-size: 13px;
      color: #555;
      margin-bottom: 8px;
      min-height: 48px;
    }

    .freelancer-tags {
      font-size: 12px;
      color: #777;
      margin-bottom: 10px;
    }

    .freelancer-rate {
      font-size: 13px;
      font-weight: bold;
      margin-bottom: 12px;
    }

    .freelancer-bottom {
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    /* ===== HOW IT WORKS ===== */
    .steps {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
      gap: 20px;
    }

    .step {
      background: #fff;
      padding: 15px;
      border-radius: 6px;
      box-shadow: 0 2px 5px rgba(0,0,0,0.06);
    }

    .step-number {
      width: 30px;
      height: 30px;
      border-radius: 50%;
      background: #3949ab;
      color: #fff;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 14px;
      margin-bottom: 10px;
    }

    .step h3 {
      font-size: 16px;
      margin-bottom: 6px;
    }

    .step p {
      font-size: 13px;
      color: #555;
    }

    /* ===== CLIENT PROJECT FORM ===== */
    .project-form {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
      gap: 20px;
      background: #fff;
      padding: 20px;
      border-radius: 6px;
      box-shadow: 0 2px 5px rgba(0,0,0,0.06);
    }

    .project-form .form-field {
      display: flex;
      flex-direction: column;
      margin-bottom: 10px;
    }

    .project-form label {
      font-size: 13px;
      margin-bottom: 5px;
    }

    .project-form input,
    .project-form select,
    .project-form textarea {
      padding: 8px;
      border-radius: 4px;
      border: 1px solid #ccc;
      font-size: 13px;
    }

    .project-form textarea {
      resize: vertical;
      min-height: 80px;
    }

    .form-full-width {
      grid-column: 1 / -1;
    }

    .project-form button {
      margin-top: 10px;
    }

    /* ===== FOOTER ===== */
    footer {
      background: #222;
      color: #ddd;
      padding: 20px 40px;
      font-size: 13px;
      text-align: center;
    }

    footer a {
      color: #ffca28;
    }

    /* ===== RESPONSIVE ===== */
    @media (max-width: 600px) {
      header {
        flex-direction: column;
        align-items: flex-start;
        gap: 10px;
      }

      .hero {
        padding: 40px 20px;
      }

      main {
        padding: 30px 20px;
      }
    }
  </style>
</head>
<body>

  <!-- ===== HEADER / NAV ===== -->
  <header>
    <div class="logo">FreelanceHub</div>
    <nav>
      <ul>
        <li><a href="#freelancers">Browse Freelancers</a></li>
        <li><a href="#how-it-works">How It Works</a></li>
        <li><a href="#post-project">Post a Project</a></li>
      </ul>
    </nav>
  </header>

  <!-- ===== HERO SECTION ===== -->
  <section class="hero">
    <div class="hero-text">
      <h1>Hire Freelancers for Video Editing, Web Development & More</h1>
      <p>
        Connect with skilled freelancers for websites, apps, video editing, logos, thumbnails,
        and social media content. Post your project and start getting proposals within minutes.
      </p>
      <div class="hero-buttons">
        <a href="#post-project" class="btn btn-primary">Post a Project (Free)</a>
        <a href="#freelancers" class="btn btn-secondary">Browse Freelancers</a>
      </div>
    </div>

    <div class="hero-image">
      <h3>Popular Categories</h3>
      <p>• Video Editors – Reels, YouTube, promos</p>
      <p>• Web Developers – Portfolio, e-commerce, business sites</p>
      <p>• Graphic Designers – Logos, banners, thumbnails</p>
      <p>• Social Media Managers – Content, posting, strategy</p>
    </div>
  </section>

  <!-- ===== MAIN CONTENT ===== -->
  <main>

    <!-- FREELANCERS SECTION -->
    <section id="freelancers">
      <h2 class="section-title">Top Freelancers</h2>
      <p class="section-subtitle">
        Explore verified freelancers ready to work on your next project.
      </p>

      <!-- Fake filter pills (only design, no JS) -->
      <div class="categories">
        <div class="category-pill active">All</div>
        <div class="category-pill">Video Editors</div>
        <div class="category-pill">Web Developers</div>
        <div class="category-pill">Graphic Designers</div>
        <div class="category-pill">Social Media</div>
      </div>

      <div class="freelancer-grid">

        <!-- Freelancer 1 -->
        <article class="freelancer-card">
          <div>
            <h3>Tarun Maurya</h3>
            <div class="freelancer-role">Video Editor • Reels & YouTube</div>
            <p class="freelancer-desc">
              3+ years experience editing gaming, vlogs and cinematic travel videos.
              Specialized in fast-paced, TikTok style edits.
            </p>
            <p class="freelancer-tags">
              Premiere Pro • After Effects • Shorts • Reels
            </p>
            <p class="freelancer-rate">Starting at ₹800 per video</p>
          </div>
          <div class="freelancer-bottom">
            <span>⭐ 4.9 (120 reviews)</span>
            <a href="#post-project" class="btn btn-primary" style="padding:6px 12px;font-size:12px;">Hire Tarun</a>
          </div>
        </article>

        <!-- Freelancer 2 -->
        <article class="freelancer-card">
          <div>
            <h3>Varun Yadav</h3>
            <div class="freelancer-role">Front-End Web Developer</div>
            <p class="freelancer-desc">
              Builds responsive portfolio sites, landing pages and business websites
              using HTML, CSS and basic JavaScript.
            </p>
            <p class="freelancer-tags">
              HTML • CSS • JS • Responsive Design
            </p>
            <p class="freelancer-rate">Starting at ₹3000 per website</p>
          </div>
          <div class="freelancer-bottom">
            <span>⭐ 4.8 (90 reviews)</span>
            <a href="#post-project" class="btn btn-primary" style="padding:6px 12px;font-size:12px;">Hire Varun</a>
          </div>
        </article>

        <!-- Freelancer 3 -->
        <article class="freelancer-card">
          <div>
            <h3>Kanishk Yadav</h3>
            <div class="freelancer-role">Full-Stack Web Developer</div>
            <p class="freelancer-desc">
              E-commerce and custom web apps with clean UI and simple admin panels.
            </p>
            <p class="freelancer-tags">
              HTML • CSS • JavaScript • Node.js
            </p>
            <p class="freelancer-rate">Starting at ₹8000 per project</p>
          </div>
          <div class="freelancer-bottom">
            <span>⭐ 5.0 (50 reviews)</span>
            <a href="#post-project" class="btn btn-primary" style="padding:6px 12px;font-size:12px;">Hire Kanishk</a>
          </div>
        </article>

        <!-- Freelancer 4 -->
        <article class="freelancer-card">
          <div>
            <h3>Shruti Mehta</h3>
            <div class="freelancer-role">Graphic Designer & Thumbnail Artist</div>
            <p class="freelancer-desc">
              Eye-catching YouTube thumbnails, logos and social media posts that
              boost clicks and engagement.
            </p>
            <p class="freelancer-tags">
              Photoshop • Illustrator • Canva
            </p>
            <p class="freelancer-rate">Starting at ₹500 per design</p>
          </div>
          <div class="freelancer-bottom">
            <span>⭐ 4.7 (75 reviews)</span>
            <a href="#post-project" class="btn btn-primary" style="padding:6px 12px;font-size:12px;">Hire Shruti</a>
          </div>
        </article>

      </div>
    </section>


    <section id="how-it-works">
      <h2 class="section-title">How It Works</h2>
      <p class="section-subtitle">
        Simple 3-step process to get your project done.
      </p>

      <div class="steps">
        <div class="step">
          <div class="step-number">1</div>
          <h3>Post Your Project</h3>
          <p>
            Tell us what you need: video editing, website, logo, or anything else.
            Share budget, timeline and requirements.
          </p>
        </div>
        <div class="step">
          <div class="step-number">2</div>
          <h3>Get Proposals</h3>
          <p>
            Freelancers will send you offers. Compare portfolios, ratings and prices
            before you choose.
          </p>
        </div>
        <div class="step">
          <div class="step-number">3</div>
          <h3>Hire & Get Work Done</h3>
          <p>
            Chat with your freelancer, share files and get your final work delivered
            on time.
          </p>
        </div>
      </div>
    </section>

   
    <section id="post-project">
      <h2 class="section-title">Post a Project</h2>
      <p class="section-subtitle">
        Fill this form and we’ll match you with the best freelancers.
      </p>

      <form class="project-form">
        <div class="form-field">
          <label for="name">Your Name</label>
          <input id="name" type="text" placeholder="Enter your name">
        </div>

        <div class="form-field">
          <label for="email">Email</label>
          <input id="email" type="email" placeholder="you@example.com">
        </div>

        <div class="form-field">
          <label for="project-type">Project Type</label>
          <select id="project-type">
            <option>Video Editing</option>
            <option>Web Development</option>
            <option>Graphic Design</option>
            <option>Social Media Management</option>
            <option>Other</option>
          </select>
        </div>

        <div class="form-field">
          <label for="budget">Approx Budget (₹)</label>
          <input id="budget" type="text" placeholder="e.g. 2000 - 5000">
        </div>

        <div class="form-field form-full-width">
          <label for="details">Project Details</label>
          <textarea id="details" placeholder="Describe your project, goals, style preference, deadline, etc."></textarea>
        </div>

        <div class="form-field form-full-width">
          <button type="submit" class="btn btn-primary">Submit Project</button>
        </div>
      </form>
    </section>

  </main>

 
  <footer>
    © 2025 FreelanceHub. Built with basic HTML & CSS.  
    For freelancers: <a href="#post-project">want to be featured?</a>
  </footer>

</body>
</html>
