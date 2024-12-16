<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dushantha Majith - Profile</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Arial', sans-serif;
        }
        body {
            background-color: #f4f6f9;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            line-height: 1.6;
        }
        .profile-container {
            width: 100%;
            max-width: 600px;
            background-color: white;
            border-radius: 15px;
            box-shadow: 0 10px 25px rgba(0,0,0,0.1);
            overflow: hidden;
            transition: transform 0.3s ease;
        }
        .profile-container:hover {
            transform: scale(1.02);
        }
        .profile-header {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            text-align: center;
            padding: 30px 20px;
            position: relative;
        }
        .profile-image {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            border: 5px solid white;
            object-fit: cover;
            margin-bottom: 15px;
        }
        .profile-name {
            font-size: 24px;
            font-weight: bold;
            margin-bottom: 10px;
        }
        .profile-title {
            color: rgba(255,255,255,0.8);
            font-size: 16px;
        }
        .nav-tabs {
            display: flex;
            justify-content: center;
            background-color: #f8f9fa;
            padding: 15px;
        }
        .nav-tab {
            margin: 0 10px;
            padding: 10px 20px;
            border: none;
            background-color: #e9ecef;
            color: #495057;
            border-radius: 20px;
            cursor: pointer;
            transition: all 0.3s ease;
        }
        .nav-tab:hover, .nav-tab.active {
            background-color: #007bff;
            color: white;
        }
        .profile-content {
            padding: 20px;
            text-align: center;
        }
        .social-links {
            display: flex;
            justify-content: center;
            margin-top: 20px;
        }
        .social-link {
            margin: 0 10px;
            color: #007bff;
            text-decoration: none;
            font-size: 24px;
            transition: color 0.3s ease;
        }
        .social-link:hover {
            color: #0056b3;
        }
        .tech-stack {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 10px;
            margin-top: 20px;
        }
        .tech-badge {
            background-color: #e9ecef;
            padding: 8px 15px;
            border-radius: 20px;
            display: flex;
            align-items: center;
            gap: 8px;
        }
        .tech-badge img {
            width: 24px;
            height: 24px;
        }
        .contact-section {
            background-color: #f8f9fa;
            padding: 15px;
            text-align: center;
        }
        .contact-btn {
            display: inline-block;
            background-color: #007bff;
            color: white;
            padding: 10px 20px;
            text-decoration: none;
            border-radius: 25px;
            transition: background-color 0.3s ease;
        }
        .contact-btn:hover {
            background-color: #0056b3;
        }
    </style>
</head>
<body>
    <div class="profile-container">
        <div class="profile-header">
            <img src="https://raw.githubusercontent.com/dushantha2000/dushantha2000/main/12345.png" alt="Profile" class="profile-image">
            <div class="profile-name">Dushantha Majith</div>
            <div class="profile-title">Web Developer | Creative Designer</div>
        </div>

        <div class="nav-tabs">
            <button class="nav-tab active" onclick="showSection('about')">About</button>
            <button class="nav-tab" onclick="showSection('skills')">Skills</button>
            <button class="nav-tab" onclick="showSection('blog')">Blog</button>
        </div>

        <div id="about" class="profile-content" style="display: block;">
            <p>
                Passionate web developer from Sri Lanka, currently diving deep into Laravel. 
                I love creating innovative solutions and exploring new technologies.
            </p>
            <div class="social-links">
                <a href="https://twitter.com/dushanthamajith" class="social-link">Twitter</a>
                <a href="https://linkedin.com/in/dushantha majith" class="social-link">LinkedIn</a>
                <a href="https://instagram.com/dushantha_majith" class="social-link">Instagram</a>
            </div>
        </div>

        <div id="skills" class="profile-content" style="display: none;">
            <h2>Tech Stack</h2>
            <div class="tech-stack">
                <div class="tech-badge">
                    <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/react/react-original-wordmark.svg" alt="React">
                    React
                </div>
                <div class="tech-badge">
                    <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/nodejs/nodejs-original-wordmark.svg" alt="Node.js">
                    Node.js
                </div>
                <div class="tech-badge">
                    <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" alt="Python">
                    Python
                </div>
            </div>
        </div>

        <div id="blog" class="profile-content" style="display: none;">
            <h2>Latest Blog</h2>
            <a href="https://xtechnologyworld.blogspot.com" class="contact-btn">Visit My Tech Blog</a>
        </div>

        <div class="contact-section">
            <a href="mailto:majithdushantha@gmail.com" class="contact-btn">Contact Me</a>
        </div>
    </div>

    <script>
        function showSection(sectionId) {
            // Hide all sections
            ['about', 'skills', 'blog'].forEach(section => {
                document.getElementById(section).style.display = 'none';
            });

            // Remove active class from all tabs
            document.querySelectorAll('.nav-tab').forEach(tab => {
                tab.classList.remove('active');
            });

            // Show selected section
            document.getElementById(sectionId).style.display = 'block';

            // Add active class to clicked tab
            event.target.classList.add('active');
        }
    </script>
</body>
</html>
