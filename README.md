# 🎓 Student Management System – Oracle 21c

## 📝 Project Title:
**Student Management System**  
Capstone Project | Academic Year: 2024–2025  
Institution: Adventist University of Central Africa (AUCA)

## 👤 Student Information:
- **Name:** Kevin Manzi Eric
- **Student ID:** 27387  
- **Program:** Bachelor of Science in Computer Science  
- **Database Name (PDB):** KEVIN27387

## 👨‍🏫 Lecturer:
- **Name:** Dr. Niyigena Gilbert  
- **Department:** Information Systems  
- **Course:** Database Systems – PL/SQL Capstone Project  

---

## 📖 Introduction

This Student Management System is a comprehensive PL/SQL-based application built using **Oracle 21c**. Designed to mimic the functionality of a real-world academic institution, this system handles student data, course management, enrollments, and transactions. It is structured across **eight development phases**, following a capstone methodology to simulate software engineering practices and database system design.

Each component—ranging from schema creation to packaged procedures and dynamic testing—was thoughtfully developed to demonstrate a deep understanding of relational modeling, procedural logic, and Oracle-specific database features like triggers, views, and packages.

---

## 📦 Phase I – Database Schema Design

In this phase, four primary tables were designed:

1. **Students:** Captures student bio and enrollment data  
2. **Courses:** Lists all available academic courses  
3. **Enrollments:** Tracks which students are enrolled in which courses  
4. **Transactions:** Manages tuition and fee payment records  

Each table uses **primary and foreign keys** for referential integrity, alongside `NOT NULL` and `CHECK` constraints to enforce business rules.

---

## 🧱 Phase II – Constraints & Table Management

We implemented:

- **NOT NULL**, **CHECK**, and **FOREIGN KEY** constraints
- Ensured data normalization
- Defined **composite and unique constraints** where applicable
- Enforced **data type integrity**

All DDL scripts are written and tested in Oracle 21c using SQL Developer and Kali Linux VirtualBox setup.

---

## ✍️ Phase III – Data Population

This phase focused on inserting real-world data:

- 10 students with unique birthdates and enrollment dates  
- 10 distinct courses with credits and descriptions  
- Multiple enrollment records ensuring student-course combinations  
- 10+ transactions across different students for fees, refunds, and tuition payments

---

## 👁️ Phase IV – Views and Indexes

To simplify reporting and optimize queries:

- Views were created to retrieve frequently accessed information like:
  - Total transactions per student
  - Recently enrolled students
  - Enrollment summary reports

- Indexes were created on `student_id`, `course_id`, and `transaction_date` for performance optimization.

---

## 🔄 Phase V – Triggers

Three critical triggers were developed:

1. **BEFORE INSERT** on Enrollments: prevents duplicate enrollments.
2. **AFTER INSERT** on Transactions: logs financial activity.
3. **BEFORE UPDATE** on Students: audit trail of name changes.

These were tested thoroughly for edge cases, ensuring the database remains consistent even during complex insert/update scenarios.

---

## 🧮 Phase VI – Procedures and Functions

Custom procedures and functions provide business logic:

- `add_student`: Adds a new student while checking for duplicates
- `enroll_student`: Enrolls a student in a course, with checks on availability
- `calculate_fees`: Function to calculate total payable for a student
- `get_student_summary`: Returns all details of a student (name, courses, balance)

These are stored in the database and callable from client-side applications or scripts.

---

## 📦 Phase VII – Packages

We encapsulated reusable code into **PL/SQL Packages**:

- `student_pkg`: Contains procedures like `register`, `enroll`, `pay_fees`
- Facilitates modular programming, easy debugging, and team collaboration
- Package specification and body are included in this repository

---

## 🧪 Phase VIII – Testing and Final Evaluation

Comprehensive testing covered:

- Insert operations with invalid/valid data
- Constraint validation (foreign key, duplicate insert)
- Trigger actions (logs, preventions)
- Function and procedure outputs
- SQL queries for reporting

Results were verified using `SELECT`, `JOIN`, and `GROUP BY` statements. Edge cases were explored to ensure stability under unusual inputs (e.g., repeated enrollments, null transactions).

---

## 💻 Technologies Used

- **Database:** Oracle 21c
- **Languages:** SQL, PL/SQL
- **Tools:** Oracle SQL Developer, VirtualBox, Kali Linux
- **Environment:** Personal Pluggable Database – `KEVIN27387`

---

## ▶️ How to Run

1. Clone this repository  
2. Open SQL Developer or SQL*Plus  
3. Connect to your Oracle PDB (`KEVIN27387`)  
4. Execute `schema.sql` → to create all tables and constraints  
5. Execute `data_insert.sql` → to populate initial data  
6. Execute `procedures_and_functions.sql`, `triggers.sql`, and `packages.sql`  
7. Use `test_queries.sql` for output verification

---

## 📚 Learning Outcomes

- Mastery in DDL, DML, PL/SQL triggers, and procedural logic
- Real-world application of database principles
- Structured development through phased approach
- Effective testing strategies in relational databases

---

## 📬 Contact

For more information or academic references:

- **Student:** Kevin  
- **Email:** kevin@student.auca.ac.rw  
- **Lecturer:** Dr. Niyigena Gilbert  
- **Course:** Advanced Database Systems (PL/SQL)

---

> “This project demonstrates my ability to design, build, and manage a complete PL/SQL-based database system aligned with enterprise-level academic needs.”

