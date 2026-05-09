<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Lovely University Professional- Welcome</title>
    
    <style>
        /* ===== GLOBAL STYLES ===== */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #333;
            background-color: #f4f4f4;
        }

        /* ===== HEADER & NAVIGATION ===== */
        header {
            background: linear-gradient(135deg, #1e3c72 0%, #2a5298 100%);
            color: white;
            padding: 1rem 0;
            position: sticky;
            top: 0;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
            z-index: 100;
        }

        header-content {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
        }

        .school-name {
            font-size: 1.8rem;
            font-weight: bold;
            letter-spacing: 1px;
        }

        /* Navigation Menu */
        nav ul {
            list-style: none;
            display: flex;
            gap: 2rem;
        }

        nav a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s ease;
            cursor: pointer;
        }

        nav a:hover {
            color: #ffd700;
            text-shadow: 0 0 8px rgba(255, 215, 0, 0.5);
        }

        /* Mobile Menu Toggle */
        .menu-toggle {
            display: none;
            background: none;
            border: none;
            color: white;
            font-size: 1.5rem;
            cursor: pointer;
        }

        /* ===== SECTIONS ===== */
        section {
            display: none;
            padding: 3rem 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        section.active {
            display: block;
        }

        h1, h2 {
            color: #1e3c72;
            margin-bottom: 1.5rem;
            text-align: center;
        }

        h2 {
            font-size: 2rem;
            border-bottom: 3px solid #2a5298;
            padding-bottom: 0.5rem;
            display: inline-block;
        }

        /* ===== HOME SECTION ===== */
        #home {
            text-align: center;
            background: linear-gradient(135deg, rgba(30, 60, 114, 0.9), rgba(42, 82, 152, 0.9)), 
                        url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 600"><rect fill="%23f0f0f0" width="1200" height="600"/></svg>');
            color: white;
            padding: 5rem 2rem;
            border-radius: 10px;
            margin: 2rem 0;
        }

        #home h1 {
            color: white;
            font-size: 3rem;
            margin-bottom: 1rem;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
        }

        .welcome-message {
            font-size: 1.3rem;
            margin: 1.5rem 0;
            line-height: 1.8;
        }

        .welcome-btn {
            background: #ffd700;
            color: #1e3c72;
            padding: 0.8rem 2rem;
            font-size: 1rem;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-weight: bold;
            transition: all 0.3s ease;
            margin-top: 1.5rem;
        }

        .welcome-btn:hover {
            background: #ffed4e;
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        }

        .welcome-btn:active {
            transform: translateY(0);
        }

        /* ===== ABOUT SECTION ===== */
        #about {
            background: white;
            border-radius: 10px;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        }

        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 2rem;
            align-items: center;
        }

        .about-text p {
            margin: 1rem 0;
            font-size: 1.05rem;
            line-height: 1.8;
            color: #555;
        }

        .about-highlight {
            color: #2a5298;
            font-weight: bold;
        }

        /* ===== COURSES SECTION ===== */
        #courses {
            background: white;
            border-radius: 10px;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        }

        .courses-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 2rem;
        }

        .course-card {
            background: linear-gradient(135deg, #1e3c72 0%, #2a5298 100%);
            color: white;
            padding: 2rem;
            border-radius: 8px;
            text-align: center;
            transition: all 0.3s ease;
            box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
        }

        .course-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 8px 20px rgba(30, 60, 114, 0.3);
        }

        .course-card h3 {
            color: #ffd700;
            margin-bottom: 1rem;
            font-size: 1.5rem;
        }

        .course-card p {
            margin: 0.5rem 0;
            line-height: 1.6;
        }

        /* ===== CONTACT SECTION ===== */
        #contact {
            background: white;
            border-radius: 10px;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        }

        .contact-container {
            max-width: 600px;
            margin: 0 auto;
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        label {
            display: block;
            margin-bottom: 0.5rem;
            color: #1e3c72;
            font-weight: 600;
        }

        input[type="text"],
        input[type="email"],
        textarea {
            width: 100%;
            padding: 0.8rem;
            border: 2px solid #ddd;
            border-radius: 5px;
            font-size: 1rem;
            font-family: inherit;
            transition: border-color 0.3s ease;
        }

        input[type="text"]:focus,
        input[type="email"]:focus,
        textarea:focus {
            outline: none;
            border-color: #2a5298;
            box-shadow: 0 0 8px rgba(42, 82, 152, 0.2);
        }

        textarea {
            resize: vertical;
            min-height: 150px;
        }

        .submit-btn {
            background: linear-gradient(135deg, #1e3c72 0%, #2a5298 100%);
            color: white;
            padding: 1rem 2rem;
            font-size: 1rem;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-weight: bold;
            width: 100%;
            transition: all 0.3s ease;
        }

        .submit-btn:hover {
            box-shadow: 0 5px 15px rgba(30, 60, 114, 0.3);
            transform: translateY(-2px);
        }

        .submit-btn:active {
            transform: translateY(0);
        }

        .error-message {
            color: #d32f2f;
            font-size: 0.9rem;
            margin-top: 0.3rem;
            display: none;
        }

        .error-message.show {
            display: block;
        }

        /* ===== RESPONSIVE DESIGN ===== */
        @media (max-width: 768px) {
            header-content {
                flex-direction: column;
                gap: 1rem;
            }

            .school-name {
                font-size: 1.4rem;
            }

            nav ul {
                gap: 1rem;
                flex-wrap: wrap;
                justify-content: center;
            }

            nav a {
                font-size: 0.9rem;
            }

            #home h1 {
                font-size: 2rem;
            }

            .welcome-message {
                font-size: 1.1rem;
            }

            .about-content {
                grid-template-columns: 1fr;
            }

            h2 {
                font-size: 1.5rem;
            }

            section {
                padding: 2rem 1rem;
            }

            .courses-grid {
                grid-template-columns: 1fr;
            }
        }

        @media (max-width: 480px) {
            .school-name {
                font-size: 1.2rem;
            }

            nav ul {
                gap: 0.5rem;
            }

            nav a {
                font-size: 0.8rem;
            }

            #home h1 {
                font-size: 1.5rem;
            }

            .welcome-message {
                font-size: 1rem;
            }

            .course-card {
                padding: 1.5rem;
            }

            .submit-btn {
                padding: 0.8rem 1.5rem;
            }
        }

        /* ===== FOOTER ===== */
        footer {
            background: #1e3c72;
            color: white;
            text-align: center;
            padding: 2rem;
            margin-top: 2rem;
        }

        footer p {
            margin: 0.5rem 0;
        }
    </style>
