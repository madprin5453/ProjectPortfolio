<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Madan Lal | Portfolio</title>

    <style>

        /* =====================================================
           RESET
        ===================================================== */
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
            background: #aaa;
            color: #111;
        }

        a {
            text-decoration: none;
            color: inherit;
        }

        /* =====================================================
           MAIN WRAPPER
        ===================================================== */

        .page {
            width: 100%;
        }

        /* =====================================================
           NAVIGATION
        ===================================================== */
        .navbar {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 65px;
            background: rgba(255,255,255,0.96);
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 0 7%;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0,0,0,0.15);
        }

        .logo {
            font-size: 18px;
            font-weight: 900;
            letter-spacing: -1px;
        }

        .logo span {
            color: #ffd33f;
        }

        .nav-links {
            display: flex;
            gap: 30px;
            list-style: none;
        }

        .nav-links a {
            font-size: 11px;
            font-weight: 800;
            text-transform: uppercase;
            position: relative;
            transition: 0.3s ease;
        }

        .nav-links a::after {
            content: "";
            position: absolute;
            width: 0;
            height: 3px;
            left: 0;
            bottom: -6px;
            background: #ffd33f;
            transition: width 0.3s ease;
        }

        .nav-links a:hover::after {
            width: 100%;
        }

        /* =====================================================
           GENERAL SECTION
        ===================================================== */
        section {
            width: 100%;
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 100px 7%;
        }

        .container {
            width: 100%;
            max-width: 1100px;
            margin: auto;
        }

        /* =====================================================
           SECTION TITLE
        ===================================================== */
        .section-heading {
            font-size: 45px;
            font-weight: 900;
            letter-spacing: -3px;
            margin-bottom: 20px;
        }

        .section-heading span {
            position: relative;
        }

        .section-heading span::after {
            content: "";
            position: absolute;
            width: 45px;
            height: 5px;
            background: #ffd33f;
            left: 0;
            bottom: -8px;
        }

        /* =====================================================
           HERO / PORTFOLIO
        ===================================================== */
        #home {
            background: #ffd33f;
            min-height: 100vh;
            padding-top: 65px;
            position: relative;
            overflow: hidden;
        }

        .hero {
            min-height: calc(100vh - 65px);
            display: flex;
            align-items: center;
            justify-content: space-between;
            gap: 50px;
        }

        .hero-left {
            width: 55%;
        }

        .small-title {
            font-size: 16px;
            font-weight: 800;
            letter-spacing: 2px;
            margin-bottom: 20px;
        }

        .hero-title {
            font-size: clamp(80px, 12vw, 160px);
            line-height: 0.78;
            font-weight: 900;
            letter-spacing: -5px;
        }

        .hero-title span {
            display: block;
        }

        .hero-description {
            max-width: 450px;
            margin-top: 35px;
            font-size: 13px;
            line-height: 1.7;
        }

        .hero-button {
            display: inline-block;
            margin-top: 30px;
            background: #111;
            color: #fff;
            padding: 13px 25px;
            font-size: 11px;
            font-weight: 900;
            text-transform: uppercase;
            transition:
                transform 0.3s ease,
                background 0.3s ease;
        }

        .hero-button:hover {
            transform: translateY(-5px);
            background: #333;
        }

        /* =====================================================
           HERO DECORATION
        ===================================================== */
        .hero-right {
            width: 40%;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .hero-shape {
            width: 330px;
            height: 330px;
            background: #fff;
            border-radius: 50%;
            position: relative;
            display: flex;
            justify-content: center;
            align-items: center;
            box-shadow: 0 15px 30px rgba(0,0,0,0.15);
            transition: transform 0.5s ease;
        }

        .hero-shape:hover {
            transform: rotate(5deg) scale(1.03);
        }

        .hero-shape::before {
            content: "✳";
            position: absolute;
            top: -50px;
            right: -25px;
            font-size: 65px;
        }

        .hero-name {
            font-size: 40px;
            font-weight: 900;
            text-align: center;
            line-height: 0.9;
            letter-spacing: -3px;
        }

        /* =====================================================
           ABOUT SECTION
        ===================================================== */
        #about {
            background: #fff;
        }

        .about-grid {
            display: grid;
            grid-template-columns:
                1fr 1.4fr;
            gap: 70px;
            align-items: center;
        }

        .profile-box {
            background: #ffd33f;
            width: 100%;
            max-width: 400px;
            height: 420px;
            display: flex;
            justify-content: center;
            align-items: flex-end;
            position: relative;
            margin: auto;
            overflow: hidden;
            transition: transform 0.4s ease;
        }

        .profile-box:hover {
            transform: translateY(-8px);
        }

        .profile-box::before {
            content: "✳";
            position: absolute;
            top: 25px;
            left: 25px;
            font-size: 55px;
        }

        /* CSS profile placeholder */
        .person {
            width: 230px;
            height: 350px;
            position: relative;
        }

        .person-head {
            position: absolute;
            width: 105px;
            height: 105px;
            border-radius: 50%;
            background: #d69b72;
            top: 10px;
            left: 63px;
            z-index: 2;
        }

        .person-hair {
            position: absolute;
            width: 110px;
            height: 75px;
            background: #222;
            border-radius: 55% 55% 25% 25%;
            top: 0;
            left: 60px;
            z-index: 3;
        }

        .person-body {
            position: absolute;
            width: 175px;
            height: 190px;
            background: #f2f2f2;
            border-radius: 45px 45px 5px 5px;
            left: 28px;
            bottom: 0;
        }

        .person-arm {
            position: absolute;
            width: 42px;
            height: 155px;
            background: #eee;
            border-radius: 30px;
            bottom: 20px;
            z-index: 4;
        }

        .arm-left {
            left: 17px;
            transform: rotate(22deg);
        }

        .arm-right {
            right: 17px;
            transform: rotate(-22deg);
        }

        .about-content h2 {
            font-size: 45px;
            font-weight: 900;
            letter-spacing: -3px;
            margin-bottom: 10px;
        }

        .role {
            font-size: 14px;
            font-weight: 800;
            margin-bottom: 20px;
        }

        .about-text {
            font-size: 13px;
            line-height: 1.8;
            color: #333;
            max-width: 600px;
        }

        .education {
            margin-top: 35px;
        }

        .education h3 {
            font-size: 18px;
            font-weight: 900;
            margin-bottom: 15px;
        }

        .education-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 20px;
        }

        .education-item {
            border-left: 5px solid #ffd33f;
            padding-left: 15px;
        }

        .education-item strong {
            display: block;
            font-size: 12px;
            margin-bottom: 5px;
        }

        .education-item span {
            font-size: 11px;
            color: #555;
        }

        /* =====================================================
           SKILLS SECTION
        ===================================================== */
        #skills {
            background: #ffd33f;
        }

        .skills-grid {
            display: grid;
            grid-template-columns:
                1fr 1fr;
            gap: 80px;
        }

        .skills-list {
            margin-top: 30px;
        }

        .skill {
            margin-bottom: 25px;
        }

        .skill-top {
            display: flex;
            justify-content: space-between;
            margin-bottom: 7px;
        }

        .skill-top strong {
            font-size: 12px;
        }

        .skill-top span {
            font-size: 11px;
            font-weight: 800;
        }

        .skill-bar {
            width: 100%;
            height: 10px;
            background: #fff;
        }

        .skill-progress {
            height: 100%;
            background: #111;
            transition: width 1s ease;
        }

        .skill:hover .skill-progress {
            background: #444;
        }

        .skill:nth-child(1) .skill-progress {
            width: 95%;
        }

        .skill:nth-child(2) .skill-progress {
            width: 90%;
        }

        .skill:nth-child(3) .skill-progress {
            width: 85%;
        }

        .skill:nth-child(4) .skill-progress {
            width: 80%;
        }

        .skill:nth-child(5) .skill-progress {
            width: 75%;
        }

        /* =====================================================
           SKILLS RIGHT SIDE
        ===================================================== */
        .skills-info {
            background: #fff;
            padding: 35px;
            box-shadow: 0 8px 20px rgba(0,0,0,0.12);
        }

        .skills-info h3 {
            font-size: 25px;
            font-weight: 900;
            margin-bottom: 20px;
        }

        .skills-info p {
            font-size: 12px;
            line-height: 1.7;
            color: #333;
        }

        .skill-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
            margin-top: 25px;
        }

        .skill-tag {
            background: #111;
            color: #fff;
            padding: 8px 12px;
            font-size: 9px;
            font-weight: 800;
            transition:
                transform 0.3s ease,
                background 0.3s ease;
        }

        .skill-tag:hover {
            background: #555;
            transform: translateY(-3px);
        }

        /* =====================================================
           PROJECTS SECTION
        ===================================================== */
        #projects {
            background: #fff;
        }

        .projects-header {
            display: flex;
            justify-content: space-between;
            align-items: flex-end;
            margin-bottom: 35px;
        }

        .projects-header p {
            max-width: 350px;
            font-size: 12px;
            line-height: 1.6;
        }

        .projects-grid {
            display: grid;
            grid-template-columns:
                repeat(3, 1fr);
            gap: 20px;
        }

        .project-card {
            background: #ffd33f;
            min-height: 320px;
            padding: 25px;
            position: relative;
            overflow: hidden;
            transition:
                transform 0.4s ease,
                box-shadow 0.4s ease;
        }

        .project-card:hover {
            transform: translateY(-10px);
            box-shadow:
                0 15px 25px rgba(0,0,0,0.18);
        }

        .project-number {
            font-size: 13px;
            font-weight: 900;
            margin-bottom: 40px;
        }

        .project-icon {
            width: 90px;
            height: 90px;
            background: #fff;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 35px;
            margin-bottom: 30px;
            transition: transform 0.4s ease;
        }

        .project-card:hover .project-icon {
            transform: rotate(8deg);
        }

        .project-card h3 {
            font-size: 22px;
            font-weight: 900;
            letter-spacing: -1px;
            margin-bottom: 10px;
        }

        .project-card p {
            font-size: 10px;
            line-height: 1.6;
        }

        .project-link {
            position: absolute;
            bottom: 20px;
            right: 20px;
            width: 35px;
            height: 35px;
            background: #111;
            color: #fff;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 14px;
            transition: transform 0.3s ease;
        }

        .project-link:hover {
            transform: rotate(45deg);
        }

        /* =====================================================
           CONTACT SECTION
        ===================================================== */
        #contact {
            background: #ffd33f;
        }

        .contact-grid {
            display: grid;
            grid-template-columns:
                1.2fr 1fr;
            gap: 70px;
            align-items: stretch;
        }

        .contact-left {
            background: #fff;
            padding: 45px;
        }

        .contact-left h2 {
            font-size: 55px;
            line-height: 0.9;
            font-weight: 900;
            letter-spacing: -4px;
            margin-bottom: 25px;
        }

        .contact-left p {
            font-size: 12px;
            line-height: 1.7;
            color: #333;
            max-width: 450px;
        }

        .contact-details {
            margin-top: 35px;
        }

        .contact-item {
            margin-bottom: 20px;
        }

        .contact-item strong {
            display: block;
            font-size: 11px;
            margin-bottom: 4px;
        }

        .contact-item span {
            font-size: 12px;
            color: #444;
        }

        .contact-button {
            display: inline-block;
            margin-top: 15px;
            background: #111;
            color: #fff;
            padding: 13px 22px;
            font-size: 10px;
            font-weight: 900;
            text-transform: uppercase;
            transition:
                transform 0.3s ease,
                background 0.3s ease;
        }

        .contact-button:hover {
            transform: translateY(-5px);
            background: #333;
        }

        /* =====================================================
           CONTACT TESTIMONIAL
        ===================================================== */
        .contact-right {
            background: #fff;
            display: flex;
            flex-direction: column;
        }

        .testimonial-area {
            background: #ffd33f;
            padding: 35px;
            flex: 1;
        }

        .testimonial-area h3 {
            font-size: 27px;
            font-weight: 900;
            margin-bottom: 25px;
        }

        .testimonial {
            margin-bottom: 25px;
        }

        .testimonial p {
            font-size: 10px;
            line-height: 1.6;
            margin-bottom: 7px;
        }

        .testimonial strong {
            font-size: 10px;
        }

        .contact-bottom {
            padding: 25px;
            background: #fff;
        }

        .contact-bottom h3 {
            font-size: 15px;
            font-weight: 900;
            margin-bottom: 15px;
        }

        .socials {
            display: flex;
            gap: 10px;
            flex-wrap: wrap;
        }

        .social {
            padding: 8px 12px;
            background: #111;
            color: #fff;
            font-size: 9px;
            font-weight: 800;
            transition:
                transform 0.3s ease,
                background 0.3s ease;
        }

        .social:hover {
            transform: translateY(-3px);
            background: #444;
        }

        /* =====================================================
           FOOTER
        ===================================================== */
        footer {
            background: #111;
            color: #fff;
            padding: 25px;
            text-align: center;
            font-size: 10px;
        }

        /* =====================================================
           TABLET
        ===================================================== */
        @media (max-width: 900px) {

            section {
                padding:
                    100px 6%;
            }

            .hero {
                flex-direction: column;
                justify-content: center;
                text-align: center;
            }

            .hero-left,
            .hero-right {
                width: 100%;
            }

            .hero-description {
                margin-left: auto;
                margin-right: auto;
            }

            .about-grid,
            .skills-grid,
            .contact-grid {
                grid-template-columns: 1fr;
                gap: 40px;
            }

            .profile-box {
                max-width: 350px;
            }

            .projects-grid {
                grid-template-columns:
                    repeat(2, 1fr);
            }

            .projects-header {
                display: block;
            }

            .projects-header p {
                margin-top: 15px;
            }

        }

        /* =====================================================
           MOBILE
        ===================================================== */
        @media (max-width: 600px) {

            .navbar {
                height: auto;
                min-height: 60px;
                padding:
                    12px 5%;
                flex-direction: column;

                gap: 10px;
            }

            .nav-links {
                gap: 15px;
                flex-wrap: wrap;
                justify-content: center;
            }

            .nav-links a {
                font-size: 8px;
            }

            section {
                min-height: auto;
                padding:
                    90px 6% 70px;
            }

            #home {
                min-height: 100vh;
            }

            .hero-title {
                font-size:
                    clamp(65px, 20vw, 100px);
                letter-spacing: -7px;
            }

            .hero-shape {
                width: 250px;
                height: 250px;
            }

            .hero-name {
                font-size: 32px;
            }

            .section-heading {
                font-size: 38px;
            }

            .about-content h2 {
                font-size: 38px;
            }

            .education-grid {
                grid-template-columns: 1fr;
            }

            .skills-grid {
                gap: 30px;
            }

            .skills-info {
                padding: 25px;
            }

            .projects-grid {
                grid-template-columns: 1fr;
            }

            .project-card {
                min-height: 300px;
            }

            .contact-left {
                padding: 30px;
            }

            .contact-left h2 {
                font-size: 45px;
            }

            .contact-right {
                min-height: 500px;
            }

        }

        /* =====================================================
           VERY SMALL MOBILE
        ===================================================== */
        @media (max-width: 380px) {

            .hero-title {
                font-size: 62px;
            }

            .hero-shape {
                width: 220px;
                height: 220px;
            }

            .profile-box {
                height: 350px;
            }

        }

    </style>
