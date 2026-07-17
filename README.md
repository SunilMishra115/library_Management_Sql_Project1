# 📚 Library Management System using SQL

![SQL](https://img.shields.io/badge/SQL-MySQL-blue)
![Database](https://img.shields.io/badge/Database-Relational-success)
![Project](https://img.shields.io/badge/Project-Library%20Management-orange)

## 📖 Project Overview

The **Library Management System** is a complete SQL project developed to demonstrate real-world database design and SQL operations. It simulates the day-to-day operations of a library, including managing books, members, employees, branches, book issuance, and returns.

This project is designed for:

- SQL Beginners
- Data Analyst Portfolio
- Data Engineer Portfolio
- Database Management Practice
- College Final Year Projects
- SQL Interview Preparation

---

# 🎯 Project Objectives

- Design a normalized relational database.
- Implement CRUD operations.
- Practice Joins and Relationships.
- Perform Business Analysis using SQL.
- Create reports using Aggregate Functions.
- Implement CTAS (Create Table As Select).
- Build Stored Procedures.
- Solve real-world business problems using SQL.

---

# 🏗 Database Schema

The project consists of the following relational tables:

| Table Name | Description |
|------------|-------------|
| Branch | Stores branch details |
| Employees | Stores employee information |
| Members | Stores library member information |
| Books | Stores book inventory |
| Issued_Status | Stores issued book records |
| Return_Status | Stores returned book records |

---

# 🗃 Database Relationships

```
                    Branch
                      │
          ┌───────────┴───────────┐
          │                       │
      Employees              Manager
          │
          │
Members ─────── Issued_Status ─────── Books
                     │
                     │
              Return_Status
```

---

# 📂 Database Tables

## 1️⃣ Branch

Stores branch information.

Columns

- Branch ID (Primary Key)
- Manager ID
- Branch Address
- Contact Number

---

## 2️⃣ Employees

Stores employee details.

Columns

- Employee ID (Primary Key)
- Employee Name
- Position
- Salary
- Branch ID (Foreign Key)

---

## 3️⃣ Members

Stores library member details.

Columns

- Member ID (Primary Key)
- Member Name
- Member Address
- Registration Date

---

## 4️⃣ Books

Stores all available books.

Columns

- ISBN (Primary Key)
- Book Title
- Category
- Rental Price
- Status
- Author
- Publisher

---

## 5️⃣ Issued Status

Stores information about issued books.

Columns

- Issued ID (Primary Key)
- Member ID (Foreign Key)
- Book Name
- Issue Date
- Book ISBN (Foreign Key)
- Employee ID (Foreign Key)

---

## 6️⃣ Return Status

Stores returned book details.

Columns

- Return ID (Primary Key)
- Issued ID
- Return Book Name
- Return Date
- Return Book ISBN (Foreign Key)

---

# 🚀 SQL Tasks Implemented

## 🔹 CRUD Operations

### Task 1
Create a new book record.

### Task 2
Update an existing member's address.

### Task 3
Delete a record from the Issued Status table.

### Task 4
Retrieve all books issued by a specific employee.

### Task 5
Find members who have issued more than one book.

---

## 🔹 CTAS (Create Table As Select)

### Task 6

Create summary tables showing:

- Book information
- Number of times each book has been issued

---

## 🔹 Data Analysis

### Task 7

Retrieve all books belonging to a specific category.

### Task 8

Calculate total rental income by category.

### Task 9

List members registered within the last 180 days.

### Task 10

Display employees along with their branch details and manager information.

### Task 11

Create a table containing books with rental prices above a specified threshold.

### Task 12

Retrieve books that have not yet been returned.

---

# 🚀 Advanced SQL Operations

## Task 13

Identify members with overdue books (30-day return policy).

Display:

- Member Name
- Book Title
- Issue Date
- Days Overdue

---

## Task 14

Automatically update book availability after return.

- Issued Book → Status = 'No'
- Returned Book → Status = 'Yes'

---

## Task 15

Generate Branch Performance Report.

Includes:

- Books Issued
- Books Returned
- Total Rental Revenue

---

## Task 16

Create Active Members table using CTAS.

Criteria:

Members who issued at least one book within the last six months.

---

## Task 17

Find the Top 3 employees who processed the highest number of book issues.

Display:

- Employee Name
- Number of Books Issued
- Branch

---

## Task 18

Stored Procedure

Create a Stored Procedure to manage book status.

Business Logic:

- Book Issued → Status becomes **No**
- Book Returned → Status becomes **Yes**

---

## Task 19

CTAS for Overdue Books and Fine Calculation.

Create a new table containing:

- Member ID
- Number of Overdue Books
- Total Books Issued
- Total Fine

Fine Calculation:

```
$0.50 × Number of Overdue Days
```

---

# 📊 SQL Concepts Covered

This project demonstrates:

- CREATE DATABASE
- CREATE TABLE
- PRIMARY KEY
- FOREIGN KEY
- INSERT
- UPDATE
- DELETE
- SELECT
- WHERE
- ORDER BY
- GROUP BY
- HAVING
- INNER JOIN
- LEFT JOIN
- Aggregate Functions
- CASE WHEN
- Date Functions
- CTAS
- Stored Procedures
- Business Reporting

---

# 📈 Business Insights Generated

Using SQL, this project answers important business questions such as:

- Which books are currently issued?
- Which books have not yet been returned?
- Which members frequently borrow books?
- Which books are overdue?
- How much revenue is generated by each book category?
- Which employee processes the highest number of book issues?
- Which branch performs the best?
- Which members are active?
- How much fine should overdue members pay?

---

# 💻 Technologies Used

- SQL
- MySQL
- Relational Database Management System (RDBMS)

---

# 📁 Repository Contents

| File | Description |
|------|-------------|
| `README.md` | Project documentation |
| `Practise_question.sql` | SQL project questions and practice tasks |
| `Library_Solution_sql.sql` | Complete solutions for all SQL tasks |
| `insert_queries.sql` | SQL script to insert sample data (Part 1) |
| `insert_queries2.sql` | SQL script to insert additional sample data (Part 2) |
| `books.csv` | Books dataset |
| `branch.csv` | Branch dataset |
| `employees.csv` | Employees dataset |
| `members.csv` | Members dataset |
| `issued_status.csv` | Issued books dataset |
| `return_status.csv` | Returned books dataset |
| `ER_library_sql.pdf` | Entity Relationship (ER) Diagram |

---

# 🎓 Learning Outcomes

After completing this project, you will gain practical knowledge of:

- Relational Database Design
- SQL Query Writing
- CRUD Operations
- Database Relationships
- Aggregate Analysis
- Business Reporting
- CTAS
- Stored Procedures
- Real-world SQL Problem Solving

---

# 🚀 Future Enhancements

- Views
- Triggers
- Window Functions
- Indexing
- Transactions
- User Authentication
- Power BI Dashboard
- Tableau Dashboard
- Python Integration

---

# ⭐ Why This Project?

This project is an excellent addition to a Data Analyst or Data Engineer portfolio because it demonstrates:

- Database Design
- Data Modeling
- SQL Query Optimization
- Reporting Skills
- Analytical Thinking
- Business Problem Solving

---

# 🤝 Contributing

Contributions are welcome!

If you'd like to improve this project:

1. Fork the repository.
2. Create a feature branch.
3. Commit your changes.
4. Push to your branch.
5. Open a Pull Request.

---

# 📜 License

This project is licensed under the **MIT License**.

---

# 👨‍💻 Author

**Sunil Mishra**

SQL Developer | Data Analytics Enthusiast

If you found this project useful, please consider giving it a ⭐ on GitHub.

---

## 🌟 Support

If you like this project, don't forget to **Star ⭐ the repository** and share it with others.

Happy Learning! 🚀
