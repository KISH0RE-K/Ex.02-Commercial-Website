# Ex02 Commercial Website
## Date:

## AIM
To create a commercial website using CSS Flexbox.

## ALGORITHM
### STEP 1
Create an HTML file (index.html)

### STEP 2
Create a CSS file (style.css)

### STEP 3
Include a navigation bar with links to different sections.

### STEP 4
Add structured sections for Homepage, Products / Services, About Us, Contact Details and User Account.

### STEP 5
Include social media links at the footer with copyright information.

### STEP 6
Define global styles for fonts, colors, and layout.

### STEP 7
Style the header, navigation bar, and sections.

### STEP 8
Use Flexbox for layout design.

### STEP 9
Add hover effects and transitions for interactivity.

### STEP 10
Add Images and Media.

### STEP 11
Use optimized images for a professional look.

### STEP 12
Open the HTML file in a browser to check layout and functionality.

### STEP 13
Fix styling issues and refine content placement.

### STEP 14
Deploy the website.

### STEP 15
Upload to GitHub Pages for free hosting.

## PROGRAM
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>NexGen Solutions - Commercial Website</title>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;600;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary-color: #3498db;
            --secondary-color: #2c3e50;
            --accent-color: #e74c3c;
            --text-color: #333;
            --light-bg: #ecf0f1;
            --white: #fff;
            --shadow-light: 0 4px 8px rgba(0, 0, 0, 0.1);
            --shadow-medium: 0 8px 16px rgba(0, 0, 0, 0.15);
        }

        body {
            font-family: 'Montserrat', sans-serif;
            margin: 0;
            padding: 0;
            background-color: var(--light-bg);
            color: var(--text-color);
            line-height: 1.6;
        }

        .container {
            max-width: 1100px;
            margin: 0 auto;
            padding: 0 20px;
        }

        h1, h2, h3 {
            color: var(--secondary-color);
            text-align: center;
        }

        h2 {
            font-size: 2.5em;
            margin-bottom: 0.5em;
        }

        p {
            font-size: 1.1em;
            text-align: center;
        }

        .btn {
            display: inline-block;
            background: var(--primary-color);
            color: var(--white);
            padding: 12px 25px;
            text-decoration: none;
            border-radius: 50px;
            transition: background 0.3s ease, transform 0.3s ease;
            box-shadow: var(--shadow-light);
        }

        .btn:hover {
            background: #2980b9;
            transform: translateY(-2px);
            box-shadow: var(--shadow-medium);
        }

        header {
            background: var(--white);
            padding: 1rem 0;
            border-bottom: 1px solid #ddd;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        header .logo {
            font-size: 1.8em;
            font-weight: bold;
            color: var(--secondary-color);
            text-decoration: none;
            transition: color 0.3s ease;
        }

        header .logo:hover {
            color: var(--primary-color);
        }

        nav ul {
            list-style: none;
            display: flex;
            margin: 0;
            padding: 0;
            gap: 25px;
        }

        nav a {
            color: #555;
            text-decoration: none;
            font-weight: 600;
            transition: color 0.3s ease;
        }

        nav a:hover {
            color: var(--primary-color);
        }

        #hero {
            background: linear-gradient(rgba(236, 240, 241, 0.9), rgba(236, 240, 241, 0.9)), url('1348334.jpg') no-repeat center center/cover;
            padding: 80px 0;
            text-align: center;
            animation: fadeIn 1s ease-in-out;
        }

        #hero h1 {
            font-size: 4em;
            margin: 0 0 10px;
            animation: fadeInUp 1s ease-out;
        }

        #hero p {
            font-size: 1.5em;
            max-width: 700px;
            margin: 0 auto 40px;
            animation: fadeInUp 1s ease-out 0.3s;
        }

        #services {
            padding: 60px 0;
            background: var(--white);
        }

        .services-grid {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 30px;
        }

        .service-card {
            background: var(--light-bg);
            padding: 30px;
            border-radius: 12px;
            box-shadow: var(--shadow-light);
            text-align: center;
            flex: 1 1 300px;
            box-sizing: border-box;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .service-card:hover {
            transform: translateY(-10px);
            box-shadow: var(--shadow-medium);
        }

        .service-card h3 {
            color: var(--primary-color);
            margin-top: 0;
            font-size: 1.8em;
        }

        #about-us, #contact-cta {
            padding: 60px 0;
        }

        #contact-cta {
            background: var(--secondary-color);
            color: var(--white);
        }

        #contact-cta h2 {
            color: var(--white);
        }

        #contact-cta p {
            color: #bdc3c7;
        }

        footer {
            background: var(--secondary-color);
            color: var(--white);
            text-align: center;
            padding: 30px 0;
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 15px;
        }

        .footer-info {
            font-size: 0.9em;
        }

        @media (max-width: 768px) {
            header {
                flex-direction: column;
                padding: 1rem;
            }

            nav ul {
                flex-direction: column;
                align-items: center;
                margin-top: 10px;
            }

            #hero h1 {
                font-size: 2.5em;
            }

            #hero p {
                font-size: 1.2em;
            }

            .services-grid {
                flex-direction: column;
                align-items: center;
            }

            .service-card {
                flex: 1 1 100%;
                max-width: 300px;
            }
        }

        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
    </style>
</head>
<body>

    <header class="container">
        <a href="#" class="logo">NexGen Solutions</a>
        <nav>
            <ul>
                <li><a href="#">Home</a></li>
                <li><a href="#">Services</a></li>
                <li><a href="#">About Us</a></li>
                <li><a href="#">Contact</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <section id="hero">
            <div class="container">
                <h1>Unlock Your Business's Full Potential</h1>
                <p>We provide innovative software and IT solutions to drive your success.</p>
                <a href="#" class="btn">Get Started</a>
            </div>
        </section>

        <section id="services">
            <div class="container">
                <h2>Our Services</h2>
                <div class="services-grid">
                    <div class="service-card">
                        <h3>Web Development</h3>
                        <p>Building responsive and powerful websites for your brand.</p>
                    </div>
                    <div class="service-card">
                        <h3>Mobile Apps</h3>
                        <p>Creating seamless and user-friendly mobile applications.</p>
                    </div>
                    <div class="service-card">
                        <h3>Cloud Solutions</h3>
                        <p>Scalable and secure cloud infrastructure for your business.</p>
                    </div>
                </div>
            </div>
        </section>

        <section id="about-us">
            <div class="container">
                <h2>About Us</h2>
                <p>
                    We are a team of dedicated professionals committed to delivering excellence. Our goal is to help businesses of all sizes leverage technology to achieve their objectives and stay ahead in the digital world.
                </p>
            </div>
        </section>

        <section id="contact-cta">
            <div class="container">
                <h2>Ready to Start?</h2>
                <p>Contact us today for a free consultation and let's build something amazing together.</p>
                <a href="#" class="btn">Contact Us</a>
            </div>
        </section>
    </main>

    <footer>
        <div class="container">
            <p>&copy; 2025 NexGen Solutions. All rights reserved.</p>
            <div class="footer-info">
                <p>Designed by: KISHORE K</p>
                <p>Register Number: 212223040101</p>
            </div>
        </div>
    </footer>

</body>
</html>

```
## OUTPUT


## RESULT
The program for creating commercial website using CSS Flexbox is executed successfully.