</head>
<body>
    <!-- ===== HEADER ===== -->
    <header>
        <header-content>
            <div class="University-Name">🎓 Lovely Professional University</div>
            <nav>
                <ul>
                    <li><a onclick="showSection('home')">Home</a></li>
                    <li><a onclick="showSection('about')">About</a></li>
                    <li><a onclick="showSection('courses')">Courses</a></li>
                    <li><a onclick="showSection('contact')">Contact</a></li>
                </ul>
            </nav>
        </header-content>
    </header>

    <!-- ===== HOME SECTION ===== -->
    <section id="home" class="active">
        <h1>Welcome to Lovely Professional University🧑‍🎓</h1>
        <p class="welcome-message">
            We are dedicated to providing quality education and fostering a love for learning 
            in every student. Join us on this exciting journey of knowledge and growth!
        </p>
        <button class="welcome-btn" onclick="showWelcomeMessage()">
            🎓 Learn More About Us
        </button>
    </section>

    <!-- ===== ABOUT SECTION ===== -->
    <section id="about">
        <h2>About Our University</h2>
        <div class="about-content">
            <div class="about-text">
                <p>
                    <span class="about-highlight">Lovely Professional University</span> is a premier educational 
                    institution committed to excellence in teaching and learning. 
                </p>
                <p>
                    With over 21 years of experience, we have successfully educated thousands of students 
                    who have gone on to achieve great success in their careers.
                </p>
                <p>
                    Our dedicated team of experienced educators uses innovative teaching methods and 
                    modern technology to ensure every student reaches their full potential.
                </p>
                <p>
                    <span class="about-highlight">Our Mission:</span> To empower students with knowledge, 
                    skills, and values needed to succeed in the 21st century.
                </p>
            </div>
            <div class="about-text">
                <p>
                    <span class="about-highlight">Why Choose Us?</span>
                </p>
                <ul style="margin-left: 1.5rem;">
                    <li>✅ Highly qualified and experienced faculty</li>
                    <li>✅ State-of-the-art facilities and technology</li>
                    <li>✅ Personalized attention to each student</li>
                    <li>✅ Strong focus on character development</li>
                    <li>✅ Excellent track record of student success</li>
                    <li>✅ Supportive and inclusive learning environment</li>
                </ul>
            </div>
        </div>
    </section>

    <!-- ===== COURSES SECTION ===== -->
    <section id="courses">
        <h2>Our Courses</h2>
        <div class="courses-grid">
            <!-- Course 1 -->
            <div class="course-card">
                <h3>📖 Soft Skills Development</h3>
                <p>
                    Master the fundamentals of English grammar, literature, and communication. 
                    Develop strong writing and speaking skills.
                </p>
                <p><strong>Level:</strong> Beginner to Advanced</p>
            </div>

            <!-- Course 2 -->
            <div class="course-card">
                <h3>🔬 Science</h3>
                <p>
                    Explore physics, chemistry, and biology through hands-on experiments and 
                    interactive learning. Understand the world around you.
                </p>
                <p><strong>Level:</strong> Beginner to Advanced</p>
            </div>

            <!-- Course 3 -->
            <div class="course-card">
                <h3>📐 Mathematics</h3>
                <p>
                    Build a strong foundation in algebra, geometry, and calculus. 
                    Problem-solving skills for real-world applications.
                </p>
                <p><strong>Level:</strong> Beginner to Advanced</p>
            </div>

            <!-- Course 4 -->
            <div class="course-card">
                <h3>🌍 AI Driven Industry Based Learning </h3>
                <p>
                    Learn about AI, coding and competitive programming. 
                    Understand real-world problems and develop solutions.
                </p>
                <p><strong>Level:</strong> Beginner to Intermediate</p>
            </div>

            <!-- Course 5 -->
            <div class="course-card">
                <h3>💻 Computer Science</h3>
                <p>
                    Introduction to programming, web design, and digital literacy. 
                    Prepare for the digital age.
                </p>
                <p><strong>Level:</strong> Beginner to Advanced</p>
            </div>

            <!-- Course 6 -->
            <div class="course-card">
                <h3>🎨 Arts</h3>
                <p>
                    Express yourself through art, music, and creative writing. 
                    Develop artistic skills and cultural appreciation.
                </p>
                <p><strong>Level:</strong> All Levels</p>
            </div>
            <!-- Course 7 -->
            <div class="course-card">
                <h3>⚖️ Law</h3>
                <p>
                    Make yourself eligible for civil services and law to become a lawyer or a reputed judge. 
                   Gain confidence through various events  and receive  appreciation.
                </p>
                <p><strong>Level:</strong> All Levels</p>
            </div>
             <!-- Course 8 -->
            <div class="course-card">
                <h3> 📈📊🧑‍🎓MBA </h3>
                <p>
                    Get Finance, Marketing, Human Resources(HR), Operations Management and IT.
                    Future ready programs-MBA in Business Analytics, Fintech and Artifical Intelligence.
                </p>
                <p><strong>Level:</strong> All Levels</p>
            </div>
        </div>
    </section>

    <!-- ===== CONTACT SECTION ===== -->
    <section id="contact">
        <h2>Contact Us</h2>
        <div class="contact-container">
            <p style="text-align: center; margin-bottom: 2rem; color: #555;">
                Have any questions? We'd love to hear from you! Fill out the form below and we'll get back to you soon.
            </p>

            <!-- Contact Form -->
            <form id="contactForm" onsubmit="handleFormSubmit(event)">
                <!-- Name Field -->
                <div class="form-group">
                    <label for="name">Your Name:</label>
                    <input 
                        type="text" 
                        id="name" 
                        name="name" 
                        placeholder="Enter your full name"
                    >
                    <div class="error-message" id="nameError">Please enter your name</div>
                </div>

                <!-- Email Field -->
                <div class="form-group">
                    <label for="email">Your Email:</label>
                    <input 
                        type="email" 
                        id="email" 
                        name="email" 
                        placeholder="Enter your email address"
                    >
                    <div class="error-message" id="emailError">Please enter a valid email address</div>
                </div>

                <!-- Message Field -->
                <div class="form-group">
                    <label for="message">Your Message:</label>
                    <textarea 
                        id="message" 
                        name="message" 
                        placeholder="Type your message here..."
                    ></textarea>
                    <div class="error-message" id="messageError">Please enter your message</div>
                </div>

                <!-- Submit Button -->
                <button type="submit" class="submit-btn">📧 Send Message</button>
            </form>
        </div>
    </section>

    <!-- ===== FOOTER ===== -->
    <footer>
        <p>&copy; Lovely Professional University. All rights reserved.</p>
        <p>📞 Phone: +91- 1824-517000 | 📧 Email: info@lpu.co.in</p>
        <p>📍 Address: Delhi G.T. Road (NH-1), Phagwara ,Punjab,India. </p>
    </footer>

    <!-- ===== JAVASCRIPT ===== -->
    <script>
        // ===== NAVIGATION FUNCTION =====
        // Shows the selected section and hides others
        function showSection(sectionId) {
            // Hide all sections
            const sections = document.querySelectorAll('section');
            sections.forEach(section => {
                section.classList.remove('active');
            });

            // Show the selected section
            const selectedSection = document.getElementById(sectionId);
            if (selectedSection) {
                selectedSection.classList.add('active');
                // Scroll to top of the page
                window.scrollTo(0, 0);
            }
        }

        // ===== WELCOME MESSAGE FUNCTION =====
        // Shows a welcome alert when button is clicked
        function showWelcomeMessage() {
            alert('🎓 Welcome to Lovely Professional University!\n\nWe are excited to have you here. Explore our courses, learn more about us, and don\'t hesitate to contact us with any questions!');
        }

        // ===== EMAIL VALIDATION FUNCTION =====
        // Validates email format using regular expression
        function validateEmail(email) {
            // Regular expression pattern for email validation
            const emailPattern = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
            return emailPattern.test(email);
        }

        // ===== FORM VALIDATION FUNCTION =====
        // Validates the contact form before submission
        function validateForm() {
            // Get form field values
            const name = document.getElementById('name').value.trim();
            const email = document.getElementById('email').value.trim();
            const message = document.getElementById('message').value.trim();

            // Reset all error messages
            document.getElementById('nameError').classList.remove('show');
            document.getElementById('emailError').classList.remove('show');
            document.getElementById('messageError').classList.remove('show');

            // Track if form is valid
            let isValid = true;

            // Check if name is empty
            if (name === '') {
                document.getElementById('nameError').classList.add('show');
                isValid = false;
            }

            // Check if email is empty or invalid
            if (email === '' || !validateEmail(email)) {
                document.getElementById('emailError').classList.add('show');
                isValid = false;
            }

            // Check if message is empty
            if (message === '') {
                document.getElementById('messageError').classList.add('show');
                isValid = false;
            }

            return isValid;
        }

        // ===== FORM SUBMISSION HANDLER =====
        // Handles form submission with validation
        function handleFormSubmit(event) {
            // Prevent default form submission behavior
            event.preventDefault();

            // Validate the form
            if (validateForm()) {
                // Get form values for display
                const name = document.getElementById('name').value.trim();
                const email = document.getElementById('email').value.trim();

                // Show success message
                alert(`Thank you, ${name}!\n\nWe have received your message. We'll contact you at ${email} soon.\n\nWelcome to Lovely Professional University! 🎓`);

                // Clear all form fields
                document.getElementById('contactForm').reset();

                // Optional: Navigate back to home after successful submission
                setTimeout(() => {
                    showSection('home');
                }, 1000);
            }
        }

        // ===== PAGE LOAD EVENT =====
        // Ensures home section is shown when page loads
        document.addEventListener('DOMContentLoaded', function() {
            showSection('home');
        });
    </script>
</body>
</html>
