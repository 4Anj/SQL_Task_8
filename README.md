# Employee Management: Stored Procedures and Functions (MySQL)
This mini project demonstrates how to create stored procedures and functions in MySQL using an Employees table. It showcases reusable SQL blocks for querying employee data with parameters and conditional logic.

## Objective
Learn to write stored procedures and functions in SQL

Use parameters and conditional logic

Gain hands-on experience with reusable SQL blocks

## Technologies Used
MySQL Workbench

SQL Stored Procedures

SQL User-Defined Functions

## Table
Employees

| Column            | Type          | Description               |
| ----------------- | ------------- | ------------------------- |
| `EmpID`           | INT (PK)      | Unique ID of the employee |
| `EmpName`         | VARCHAR(100)  | Employee's name           |
| `Department`      | VARCHAR(50)   | Department name           |
| `Salary`          | DECIMAL(10,2) | Monthly salary            |
| `ExperienceYears` | INT           | Total years of experience |


### Sample Data Included:
```sql
INSERT INTO Employees (EmpID, EmpName, Department, Salary, ExperienceYears) VALUES
(101, 'Anjana', 'IT', 80000, 2),
(102, 'Ravi', 'HR', 60000, 5),
(103, 'Meera', 'Finance', 120000, 10),
(104, 'John', 'IT', 90000, 7),
(105, 'Priya', 'Marketing', 55000, 1);
```
### Stored Procedure: GetEmployeesAboveSalary
```sql
CALL GetEmployeesAboveSalary(70000);
```

### SQL Function: GetExperienceLevel
```sql

SELECT EmpName, ExperienceYears, GetExperienceLevel(ExperienceYears) AS Level
FROM Employees;
```
