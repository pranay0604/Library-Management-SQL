# 📚 Library Management System Database

## Overview

This project is a relational database system for managing a library’s operations using **SQL Server**. It enables administrators to effectively manage book inventory, authors, and patron data, while leveraging **Advanced SQL Techniques** for efficient data manipulation, reporting, and system consistency.

---

## Features

- Store and manage information about books, authors, and library patrons.
- Search books by title, author, or ISBN with flexible filtering options.
- Track book availability, borrowing, and returning.
- Generate detailed reports using advanced SQL features.
- Maintain data accuracy and efficiency using upsert logic.

---

## Technologies

- **SQL Server**
- **T-SQL** (DDL, DML, `MERGE`, CTEs, window functions, subqueries, `SELECT INTO`)

---

## Database Schema

### 📘 `Books` Table

| Column     | Data Type     | Description                  |
|------------|---------------|------------------------------|
| book_id    | `INT` (PK)     | Auto-generated book ID       |
| title      | `VARCHAR(255)` | Book title                   |
| author_id  | `INT` (FK)     | References `Authors` table   |
| isbn       | `VARCHAR(20)`  | Unique book identifier (ISBN)|
| available  | `BIT`          | 1 for available, 0 for borrowed |

---

### ✍️ `Authors` Table

| Column      | Data Type     | Description                 |
|-------------|---------------|-----------------------------|
| author_id   | `INT` (PK)     | Unique author ID            |
| name        | `VARCHAR(255)` | Full name                   |
| birthdate   | `DATE`         | Date of birth               |
| nationality | `VARCHAR(100)` | Country of origin           |

---

### 👥 `Patrons` Table

| Column     | Data Type     | Description                  |
|------------|---------------|------------------------------|
| patron_id  | `INT` (PK)     | Unique patron ID             |
| name       | `VARCHAR(255)` | Patron full name             |
| contact    | `VARCHAR(100)` | Email or phone number        |

---

## Advanced SQL Concepts Used

- **Common Table Expressions (CTEs):** For hierarchical queries and reporting.
- **Window Functions:** For generating rankings, partitions, and trends.
- **Subqueries:** Used for dynamic filtering and nested logic.
- **`MERGE` Statement:** Handles efficient upsert logic for borrow/return operations.
- **`SELECT INTO`:** For temporary report creation without modifying base tables.

---

## Project Goals

- Build a well-structured database schema with strong relational integrity.
- Improve query performance and scalability using SQL Server best practices.
- Enable insightful reporting and analysis for administrative decision-making.
- Ensure consistent data states through transactional upsert logic.

---

