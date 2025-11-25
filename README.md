# Smart-Attendance-System
📖 Overview
Smart Attendance System is an AI-powered solution designed to automate student attendance tracking using facial recognition.

Students register by submitting their facial data, which is trained by an AI model. During class sessions, a high-level camera captures live video streams, converts them into frames, and detects student presence/absence. The attendance data is then updated in the system in real time.

This repository contains the server-side implementation built with Golang, handling all business logic, APIs, and communication with the AI service.

✨ Features
Student Module

Student registration with face features
View attendance records
Update personal details & face features
Faculty Module

Add and manage subjects
Monitor student attendance in real time
Manage class records
Core Attendance System

AI-powered face recognition
Frame extraction from classroom videos
Automatic presence/absence detection using USN mapping
Secure data persistence with PostgreSQL
APIs

REST APIs built using Echo framework
Authentication & authorization via middlewares
Smooth communication with external Python AI service
🛠️ Tech Stack
Backend: Golang (Echo Framework)
Database: PostgreSQL
AI Service: Python (Facial Recognition Model)
Authentication: JWT Tokens, Middleware Security
🏗️ System Architecture
Backend (Golang): Handles all business logic, API endpoints, and database operations. Built using the Echo framework, it provides secure, high-performance REST APIs for students, faculty, subjects, and attendance management.

AI Integration (Python Service): Facial recognition and model training are handled by a separate Python service. The backend communicates seamlessly with this service for student face registration and real-time attendance detection, keeping the heavy AI computation isolated from API handling.

Database (PostgreSQL): All data—including student profiles, facial embeddings, subjects, and attendance records—is stored securely and efficiently. The backend ensures data integrity, validation, and optimized queries.

Attendance Workflow:

Students register and submit their face data.
Python AI service trains the model and notifies the backend.
During class, video frames are processed to detect student presence.
Attendance payloads are validated by the backend and stored in the database.
