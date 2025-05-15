# 🏠 Airbnb Clone Project

A full-stack project simulating the core functionalities of Airbnb — focusing on scalable backend development, secure APIs, database architecture, and DevOps automation.

---

## 🎯 Project Overview

The **Airbnb Clone** project replicates a real-world booking platform where users can register, list properties, book stays, and leave reviews. The main goal is to develop a robust backend infrastructure using modern web technologies, ensuring secure, scalable, and maintainable code.

### 🧾 Project Goals

- Practice full-stack development with Django and PostgreSQL.
- Understand relational database modeling.
- Implement secure RESTful APIs.
- Use GitHub for collaboration and CI/CD automation.

---

## 👥 Team Roles

| Role                   | Responsibility                        |
|------------------------|----------------------------------------|
| 👨‍💻 Backend Developer    | Develops API endpoints and business logic. |
| 🧠 Product Owner        | Defines product features and priorities.  |
| 🎨 UI/UX Designer       | Designs intuitive user experiences.     |
| 🧪 QA Tester            | Verifies application reliability and correctness. |
| 🧱 Database Administrator | Designs and manages database structure. |
| ⚙️ DevOps Engineer      | Automates deployments and ensures CI/CD. |
| 📋 Scrum Master         | Facilitates team processes and Agile rituals. |

---

## 🛠️ Technology Stack

| Technology     | Purpose |
|----------------|---------|
| **Django**     | Backend web framework for building REST APIs. |
| **PostgreSQL** | Relational database system. |
| **GraphQL**    | API query language for flexible data access. |
| **Docker**     | Containerization and environment consistency. |
| **GitHub Actions** | Automates CI/CD pipelines. |
| **JWT**        | Authentication and secure token-based sessions. |

---

## 🗄️ Database Design

### 📌 Entities and Fields

**User**
- user_id (PK)
- name
- email
- password_hash
- created_at

**Property**
- property_id (PK)
- title
- description
- owner_id (FK to User)
- price_per_night

**Booking**
- booking_id (PK)
- user_id (FK to User)
- property_id (FK to Property)
- start_date
- end_date
- total_price

**Review**
- review_id (PK)
- user_id (FK)
- property_id (FK)
- rating
- comment

**Payment**
- payment_id (PK)
- booking_id (FK)
- amount
- payment_status
- payment_date

### 🔁 Relationships

- A user can have many bookings.
- A booking is linked to one property and one user.
- A property has many reviews.
- Each booking can have one payment.

---

## 🔓 API Security

### 🔐 Key Security Measures

- **Authentication**: Using **JWT** tokens for secure user sessions.
- **Authorization**: Access control for booking, editing, and managing resources.
- **Rate Limiting**: Prevent brute-force and DoS attacks.
- **Data Validation**: Use of serializers and field constraints.
- **HTTPS/SSL**: Ensures secure data in transit.

---

## 🔁 CI/CD Pipeline

### 🛠 What is CI/CD?

**CI/CD** (Continuous Integration/Continuous Deployment) is the automation of software delivery:
- **CI**: Automatically runs tests and integrates code with the main branch.
- **CD**: Deploys tested code to staging/production automatically.

### ⚙️ Tools Used
- **GitHub Actions**: Automates testing and deployment.
- **Docker**: Ensures consistent builds across environments.

### 🔄 Benefits
- Faster, more reliable deployments.
- Reduces human errors.
- Immediate feedback on code changes.

---

## 🔍 Feature Breakdown

| Feature              | Description |
|----------------------|-------------|
| 👤 User Registration/Login | Users can create accounts, login, and manage sessions. |
| 🏠 Property Listing    | Users can list and browse rental properties. |
| 📅 Booking System      | Users can book properties with availability management. |
| 💳 Payment Integration | Bookings include payment tracking and status updates. |
| 🌟 Reviews             | Guests can rate and review properties. |
| 🧾 Admin Panel         | Admins can view and manage all system data. |

---

## ✅ Acceptance Criteria Example

**Feature:** Booking System  
**Criteria:**
- User must be logged in to book a property.
- System checks availability before booking.
- Booking dates must not overlap.
- Total price is calculated based on duration and nightly rate.
- Confirmation email is sent on success.

---

## 📌 Learning Objectives

- Learn how real-world web apps are planned and executed.
- Understand team collaboration and Agile methodologies.
- Implement secure, scalable backends using Django.
- Create and optimize relational databases.
- Integrate DevOps tools for automated testing and deployment.

---

## 📂 Folder Structure (optional)

airbnb-clone/
├── backend/
│
├── bookings/
│ ├── users/
│ ├── properties/
│ └── reviews/
├── database/
│ └── schema.sql
├── .github/workflows/
│ └── ci.yml
└── README.md


---

## 🧠 Final Thoughts

This project showcases a production-grade design for a rental platform, emphasizing technical depth, teamwork, and secure development practices.

