# curly-telegram
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Victory Website Storyboard</title>

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      font-family: Arial, Helvetica, sans-serif;
      background: #f4f8ff;
      color: #14213d;
      overflow-x: hidden;
    }

    /* =========================
       NAVIGATION
    ========================= */

    nav {
      position: fixed;
      top: 0;
      width: 100%;
      z-index: 1000;
      padding: 18px 7%;
      display: flex;
      justify-content: space-between;
      align-items: center;

      background: rgba(255, 255, 255, 0.85);
      backdrop-filter: blur(15px);
      border-bottom: 1px solid rgba(25, 90, 160, 0.1);
    }

    .logo {
      font-size: 1.5rem;
      font-weight: 800;
      color: #155eef;
    }

    .logo span {
      color: #08b6d8;
    }

    nav ul {
      display: flex;
      gap: 28px;
      list-style: none;
    }

    nav a {
      text-decoration: none;
      color: #14213d;
      font-weight: 600;
      transition: 0.3s;
    }

    nav a:hover {
      color: #08a9cc;
    }

    /* =========================
       HERO / HOME
    ========================= */

    .hero {
      min-height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      text-align: center;
      padding: 100px 20px 60px;

      background:
        radial-gradient(circle at 20% 20%, rgba(8,182,216,.18), transparent 30%),
        radial-gradient(circle at 80% 70%, rgba(21,94,239,.18), transparent 30%),
        linear-gradient(135deg, #ffffff, #edf5ff);
    }

    .hero-content {
      max-width: 850px;
      animation: heroIn 1.2s ease forwards;
    }

    .hero-logo {
      width: 90px;
      height: 90px;
      margin: 0 auto 25px;

      display: grid;
      place-items: center;

      border-radius: 25px;
      background: linear-gradient(135deg, #155eef, #08b6d8);
      color: white;
      font-size: 3rem;
      font-weight: bold;

      box-shadow: 0 20px 50px rgba(21,94,239,.25);
      animation: float 3s ease-in-out infinite;
    }

    .hero h1 {
      font-size: clamp(3rem, 8vw, 6rem);
      line-height: 1;
      margin-bottom: 25px;
    }

    .hero h1 span {
      color: #155eef;
    }

    .hero p {
      font-size: 1.2rem;
      color: #52627a;
      max-width: 650px;
      margin: auto;
      line-height: 1.7;
    }

    .button {
      display: inline-block;
      margin-top: 35px;
      padding: 15px 30px;
      border-radius: 50px;

      background: #155eef;
      color: white;
      text-decoration: none;
      font-weight: bold;

      box-shadow: 0 10px 30px rgba(21,94,239,.25);
      transition: .3s;
    }

    .button:hover {
      transform: translateY(-5px);
      background: #08a9cc;
      box-shadow: 0 15px 35px rgba(8,169,204,.3);
    }

    /* =========================
       GENERAL SECTIONS
    ========================= */

    section {
      padding: 110px 7%;
    }

    .section-title {
      text-align: center;
      margin-bottom: 60px;
    }

    .section-title small {
      color: #08a9cc;
      font-weight: bold;
      text-transform: uppercase;
      letter-spacing: 3px;
    }

    .section-title h2 {
      font-size: 3rem;
      margin-top: 10px;
    }

    .section-title p {
      color: #68778f;
      margin-top: 15px;
    }

    /* =========================
       ABOUT
    ========================= */

    .about {
      background: white;
    }

    .about-grid {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 25px;
      max-width: 1000px;
      margin: auto;
    }

    .card {
      background: white;
      padding: 35px;
      border-radius: 25px;

      border: 1px solid #e3ebf7;

      box-shadow: 0 15px 40px rgba(20,33,61,.07);

      transition: .4s;
      opacity: 0;
      transform: translateY(40px);
    }

    .card.show {
      opacity: 1;
      transform: translateY(0);
    }

    .card:hover {
      transform: translateY(-10px);
      border-color: #08b6d8;
      box-shadow: 0 20px 50px rgba(21,94,239,.13);
    }

    .icon {
      width: 55px;
      height: 55px;
      border-radius: 16px;

      display: grid;
      place-items: center;

      background: #e9f8fc;
      color: #08a9cc;

      font-size: 1.5rem;
      margin-bottom: 20px;
    }

    .card h3 {
      margin-bottom: 12px;
      font-size: 1.4rem;
    }

    .card p {
      color: #68778f;
      line-height: 1.7;
    }

    /* =========================
       PURPOSE
    ========================= */

    .purpose {
      background: #eef5ff;
    }

    .purpose-grid {
      max-width: 1100px;
      margin: auto;

      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 25px;
    }

    .purpose-card {
      padding: 40px 30px;
      text-align: center;

      border-radius: 25px;
      background: white;

      box-shadow: 0 15px 40px rgba(20,33,61,.08);

      transition: .4s;
      opacity: 0;
      transform: scale(.9);
    }

    .purpose-card.show {
      opacity: 1;
      transform: scale(1);
    }

    .purpose-card:hover {
      transform: scale(1.05);
    }

    .number {
      font-size: 3rem;
      font-weight: 900;
      color: #155eef;
      margin-bottom: 15px;
    }

    /* =========================
       AUDIENCE
    ========================= */

    .audience {
      background: white;
    }

    .audience-container {
      max-width: 1000px;
      margin: auto;
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 30px;
    }

    .audience-box {
      padding: 40px;
      border-radius: 25px;

      background: linear-gradient(135deg, #155eef, #08b6d8);
      color: white;

      position: relative;
      overflow: hidden;

      opacity: 0;
      transform: translateX(-40px);
      transition: .8s;
    }

    .audience-box:nth-child(2) {
      transform: translateX(40px);
    }

    .audience-box.show {
      opacity: 1;
      transform: translateX(0);
    }

    .audience-box::after {
      content: "";
      position: absolute;
      width: 200px;
      height: 200px;
      border-radius: 50%;
      background: rgba(255,255,255,.1);
      right: -70px;
      bottom: -70px;
    }

    .audience-box h3 {
      font-size: 1.8rem;
      margin-bottom: 15px;
    }

    .audience-box p {
      line-height: 1.7;
      opacity: .9;
    }

    /* =========================
       SERVICES
    ========================= */

    .services {
      background: #f4f8ff;
    }

    .services-grid {
      max-width: 1100px;
      margin: auto;

      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 25px;
    }

    .service {
      padding: 35px;
      border-radius: 25px;

      background: white;
      border: 1px solid #e2eaf5;

      transition: .4s;

      opacity: 0;
      transform: translateY(40px);
    }

    .service.show {
      opacity: 1;
      transform: translateY(0);
    }

    .service:hover {
      transform: translateY(-12px);
      box-shadow: 0 20px 50px rgba(21,94,239,.15);
    }

    .service h3 {
      margin-bottom: 12px;
      color: #155eef;
    }

    .service p {
      color: #68778f;
      line-height: 1.6;
    }

    /* =========================
       STORYBOARD FLOW
    ========================= */

    .storyboard {
      background: #101c35;
      color: white;
    }

    .storyboard .section-title p {
      color: #aebbd1;
    }

    .flow {
      max-width: 1100px;
      margin: auto;

      display: flex;
      justify-content: center;
      align-items: center;
      flex-wrap: wrap;
      gap: 15px;
    }

    .flow-box {
      padding: 20px 30px;
      border-radius: 18px;

      background: #17294b;
      border: 1px solid #2b4673;

      color: white;
      font-weight: bold;

      position: relative;
      transition: .3s;
    }

    .flow-box:hover {
      background: #155eef;
      transform: translateY(-8px);
    }

    .arrow {
      color: #08b6d8;
      font-size: 2rem;
      animation: pulse 1.5s infinite;
    }

    /* =========================
       FOOTER
    ========================= */

    footer {
      text-align: center;
      padding: 40px;
      background: #0b1428;
      color: #8e9bb2;
    }

    footer strong {
      color: #08b6d8;
    }

    /* =========================
       ANIMATIONS
    ========================= */

    @keyframes heroIn {
      from {
        opacity: 0;
        transform: translateY(40px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    @keyframes float {
      0%, 100% {
        transform: translateY(0);
      }

      50% {
        transform: translateY(-15px);
      }
    }

    @keyframes pulse {
      0%, 100% {
        opacity: .5;
        transform: translateX(0);
      }

      50% {
        opacity: 1;
        transform: translateX(5px);
      }
    }

    /* =========================
       MOBILE
    ========================= */

    @media (max-width: 800px) {

      nav ul {
        display: none;
      }

      .about-grid,
      .audience-container,
      .purpose-grid,
      .services-grid {
        grid-template-columns: 1fr;
      }

      section {
        padding: 80px 5%;
      }

      .section-title h2 {
        font-size: 2.3rem;
      }

      .flow {
        flex-direction: column;
      }

      .arrow {
        transform: rotate(90deg);
      }
    }
  </style>
</head>

<body>

  <!-- =========================
       NAVIGATION
  ========================== -->

  <nav>
    <div class="logo">
      V<span>ICTORY</span>
    </div>

    <ul>
      <li><a href="#home">Home</a></li>
      <li><a href="#about">About</a></li>
      <li><a href="#purpose">Purpose</a></li>
      <li><a href="#audience">Audience</a></li>
      <li><a href="#services">Services</a></li>
    </ul>
  </nav>


  <!-- =========================
       HOME
  ========================== -->

  <section class="hero" id="home">

    <div class="hero-content">

      <div class="hero-logo">
        V
      </div>

      <h1>
        Welcome to <span>Victory</span>
      </h1>

      <p>
        A modern website designed to provide useful,
        accurate and easy-to-understand information
        for visitors looking for answers and services.
      </p>

      <a href="#about" class="button">
        Explore the Website ↓
      </a>

    </div>

  </section>


  <!-- =========================
       ABOUT
  ========================== -->

  <section class="about" id="about">

    <div class="section-title">
      <small>01 — About</small>
      <h2>About the Page</h2>
      <p>Get to know what the website is all about.</p>
    </div>

    <div class="about-grid">

      <div class="card reveal">
        <div class="icon">ℹ</div>
        <h3>What is Victory?</h3>
        <p>
          Victory is an information-based website
          created to help visitors quickly understand
          important topics and available services.
        </p>
      </div>

      <div class="card reveal">
        <div class="icon">👥</div>
        <h3>Who We Are</h3>
        <p>
          This section introduces the website,
          its goals, and the people behind the
          information presented.
        </p>
      </div>

      <div class="card reveal">
        <div class="icon">🔗</div>
        <h3>Helpful Links</h3>
        <p>
          Visitors can follow trusted external links
          when they need more detailed information.
        </p>
      </div>

      <div class="card reveal">
        <div class="icon">✓</div>
        <h3>Reliable Information</h3>
        <p>
          Information is organized clearly so users
          can find what they need without confusion.
        </p>
      </div>

    </div>

  </section>


  <!-- =========================
       PURPOSE
  ========================== -->

  <section class="purpose" id="purpose">

    <div class="section-title">
      <small>02 — Purpose</small>
      <h2>Why This Website Exists</h2>
      <p>The three main purposes shown in your storyboard.</p>
    </div>

    <div class="purpose-grid">

      <div class="purpose-card reveal">
        <div class="number">01</div>
        <h3>To Inform</h3>
        <p>
          Give visitors useful information
          about the topic.
        </p>
      </div>

      <div class="purpose-card reveal">
        <div class="number">02</div>
        <h3>To Attract</h3>
        <p>
          Create an attractive and engaging
          website that encourages visitors
          to explore.
        </p>
      </div>

      <div class="purpose-card reveal">
        <div class="number">03</div>
        <h3>To Provide Facts</h3>
        <p>
          Present factual and trustworthy
          information in an easy-to-read way.
        </p>
      </div>

    </div>

  </section>


  <!-- =========================
       AUDIENCE
  ========================== -->

  <section class="audience" id="audience">

    <div class="section-title">
      <small>03 — Audience</small>
      <h2>Who Is It For?</h2>
      <p>Designed around the needs of potential visitors.</p>
    </div>

    <div class="audience-container">

      <div class="audience-box reveal">
        <h3>Potential Readers</h3>
        <p>
          People who want to learn more about
          the topic and are looking for clear,
          useful information.
        </p>
      </div>

      <div class="audience-box reveal">
        <h3>People Seeking Information</h3>
        <p>
          Visitors who already have questions
          and need reliable information or
          helpful resources.
        </p>
      </div>

    </div>

  </section>


  <!-- =========================
       SERVICES
  ========================== -->

  <section class="services" id="services">

    <div class="section-title">
      <small>04 — Services</small>
      <h2>What We Offer</h2>
      <p>Useful resources and information for visitors.</p>
    </div>

    <div class="services-grid">

      <div class="service reveal">
        <h3>Information</h3>
        <p>
          Easy-to-understand information
          organized into useful sections.
        </p>
      </div>

      <div class="service reveal">
        <h3>Helpful Resources</h3>
        <p>
          Links and resources that direct
          users toward better and more detailed
          information.
        </p>
      </div>

      <div class="service reveal">
        <h3>Guidance</h3>
        <p>
          Simple guidance to help visitors
          find the information they need.
        </p>
      </div>

    </div>

  </section>


  <!-- =========================
       STORYBOARD FLOW
  ========================== -->

  <section class="storyboard">

    <div class="section-title">
      <small>Website Storyboard</small>
      <h2>Navigation Flow</h2>
      <p>
        This represents the structure of your
        original hand-drawn site diagram.
      </p>
    </div>

    <div class="flow">

      <div class="flow-box">
        HOME
      </div>

      <div class="arrow">
        →
      </div>

      <div class="flow-box">
        ABOUT
      </div>

      <div class="arrow">
        →
      </div>

      <div class="flow-box">
        PURPOSE
      </div>

      <div class="arrow">
        →
      </div>

      <div class="flow-box">
        AUDIENCE
      </div>

      <div class="arrow">
        →
      </div>

      <div class="flow-box">
        SERVICES
      </div>

    </div>

  </section>


  <!-- =========================
       FOOTER
  ========================== -->

  <footer>
    <p>
      © 2026 <strong>Victory</strong> — Information Website
    </p>
  </footer>


  <!-- =========================
       JAVASCRIPT ANIMATIONS
  ========================== -->

  <script>

    /*
      Scroll Reveal Animation
    */

    const elements =
      document.querySelectorAll(".reveal");

    const observer =
      new IntersectionObserver(
        (entries) => {

          entries.forEach(entry => {

            if (entry.isIntersecting) {

              entry.target.classList.add("show");

            }

          });

        },
        {
          threshold: 0.15
        }
      );


    elements.forEach(element => {
      observer.observe(element);
    });


    /*
      Add a small stagger effect
      to cards.
    */

    document.querySelectorAll(".card").forEach(
      (card, index) => {

        card.style.transitionDelay =
          `${index * 0.12}s`;

      }
    );


    document.querySelectorAll(".purpose-card").forEach(
      (card, index) => {

        card.style.transitionDelay =
          `${index * 0.15}s`;

      }
    );


    document.querySelectorAll(".service").forEach(
      (service, index) => {

        service.style.transitionDelay =
          `${index * 0.12}s`;

      }
    );


    /*
      Change navigation background
      when scrolling.
    */

    const nav = document.querySelector("nav");

    window.addEventListener("scroll", () => {

      if (window.scrollY > 50) {

        nav.style.boxShadow =
          "0 10px 30px rgba(20,33,61,.08)";

      } else {

        nav.style.boxShadow = "none";

      }

    });

  </script>

</body>
</html>
