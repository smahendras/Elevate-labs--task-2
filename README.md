# 🎓 College Database Management System

This project demonstrates the creation and management of a relational database for a college using MySQL. It includes two core tables: `studentRecord` and `guardian`, with a foreign key relationship to maintain data integrity.

## 📁 Project Overview

The goal is to build a simple yet structured database that stores student details and their corresponding guardian information. The database supports operations like insertion, deletion, updates, and schema inspection.

## 🛠️ Tasks Performed

### 1. Database Setup
- Created a database named `college`.
- Selected the database using `USE college`.

### 2. Table Creation

#### `studentRecord`
Stores student information:
- `enroll`: Primary key (INT)
- `fname`, `lname`: First and last names (VARCHAR)
- `address`: Full address (VARCHAR)
- `DOB`: Date of birth (DATE)
- `religion`: Religion (VARCHAR)
- `adhaarNo`: Aadhaar number (VARCHAR)

#### `guardian`
Stores guardian details:
- `enroll`: Foreign key referencing `studentRecord(enroll)`
- `fatherName`, `motherName`: Guardian names (VARCHAR)
- `fatherOccupation`: Occupation (VARCHAR)
- `familyContact`: Contact number (BIGINT)

### 3. Data Insertion
- Inserted 10 sample records into `studentRecord`.
- Inserted 10 matching records into `guardian`.

### 4. Schema Modification
- Altered `familyContact` to `BIGINT` to support 10-digit mobile numbers.

### 5. Data Manipulation
- Updated a guardian's `motherName` using `UPDATE`.
- Deleted a student record after removing the corresponding guardian entry.

### 6. Data Verification
- Used `SELECT *` to view contents of both tables.
- Used `DESC` to inspect table structures.

## Outcome

The database now supports:
- Referential integrity between students and guardians.
- Safe deletion and updates.
- Scalable contact storage.

## Technologies Used
- MySQL

## How to Run

1. Open MySQL Workbench or CLI.
2. Copy and execute the SQL statements step-by-step.
3. Verify table creation and data using `SELECT` and `DESC`.

---

Feel free to extend this project with additional tables like courses, grades, or attendance. Contributions and suggestions are welcome!
