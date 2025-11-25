# 🎓 Smart Attendance System – Server

## 📖 Overview

**Smart Attendance System** is an AI-powered solution designed to automate student attendance tracking using **facial recognition**.

Students register by submitting their facial data, which is trained by an AI model. During class sessions, a high-level camera captures live video streams, converts them into frames, and detects student presence/absence. The attendance data is then updated in the system in real time.

This repository contains the **server-side implementation** built with **Golang**, handling all business logic, APIs, and communication with the AI service.

---

## ✨ Features

* **Student Module**

  * Student registration with face features
  * View attendance records
  * Update personal details & face features

* **Faculty Module**

  * Add and manage subjects
  * Monitor student attendance in real time
  * Manage class records

* **Core Attendance System**

  * AI-powered face recognition
  * Frame extraction from classroom videos
  * Automatic presence/absence detection using USN mapping
  * Secure data persistence with PostgreSQL

* **APIs**

  * REST APIs built using **Echo framework**
  * Authentication & authorization via middlewares
  * Smooth communication with external **Python AI service**

---

## 🛠️ Tech Stack

* **Backend**: Golang (Echo Framework)
* **Database**: PostgreSQL
* **AI Service**: Python (Facial Recognition Model)
* **Authentication**: JWT Tokens, Middleware Security

---

## 🏗️ System Architecture

* **Backend (Golang)**: Handles all business logic, API endpoints, and database operations. Built using the **Echo framework**, it provides secure, high-performance REST APIs for students, faculty, subjects, and attendance management.

* **AI Integration (Python Service)**: Facial recognition and model training are handled by a separate Python service. The backend communicates seamlessly with this service for **student face registration** and **real-time attendance detection**, keeping the heavy AI computation isolated from API handling.

* **Database (PostgreSQL)**: All data—including student profiles, facial embeddings, subjects, and attendance records—is stored securely and efficiently. The backend ensures **data integrity, validation, and optimized queries**.

* **Attendance Workflow**:

  1. Students register and submit their face data.
  2. Python AI service trains the model and notifies the backend.
  3. During class, video frames are processed to detect student presence.
  4. Attendance payloads are validated by the backend and stored in the database.

---

## 📂 Folder Structure

```
SmartAttendenceSystem/
├── go.mod
├── go.sum
└── server
    ├── cmd                # App initialization (DB, router)
    ├── internals
    │   ├── domain         # Domain models
    │   ├── handler        # API route handlers
    │   ├── middlewares    # Auth & access control
    │   ├── repository     # PostgreSQL repository
    │   └── service        # Business logic services
    ├── pkg
    │   └── utils          # JWT, password hashing, tokens
    └── main.go            # Entry point
```

---

## ⚡ Quick Start

### 1️⃣ Clone the repository

```bash
git clone https://github.com/your-username/SmartAttendenceSystem.git
cd SmartAttendenceSystem/server
```

### 2️⃣ Setup `.env` file

Create a `.env` file with your PostgreSQL URL:

```env
DATABASE_URL=postgres://user:password@localhost:5432/smart_attendance
```

### 3️⃣ Run the server

```bash
go mod tidy
go run main.go
```

---

## 🌐 Related Repositories & Links

* 🤖 [AI Model Repository](https://github.com/kumar-kiran-24/Automated-Attendance-System)
* 🎓 [Student Panel (Frontend)](https://student-aiet.vercel.app/)
* 🧑‍🏫 [Faculty Panel (Frontend)](https://faculty-aiet.vercel.app/)

---

