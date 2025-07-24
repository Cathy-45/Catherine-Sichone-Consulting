# Catherine-Sichone-Consulting
![Profile image] (https://github.com/Cathy-45/Catherine-Sichone-Consulting/blob/a14f9ef4013c367f09dcf3f34903772e540568e3/IMG_1990.jpeg)


A modern, user-friendly web consulting profile for Catherine Sichone, a software development consultant based in Lusaka, Zambia. The website showcases her expertise in full-stack development, system integration, and Agile methodologies, with a sleek design inspired by the minimalist and eco-conscious aesthetic of Greta Thunberg’s website (gretathunberg.org). The site includes a contact form for clients to submit inquiries, powered by a Node.js/Express backend with MongoDB for storage and Nodemailer for email notifications to catherine.sichone@gmail.com.
Table of Contents
Features
Tech Stack
Installation
Usage
Deployment
Project Structure
Environment Variables
Contributing
License
Contact
Features
Modern Design: Minimalist, responsive UI with a Greta Thunberg-inspired color palette (dark green #1A3C34, cream #F5F5F0, muted gray #4A4A4A, accent green #A3E4D7).
Interactive Contact Form: Clients can submit consulting inquiries or fee questions, stored in MongoDB and emailed to catherine.sichone@gmail.com.
Backend Functionality: Node.js/Express API with MongoDB for data persistence and Nodemailer for reliable email delivery.
Responsive Layout: Optimized for mobile and desktop with card-based services and projects sections.
Smooth Navigation: Anchor links and a clean header for easy access to About, Services, Projects, and Contact sections.
Tech Stack
Front-End: HTML, CSS (Inter font, Greta-inspired colors), JavaScript
Back-End: Node.js, Express.js
Database: MongoDB (Atlas)
Email: Nodemailer (Gmail SMTP)
Dependencies: cors, dotenv, mongoose, nodemailer, nodemon (dev)
Installation
Clone the Repository:
bash



git clone https://github.com/<your-username>/catherine-sichone-consulting.git
cd catherine-sichone-consulting
Install Dependencies:
bash



npm install
Set Up MongoDB Atlas:
Create a free cluster at mongodb.com.
Obtain the connection string (e.g., mongodb+srv://<username>:<password>@cluster0.mongodb.net/consulting?retryWrites=true&w=majority).
Set Up Gmail for Nodemailer:
Enable 2FA on your Gmail account.
Generate an App Password at myaccount.google.com/security.
Configure Environment Variables:
Create a .env file in the root directory:
env



MONGODB_URI=mongodb+srv://<username>:<password>@cluster0.mongodb.net/consulting?retryWrites=true&w=majority
EMAIL_USER=your-email@gmail.com
EMAIL_PASS=your-app-password
PORT=3000
Run the Application:
bash



npm start
For development with hot reloading:
bash



npm run dev
Open http://localhost:3000 in a browser.
Usage
View the Website: Navigate to http://localhost:3000 to see the consulting profile.
Test the Form:
Fill out the contact form (Name, Email, Company (optional), Message).
Submit to verify:
Inquiry is saved in MongoDB Atlas.
Email is sent to catherine.sichone@gmail.com.
Success/error message appears on the webpage.
Customize:
Update the LinkedIn URL in public/index.html and README.md.
Add a logo or favicon in public/assets/ and update public/index.html.
Deployment
Backend (Render/Heroku):
Push the repository to GitHub.
On Render:
Create a new Web Service and connect the repository.
Set environment variables (MONGODB_URI, EMAIL_USER, EMAIL_PASS, PORT) in the Render dashboard.
Update public/script.js to use the deployed backend URL (e.g., https://your-app.onrender.com/api/inquiries).
Front-End (Netlify/GitHub Pages):
For Netlify:
Drag the public/ folder to the Netlify dashboard or link the repository.
Set the build directory to public/.
For GitHub Pages:
Push the public/ folder to a gh-pages branch.
Enable GitHub Pages in repository settings.
Ensure the form’s fetch URL in public/script.js points to the backend.
Security:
Add .env to .gitignore to protect sensitive data.
Consider adding reCAPTCHA to the form for spam protection.
Enable HTTPS on the deployed site.
Project Structure
text



catherine-sichone-consulting/
├── public/
│   ├── index.html        # Main webpage
│   ├── styles.css        # Greta-inspired CSS
│   ├── script.js         # Form submission logic
│   └── assets/           # Optional images (e.g., logo, favicon)
├── server/
│   ├── index.js          # Express server setup
│   ├── routes/
│   │   └── inquiries.js  # API route for inquiries
│   └── models/
│       └── Inquiry.js    # MongoDB schema
├── .env                  # Environment variables
├── package.json          # Dependencies and scripts
└── README.md             # Project documentation
Environment Variables
MONGODB_URI: MongoDB Atlas connection string.
EMAIL_USER: Gmail address for Nodemailer.
EMAIL_PASS: Gmail App Password for Nodemailer.
PORT: Server port (default: 3000).
Contributing
Contributions are welcome! To contribute:

Fork the repository.
Create a feature branch (git checkout -b feature/your-feature).
Commit changes (git commit -m 'Add your feature').
Push to the branch (git push origin feature/your-feature).
Open a pull request.
Please ensure code follows the project’s style (Prettier/ESLint can be added for consistency).

License
This project is licensed under the MIT License. See LICENSE for details.

Contact
For inquiries or collaboration, reach out to:

Email: catherine.sichone@gmail.com
LinkedIn: linkedin.com/in/catherinesichone
GitHub Issues: Open an issue in this repository for technical questions.
