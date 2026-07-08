# 🎓 Online Learning Platform Database Management System

A comprehensive PostgreSQL database project that models an online learning platform similar to Unacademy. The system supports course management, student enrollment, educator administration, subscriptions, assessments, progress tracking, reviews, and analytics through a well-normalized relational database design.

---

## 📌 Project Overview

This project was developed as part of a Database Management Systems course to demonstrate the complete database development lifecycle:

- Requirement Analysis
- Entity-Relationship (ER) Modeling
- Relational Schema Design
- Database Normalization
- SQL DDL Implementation
- Data Population
- Complex Query Development

The platform enables students to enroll in courses, track learning progress, attempt tests, review courses, and manage subscriptions while educators create content and administrators oversee platform operations.

---

## 🚀 Features

### 👨‍🎓 Student Module
- Student registration and profile management
- Subscription-based access
- Course enrollment
- Lecture progress tracking
- Test participation and score management
- Course bookmarking
- Course reviews and ratings

### 👨‍🏫 Educator Module
- Educator profile management
- Verification workflow
- Course creation and management
- Teaching assignments
- Performance tracking

### 👨‍💼 Administrator Module
- Educator verification
- Course monitoring
- Platform management
- Category management

### 📚 Learning Management
- Course catalog
- Lecture management
- Study material repository
- Course categorization

### 📝 Assessment System
- Test creation
- Question management
- Test attempts
- Marks tracking

---

## 🗄️ Database Design

The database follows relational database design principles and is normalized to reduce redundancy and maintain data integrity.

### Core Entities

- Student
- Educator
- Administrator
- Course
- Category
- Subscription
- Lecture
- Study Material
- Test
- Question
- Review
- Bookmark
- Enrollment
- Lecture Progress
- Test Attempt

---

## 📊 Entity Relationship Diagram

The project includes a complete ER Diagram representing entity relationships and cardinalities.

```
Student ── Enrolls ── Course
   │                     │
   │                     │
Review              Lecture
   │                     │
   └─────────────── Progress

Educator ── Teaches ── Course

Course ── Test ── Question

Student ── Test Attempt ── Test
```

---

## 🔄 Relational Schema Highlights

### Student
```sql
student(
    student_id,
    name,
    email,
    password,
    phone,
    profile_details,
    subscription_date,
    subscription_id
)
```

### Course
```sql
course(
    course_id,
    title,
    description,
    price,
    duration,
    number_of_lectures,
    category_id,
    admin_id
)
```

### Educator
```sql
educator(
    educator_id,
    name,
    email,
    verification_status,
    salary,
    admin_id
)
```

---

## 🏗️ Database Constraints Implemented

### Primary Keys
- Unique identification for all entities

### Foreign Keys
- Referential integrity across relations

### Check Constraints
Examples:

```sql
rating BETWEEN 1 AND 5
```

```sql
duration > 0
```

```sql
marks > 0
```

### Unique Constraints

```sql
email UNIQUE
```

### Cascading Operations

```sql
ON DELETE CASCADE
ON UPDATE CASCADE
```

---

## 📁 Project Structure

```text
├── 202401431_ddl_script.txt
├── 202401431_entity_relationship_diagram.pdf
├── 202401431_relational_diagram.pdf
├── insert_script.sql
├── select_queries.sql
└── README.md
```

---

## 💻 Technologies Used

- PostgreSQL
- SQL
- ER Modeling
- Relational Database Design
- Database Normalization
- DBMS Concepts

---

## 🎯 Learning Outcomes

Through this project, I gained practical experience in:

- Designing scalable relational databases
- Entity-Relationship modeling
- Schema mapping
- Normalization (1NF, 2NF, 3NF, BCNF)
- Writing complex SQL queries
- Enforcing data integrity constraints
- Managing many-to-many relationships
- Implementing real-world database systems

---

## 📈 Future Enhancements

- Stored Procedures
- Database Triggers
- Role-Based Access Control
- Recommendation System
- Course Completion Certificates
- Dashboard Analytics
- REST API Integration

---

## 👨‍💻 Author

**Chandan Chhaganlal Luhar**

B.Tech ICT with Minor in Computational Science  
Dhirubhai Ambani University, Gandhinagar

📧 202401431@dau.ac.in  
🔗 LinkedIn: linkedin.com/in/chandanluhar  
💻 GitHub: github.com/B-202401431

---

### ⭐ If you found this project interesting, consider giving it a star!
