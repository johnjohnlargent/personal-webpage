<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Personal Webpage</title>
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Roboto', sans-serif;
            font-style: italic;
            margin: 0;
            padding: 0;
            background-color: #ffffff;
            color: #000000;
        }
        header {
            padding: 1em 0;
            text-align: left;
            padding-left: 1em;
            position: relative;
        }
        header h1 {
            display: block;
            margin: 0;
            font-size: 1em; /* Reduced to half the original size */
            text-transform: uppercase;
            font-weight: 700;
            -webkit-font-smoothing: antialiased;
            color: #000000; /* Changed to black */
        }
        header h2 {
            display: inline-block;
            margin: 0;
            font-size: 1.5em; /* Reduced to half the original size */
            color: #000000;
            text-transform: uppercase;
            font-weight: 700;
            -webkit-font-smoothing: antialiased;
        }
        .john-largent {
            position: absolute;
            top: 0;
            left: calc(100% + 1em);
            font-size: 0.75em; /* Reduced to half the original size */
            color: #000000;
        }
        .marquee-container {
            width: 100vw;
            overflow: hidden;
            position: absolute;
            left: 0;
            background-color: #000000; /* Changed to black */
        }
        .marquee-text {
            font-size: 0.375em; /* Reduced to half the original size */
            color: #ffffff;
            text-align: left;
            font-weight: normal;
            text-transform: uppercase;
            animation: moveText 15s linear infinite;
            padding: 0.5em;
            white-space: nowrap;
            display: inline-block;
        }
        .marquee-content {
            display: inline-block;
        }
        @keyframes moveText {
            0% {
                transform: translateX(0);
            }
            100% {
                transform: translateX(-50%);
            }
        }
        .small-c {
            font-size: 0.25em; /* Reduced to half the original size */
        }
        .banner {
            text-align: left; /* Left align */
            padding: 0.5em 0; /* Updated padding */
            padding-left: 1em; /* Added padding-left to move it more to the left */
            border-bottom: 1px solid #ccc;
            font-size: 0.7em; /* Reduced to half the original size */
            margin-top: 2em; /* Adjusted margin-top to place it higher but not hidden */
        }
        .banner a {
            margin: 0 15px;
            text-decoration: none;
            color: #000000;
            font-weight: bold;
        }
        nav {
            text-align: center;
            padding: 1em 0;
        }
        nav a {
            color: #000000;
            margin: 0 15px;
            text-decoration: none;
        }
        section {
            padding: 2em;
            max-width: 800px;
            margin: auto;
            margin-top: 1em;
            position: relative;
        }
        section h2::first-letter {
            color: #000000;
        }
        footer {
            text-align: center;
            padding: 1em 0;
        }
        .project-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr); /* Updated to 3 columns */
            gap: 1em;
        }
        .project-cell {
            text-align: center;
            padding: 1em;
            box-sizing: border-box;
        }
        .project-title {
            font-size: 1.2em;
            margin-bottom: 0.5em;
        }
        .project-image, .project-video {
            width: 100%;
            padding-bottom: 100%;
            background-color: #e0e0e0;
            position: relative;
            background-size: cover;
            background-position: center;
            border: 1px solid #000000; /* Thin black border */
        }
        .project-video {
            padding: 0;
            overflow: hidden;
        }
        .project-video video {
            width: 176%;
            height: 100%;
            object-fit: cover;
        }
        .about-image {
            position: absolute;
            left: -19em;
            top: 130%;
            transform: translateY(-50%);
            width: 400px;
            height: auto;
        }
        .about-image:hover {
            content: url(![webpp2](https://github.com/johnjohnlargent/personal-webpage/assets/170893182/62ef915b-3899-4538-9cfe-2d70e0032d37));
        }
        @media only screen and (max-width: 768px) {
            .about-image {
                width: 300px;
                left: -14em;
                top: 140%;
            }
        }
        @media only screen and (max-width: 480px) {
            .about-image {
                width: 200px;
                left: -9em;
                top: 150%;
            }
        }
        .announcement {
            position: fixed;
            top: 20px;
            right: 20px;
            width: 250px;
            background-color: #f9f9f9;
            border: 1px solid #ccc;
            padding: 15px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            z-index: 1000;
            font-size: 0.875em; /* Slightly smaller text */
        }
        .announcement p {
            margin: 0;
        }
        .close-btn {
            position: absolute;
            top: 5px;
            right: 5px;
            cursor: pointer;
            font-size: 1.25em;
            line-height: 1;
        }
        .newsletter {
            background-color: #ffffff; /* White background */
            color: #000000; /* Black text */
            padding: 2em;
            text-align: center;
            min-height: 100vh; /* Ensure it takes the full viewport height */
        }
        .newsletter h2 {
            font-size: 2em; /* Larger font size for the title */
            margin-bottom: 1em;
        }
    </style>
    <script>
        function closeAnnouncement() {
            document.getElementById('announcement').style.display = 'none';
        }
        document.addEventListener('DOMContentLoaded', function() {
            var closeButton = document.querySelector('.close-btn');
            if (closeButton) {
                closeButton.addEventListener('click', closeAnnouncement);
                closeButton.addEventListener('pointerdown', closeAnnouncement);
            }
        });
    </script>
</head>
<body>
    <div id="announcement" class="announcement">
        <span class="close-btn" onclick="closeAnnouncement()">&times;</span>
        <p>For the best experience, please visit this website on a computer screen.</p>
    </div>
    <header>
        <h2>John John Largent</h2>
        <h1 style="margin-top: -2px;">
            <span>Creative Designer</span> 
            <span class="small-c" style="color: #000000;">MTL/BXL</span>
        </h1>
        <div class="marquee-container">
            <div class="marquee-text">
                <div class="marquee-content">
                    Hi, I'm John John Largent, a Creative Designer living between Montreal and Brussels. Welcome to my personal webpage! Here, you'll discover my creative vision, learn about my work, explore my professional background, and stay updated on my future projects. Feel free to get in touch!&nbsp;&nbsp;&nbsp;&nbsp;
                </div>
                <div class="marquee-content">
                    Hi, I'm John John Largent, a Creative Designer living between Montreal and Brussels. Welcome to my personal webpage! Here, you'll discover my creative vision, learn about my work, explore my professional background, and stay updated on my future projects. Feel free to get in touch!&nbsp;&nbsp;&nbsp;&nbsp;
                </div>
            </div>
        </div>
        <div class="banner">
            <a href="#newsletter-section">Newsletter</a>
        </div>
    </header>

    <section id="about">
        <img src="![webpp](https://github.com/johnjohnlargent/personal-webpage/assets/170893182/a50f732a-041f-4b4a-901a-5e27cb4d7227)" alt="About Me Image" class="about-image">
        <h2>About Me</h2>
        <p>Hello, I'm John John Largent, currently studying for a Bachelor Degree in Art History at Concordia University in Montreal. Here you'll find information about me, my work, and how to get in touch.</p>
    </section>

    <section id="latest-Works">
        <h2>Latest Works</h2>
        <!-- Grid of 3x3 square images -->
        <div class="project-grid">
            <div class="project-cell">
                <div class="project-image" style="background-image: url('URL_TO_IMAGE_1');"></div>
            </div>
            <div class="project-cell">
                <div class="project-image" style="background-image: url('URL_TO_IMAGE_2');"></div>
            </div>
            <div class="project-cell">
                <div class="project-image" style="background-image: url('URL_TO_IMAGE_3');"></div>
            </div>
            <div class="project-cell">
                <div class="project-image" style="background-image: url('URL_TO_IMAGE_4');"></div>
            </div>
            <div class="project-cell">
                <div class="project-image" style="background-image: url('URL_TO_IMAGE_5');"></div>
            </div>
            <div class="project-cell">
                <div class="project-image" style="background-image: url('URL_TO_IMAGE_6');"></div>
            </div>
            <div class="project-cell">
                <div class="project-image" style="background-image: url('URL_TO_IMAGE_7');"></div>
            </div>
            <div class="project-cell">
                <div class="project-image" style="background-image: url('URL_TO_IMAGE_8');"></div>
            </div>
            <div class="project-cell">
                <div class="project-image" style="background-image: url('URL_TO_IMAGE_9');"></div>
            </div>
        </div>
    </section>

    <section id="contact">
        <h2>Contact</h2>
        <p>Hit me up at:</p>
        <ul>
            <li>Email: <a href="mailto:jj@magicmonkey.net">jj@magicmonkey.net</a></li>
            <li>Phone: +1 (438) 543-0691</li>
        </ul>
    </section>

    <section id="newsletter-section" class="newsletter">
        <h2>Newsletter</h2>
        <!-- You can add images and other content here later -->
    </section>

    <footer>
        <p>&copy; 2024 John John Largent. All rights reserved.</p>
    </footer>
</body>
</html>
