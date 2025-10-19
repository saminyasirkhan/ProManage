🧭 ProManage Flask App – Final Description (Accurate to Your Report)
Overview

ProManage is a collaborative project management web application developed using Flask, HTML, CSS, and SQLAlchemy.
It enables role-based task management, providing separate dashboards for Project Managers and Team Members with secure authentication and real-time task updates.

The project was developed jointly:

Front-End: Designed and implemented by Yasir Khan (u5653630) — including UI, structure diagrams, flowcharts, and form validation.

Back-End: Implemented by u5614928 — including SQLAlchemy models, Flask routing, database creation, and encryption handling.

Key Features

🔐 Secure User Authentication

Sign-up and sign-in with hashed passwords (Flask generate_password_hash() / check_password_hash()).

Role-based session control with Flask-Login.

🧩 Role-Based Dashboards

Manager Dashboard: Add, edit, delete users; assign and track tasks.

Member Dashboard: View and update assigned tasks.

🧮 Database Integration

SQLAlchemy ORM with User, Task, and Activity models linked via foreign keys.

Activity logs capture user actions for transparency.

🧱 Front-End

Modern, responsive interface (HTML + CSS).

Validation for weak passwords, duplicate usernames, and form errors.

🔒 Security Design

Unique encryption keys per user (stored securely in the DB).

Role-based route control and session protection.

Potential for HTTPS and 2FA improvements in future iterations.

Tech Stack
Layer	Technologies
Front-End	HTML, CSS, Flask Templates
Back-End	Python (Flask), SQLAlchemy, SQLite
Security	Password hashing, encryption keys, RBAC
Tools	Visual Studio Code, GitHub, Flask, Jinja2
Project Structure
ProManage/
│
├── app.py                  # Main Flask application (routing + logic)
├── create_db.py            # Database initialization script
├── encryption.py           # Encryption key generator
├── templates/              # HTML templates (auth + dashboards)
├── static/                 # CSS and assets
├── database.db             # SQLite database (auto-generated)
├── Documentation.pdf       # Development report (front & back-end)
├── ProManage.zip           # Full code archive
└── README.md               # This file

How to Run
pip install -r requirements.txt
python create_db.py     # run once to create database
python app.py


Visit: http://127.0.0.1:5000

Default users are created automatically (one Project Manager and one Team Member).

Development Challenges

Fixed Flask context errors when creating the database (RuntimeError: no active app context).

Solved foreign key violations by cascading deletions for user tasks.

Migrated session-based logs to an Activity table for shared visibility.

Planned Improvements

Add 2FA and password recovery.

Replace hard-coded tasks with dynamic task assignment.

Implement HTTPS for encrypted traffic.
