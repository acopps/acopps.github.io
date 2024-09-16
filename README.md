<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tech Help Services</title>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css" rel="stylesheet">
    <style>
        :root {
            --primary-color: #1877f2;
            --secondary-color: #42b72a;
            --background-color: #f0f2f5;
            --surface-color: #ffffff;
            --text-color: #050505;
            --text-secondary: #65676b;
        }
        body {
            font-family: Helvetica, Arial, sans-serif;
            line-height: 1.6;
            margin: 0;
            padding: 0;
            color: var(--text-color);
            background-color: var(--background-color);
        }
        header {
            background-color: var(--primary-color);
            color: white;
            text-align: left;
            padding: 1rem 2rem;
            box-shadow: 0 2px 4px rgba(0,0,0,0.1);
        }
        header h1 {
            font-size: 2rem;
            margin-bottom: 0;
        }
        main {
            max-width: 900px;
            margin: 2rem auto;
            padding: 2rem;
            background-color: var(--surface-color);
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
            border-radius: 8px;
        }
        section {
            margin-bottom: 2rem;
            padding-bottom: 1rem;
            border-bottom: 1px solid #e4e6eb;
        }
        h2 {
            color: var(--primary-color);
            font-size: 1.5rem;
            margin-top: 0;
        }
        ul {
            list-style-type: none;
            padding-left: 0;
        }
        li {
            margin-bottom: 0.75rem;
            padding-left: 1.5em;
            position: relative;
        }
        li:before {
            content: "\2022";  /* Unicode for a bullet point */
            position: absolute;
            left: 0.5em;
            color: var(--primary-color);
            font-size: 1.2em;
        }
        .contact-info {
            background-color: #f0f2f5;
            padding: 1rem;
            border-radius: 8px;
        }
        .phone-number {
            padding-left: 0;
            margin-top: 1rem;
        }
        .phone-number:before {
            content: none;
        }
        form {
            display: grid;
            gap: 1rem;
        }
        input, textarea, button {
            width: 100%;
            padding: 0.75rem;
            border: 1px solid #dddfe2;
            border-radius: 6px;
            font-size: 1rem;
        }
        button {
            background-color: var(--secondary-color);
            color: white;
            border: none;
            cursor: pointer;
            transition: background-color 0.3s ease;
            font-weight: bold;
            border-radius: 6px;
        }
        button:hover {
            background-color: #36a420;
        }
        .icon {
            margin-right: 10px;
            color: var(--primary-color);
        }
    </style>
</head>
<body>
    <header>
        <h1><i class="fas fa-laptop icon"></i>Tech Help Services</h1>
    </header>
    <main>
        <section id="about">
            <h2>About Our Services</h2>
            <p>Welcome to Tech Help Services! I offer a wide array of tech solutions, bringing expertise right to your doorstep. From basic troubleshooting to advanced AI implementations, I'm here to simplify technology and enhance your digital life.</p>
        </section>
        <section id="services">
            <h2>How I Can Help You</h2>
            <ul>
                <li>Smartphone mastery</li>
                <li>Microsoft Office suite proficiency</li>
                <li>Personal automation for enhanced productivity</li>
                <li>Social media strategy and management</li>
                <li>Smart home device setup and optimization</li>
                <li>Cybersecurity and password management</li>
                <li>AI integration for everyday tasks</li>
            </ul>
            <p>This is just the beginning. Have a unique tech challenge? Let's tackle it together!</p>
        </section>
        <section id="availability" class="contact-info">
            <h2>Availability & Contact</h2>
            <p>Ready to assist you:</p>
            <ul>
                <li>Weekdays: After 5pm</li>
                <li>Weekends: All day</li>
            </ul>
            <p class="phone-number"><strong>469-662-9792</strong></p>
        </section>
        <section id="appointment">
            <h2>Schedule Your Tech Session</h2>
            <form id="appointment-form" onsubmit="return sendEmail()">
                <input type="text" id="name" name="name" placeholder="Your Name" required>
                <input type="email" id="email" name="email" placeholder="Your Email" required>
                <input type="tel" id="phone" name="phone" placeholder="Your Phone Number">
                <input type="date" id="date" name="date" required>
                <input type="time" id="time" name="time" required>
                <textarea id="message" name="message" placeholder="What tech challenge can I help you with?" rows="4"></textarea>
                <button type="submit">Book Your Session</button>
            </form>
        </section>
    </main>
    <script>
        function sendEmail() {
            var name = document.getElementById('name').value;
            var email = document.getElementById('email').value;
            var phone = document.getElementById('phone').value;
            var date = document.getElementById('date').value;
            var time = document.getElementById('time').value;
            var message = document.getElementById('message').value;

            var mailtoLink = "mailto:austin@austincopps.com"
                + "?subject=" + encodeURIComponent("New Appointment Request")
                + "&body=" + encodeURIComponent("Name: " + name + "\n"
                    + "Email: " + email + "\n"
                    + "Phone: " + phone + "\n"
                    + "Date: " + date + "\n"
                    + "Time: " + time + "\n"
                    + "Message: " + message);

            window.location.href = mailtoLink;
            return false;
        }
    </script>
</body>
</html>
