**Flask Authentication System**

This project provides a secure and extensible authentication system built with Flask. It supports user registration, login, logout, password hashing, session management, and protected routes. The system is designed with clarity and scalability in mind and can be integrated into SaaS applications, dashboards, internal tools, or any project requiring authenticated access.

**Overview:**
This application includes:

1. User registration

2. Secure password hashing

3. Session-based authentication

4. Protected dashboard access

5. Logout functionality

**Core Technologies**:
1. Flask
2. Flask-Login
3. Flask-SQLAlchemy
4. SQLite
5. Werkzeug Security

**System Requirements**:
-> Python 3.8 or higher
-> pip package manager
-> Virtual environment recommended

**Installation**:

**1. Clone the repository:**
git clone https://github.com/Astitva13/Flask-Login-System.git

cd Flask-Login-System

**2. Create a virtual environment**:
python -m venv venv

**3. Activate the virtual environment**:
Windows:
venv\Scripts\activate
macOS/Linux:
source venv/bin/activate

**4. Install required dependencies:**
pip install -r requirements.txt

**5. Run the application**:
python app.py

**The application will be available at:**
http://127.0.0.1:5000/

**Project Structure**:


project/
│ app.py
│ requirements.txt
│ .gitignore
│
├── templates/
│     home.html
│     login.html
│     sign_up.html
│     dashboard.html
│
├── instance/
│     db.sqlite
│
└── venv/

**Authentication Flow:**

**Registration**:
A user provides a username and password. The application checks if the username already exists. The password is hashed using PBKDF2 via Werkzeug and stored securely in SQLite.

**Login:**
The system validates the entered credentials. If valid, Flask-Login establishes a logged-in session and grants access to protected routes.

**Protected Dashboard:**
The dashboard route is secured using the login_required decorator. Only authenticated users can access it.

**Logout**:
The logout_user function terminates the active session and redirects the user to the home page.

**Extensibility Options**:
Email verification
Password reset functionality
Role-based access control
OAuth login integration (Google, GitHub, etc.)
Multi-factor authentication
Migration to PostgreSQL or MySQL

**Use Cases:**
SaaS dashboards
Internal administrative tools
MVP authentication systems
Educational web development projects
Microservices requiring simple login support

**License:**
This project is intended for educational and development purposes. You may modify or integrate the code into personal or commercial applications.
