README: SQL Script for Library Employee Database

Database Name: LIBRARY

This SQL script sets up and manipulates a sample Employees table inside a database called LIBRARY. It demonstrates common operations such as creating tables, inserting records, updating values, deleting rows, and querying data with different conditions.

📁 1. Database and Table Setup
CREATE DATABASE LIBRARY;
Creates a new database named LIBRARY.

USE LIBRARY;
Switches the session to the LIBRARY database.

CREATE TABLE Employees (...)
Defines a table named Employees with fields:

emp_id: Auto-incrementing primary key

first_name, last_name: Employee names

email: Email address

department: Department name

salary: Salary (in decimal format)

join_date: Date the employee joined

✍️ 2. Insert Sample Records
Inserts 5 sample employees, including cases with NULL values to simulate missing data (e.g., salary, email, last name).

🔍 3. Data Retrieval and Basic Queries
SELECT * FROM Employees;
Displays all records from the Employees table.

SELECT emp_id, first_name, email FROM Employees WHERE first_name = 'Mike';
Fetches basic info about Mike.

✏️ 4. Data Updates
UPDATE Employees SET email = ...
Updates Mike's missing email.

UPDATE Employees SET salary = ...
Updates Mike's missing salary.

UPDATE Employees SET last_name = ...
Fills in Emily's missing last name.

UPDATE Employees SET join_date = CURDATE();
Sets Emily’s missing join date to today’s date.

UPDATE Employees SET department = 'Sales'
Updates Robert's missing department.

❌ 5. Deletion
DELETE FROM Employees WHERE emp_id = 5;
Deletes the employee (Robert) who joined before 2021.

📊 6. Query Operations
Select Operations:

All columns:
SELECT * FROM Employees;

Specific columns:
SELECT first_name, department, salary FROM Employees;

Filter Conditions:

HR department:
WHERE department = 'HR'

Finance department, salary > 50k:
WHERE department = 'Finance' AND salary > 50000

HR or IT department:
WHERE department = 'HR' OR department = 'IT'

First name starts with 'J':
WHERE first_name LIKE 'J%'

Salary in range:
WHERE salary BETWEEN 45000 AND 60000

Sorting:

Ascending salary:
ORDER BY salary ASC

Most recent joiners first:
ORDER BY join_date DESC

Limiting:

First 3 records only:
LIMIT 3

Combining Filters:

Top 2 highest-paid in Marketing or Sales:
WHERE department IN ('Marketing', 'Sales') ORDER BY salary DESC LIMIT 2

Aliasing:

Renames columns for clarity in output:
AS 'First Name', AS 'Dept', etc.

✅ Summary
This script covers:

Database and table creation

Insertion of sample data (including NULLs)

Data updates and clean-up

Conditional queries

Ordering, filtering, and limiting results

Data aliasing for better readability

Use this as a foundation for learning and experimenting with SQL in a structured way.