</head>
<body>

<div class="page">

    <!-- =====================================================
         NAVIGATION
    ====================================================== -->
    <nav class="navbar">

        <a href="#home" class="logo">
            Madan Lal<span>.</span>
        </a>

        <ul class="nav-links">

            <li>
                <a href="#home">Home</a>
            </li>

            <li>
                <a href="#about">About</a>
            </li>

            <li>
                <a href="#skills">Skills</a>
            </li>

            <li>
                <a href="#projects">Projects</a>
            </li>

            <li>
                <a href="#contact">Contact</a>
            </li>

        </ul>

    </nav>

    <!-- =====================================================
         01 — HERO / PORTFOLIO
    ====================================================== -->

    <section id="home">

        <div class="container hero">

            <div class="hero-left">

                <div class="small-title">
                    CREATIVE PORTFOLIO
                </div>

                <h1 class="hero-title">

                    <span>Port</span>
                    <span>folio</span>

                </h1>

                <p class="hero-description">

                    Welcome to my personal portfolio.
                    I create modern digital experiences by
                    combining creativity, design and technology.

                </p>

                <a
                    href="#about"
                    class="hero-button">

                    Explore Portfolio

                </a>

            </div>


            <div class="hero-right">

                <div class="hero-shape">

                    <div class="hero-name">

                        Madan<br>
                        Lal

                    </div>

                </div>

            </div>


        </div>

    </section>

    <!-- =====================================================
         02 — ABOUT
    ====================================================== -->
    <section id="about">

        <div class="container about-grid">


            <!-- Profile -->
            <div class="profile-box">

                <div class="person">

                    <div class="person-hair"></div>

                    <div class="person-head"></div>

                    <div class="person-body"></div>

                    <div class="person-arm arm-left"></div>

                    <div class="person-arm arm-right"></div>

                </div>

            </div>

            <!-- About Content -->
            <div class="about-content">

                <h2>
                    About Me
                </h2>


                <div class="role">
                    Creative Designer & Developer
                </div>


                <p class="about-text">

                    I am a passionate creative professional
                    specializing in modern web design,
                    user interfaces and digital experiences.

                    <br><br>

                    My goal is to create websites that are
                    visually impressive, easy to use and
                    responsive across all devices.

                    <br><br>

                    I enjoy turning complex ideas into simple,
                    beautiful and functional experiences.

                </p>


                <div class="education">

                    <h3>
                        Education
                    </h3>


                    <div class="education-grid">

                        <div class="education-item">

                            <strong>
                                Bachelor Degree
                            </strong>

                            <span>
                                Computer Systems Engineering
                                <br>
                                2022 - 2026
                            </span>

                        </div>


                        <div class="education-item">

                            <strong>
                                Master Degree
                            </strong>

                            <span>
                                Data Science & Artificial Intelligence
                                <br>
                                2026 - 2028
                            </span>

                        </div>

                    </div>

                </div>

            </div>


        </div>

    </section>

    <!-- =====================================================
         03 — SKILLS
    ====================================================== -->
    <section id="skills">

        <div class="container skills-grid">

            <!-- Skills -->
            <div>

                <h2 class="section-heading">

                    <span>
                        Skills
                    </span>

                </h2>

                <div class="skills-list">

                    <div class="skill">

                        <div class="skill-top">

                            <strong>
                                HTML & CSS
                            </strong>

                            <span>
                                95%
                            </span>

                        </div>

                        <div class="skill-bar">

                            <div class="skill-progress"></div>

                        </div>

                    </div>

                    <div class="skill">

                        <div class="skill-top">

                            <strong>
                                JavaScript
                            </strong>

                            <span>
                                90%
                            </span>

                        </div>

                        <div class="skill-bar">

                            <div class="skill-progress"></div>

                        </div>

                    </div>

                    <div class="skill">

                        <div class="skill-top">

                            <strong>
                                UI / UX Design
                            </strong>

                            <span>
                                85%
                            </span>

                        </div>

                        <div class="skill-bar">

                            <div class="skill-progress"></div>

                        </div>

                    </div>

                    <div class="skill">

                        <div class="skill-top">

                            <strong>
                                React
                            </strong>

                            <span>
                                80%
                            </span>

                        </div>

                        <div class="skill-bar">

                            <div class="skill-progress"></div>

                        </div>

                    </div>

                    <div class="skill">

                        <div class="skill-top">

                            <strong>
                                Graphic Design
                            </strong>

                            <span>
                                75%
                            </span>

                        </div>

                        <div class="skill-bar">

                            <div class="skill-progress"></div>

                        </div>

                    </div>


                </div>

            </div>

            <!-- Skills Information -->
            <div class="skills-info">

                <h3>
                    What I Do
                </h3>

                <p>

                    I design and develop modern digital
                    products with a strong focus on usability,
                    visual identity and responsive layouts.

                </p>

                <div class="skill-tags">

                    <div class="skill-tag">
                        Web Design
                    </div>

                    <div class="skill-tag">
                        Frontend
                    </div>

                    <div class="skill-tag">
                        UI Design
                    </div>

                    <div class="skill-tag">
                        UX Design
                    </div>

                    <div class="skill-tag">
                        Branding
                    </div>

                    <div class="skill-tag">
                        Responsive
                    </div>

                    <div class="skill-tag">
                        Prototyping
                    </div>

                    <div class="skill-tag">
                        Development
                    </div>

                </div>

            </div>

        </div>

    </section>

    <!-- =====================================================
         04 — PROJECTS
    ====================================================== -->
    <section id="projects">

        <div class="container">

            <div class="projects-header">

                <h2 class="section-heading">

                    <span>
                        Projects
                    </span>

                </h2>

                <p>

                    A selection of recent projects where
                    design, creativity and technology come
                    together to solve real problems.

                </p>

            </div>

            <div class="projects-grid">

                <!-- Project 01 -->
                <article class="project-card">

                    <div class="project-number">
                        PROJECT 01
                    </div>

                    <div class="project-icon">
                        ◈
                    </div>

                    <h3>
                        Portfolio Website
                    </h3>

                    <p>

                        A clean and responsive personal
                        portfolio designed to showcase
                        creative work and professional skills.

                    </p>

                    <a
                        href="#"
                        class="project-link">
                        →

                    </a>

                </article>

                <!-- Project 02 -->
                <article class="project-card">

                    <div class="project-number">
                        PROJECT 02
                    </div>

                    <div class="project-icon">
                        ◆
                    </div>

                    <h3>
                        E-Commerce
                    </h3>

                    <p>

                        A modern shopping experience with
                        intuitive navigation, product layouts
                        and responsive design.

                    </p>

                    <a
                        href="#"
                        class="project-link">
                        →

                    </a>

                </article>

                <!-- Project 03 -->
                <article class="project-card">

                    <div class="project-number">
                        PROJECT 03
                    </div>

                    <div class="project-icon">
                        ✦
                    </div>

                    <h3>
                        Dashboard UI
                    </h3>

                    <p>

                        A clean analytics dashboard designed
                        to make complex information easy to
                        understand.

                    </p>

                    <a
                        href="#"
                        class="project-link">
                        →

                    </a>

                </article>

            </div>

        </div>

    </section>

    <!-- =====================================================
         05 — CONTACT
    ====================================================== -->
    <section id="contact">

        <div class="container contact-grid">

            <!-- Contact Information -->
            <div class="contact-left">

                <h2>
                    Let's<br>
                    Work<br>
                    Together
                </h2>

                <p>

                    Have a project, idea or opportunity?
                    I'd love to hear from you.

                    Let's create something meaningful
                    together.

                </p>

                <div class="contact-details">

                    <div class="contact-item">

                        <strong>
                            Email
                        </strong>

                        <span>
                            hello@example.com
                        </span>

                    </div>

                    <div class="contact-item">

                        <strong>
                            Phone
                        </strong>

                        <span>
                            +123 456 7890
                        </span>

                    </div>

                    <div class="contact-item">

                        <strong>
                            Location
                        </strong>

                        <span>
                            Pakistan
                        </span>

                    </div>

                </div>

                <a
                    href="mailto:hello@example.com"
                    class="contact-button">

                    Send Message

                </a>

            </div>

            <!-- Testimonials -->
            <div class="contact-right">

                <div class="testimonial-area">

                    <h3>
                        Testimonials
                    </h3>

                    <div class="testimonial">

                        <p>

                            "Working with Madan Lal was an excellent
                            experience. His creativity and attention
                            to detail made the project successful."

                        </p>

                        <strong>
                            — Martina Villa
                        </strong>

                    </div>

                    <div class="testimonial">

                        <p>

                            "A talented designer with excellent
                            technical skills and a great eye for
                            modern design."

                        </p>

                        <strong>
                            — John Doe
                        </strong>

                    </div>

                    <div class="testimonial">

                        <p>

                            "Professional, creative and reliable.
                            I would definitely recommend her work."

                        </p>

                        <strong>
                            — Sarah Wilson
                        </strong>

                    </div>

                </div>

                <div class="contact-bottom">

                    <h3>
                        Connect With Me
                    </h3>

                    <div class="socials">

                        <a href="#" class="social">
                            LinkedIn
                        </a>

                        <a href="#" class="social">
                            GitHub
                        </a>

                        <a href="#" class="social">
                            Instagram
                        </a>

                        <a href="#" class="social">
                            Behance
                        </a>

                    </div>

                </div>

            </div>

        </div>

    </section>

    <!-- =====================================================
         FOOTER
    ====================================================== -->
    <footer>

        © 2026 Madan Lal — Portfolio Website

    </footer>

</div>

</body>
</html>
