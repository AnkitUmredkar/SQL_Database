# SQL Database
## 18.1 Employees Management System

-  This Project SQL queries to perform CRUD operations on employee data in a relational database, enabling seamless management of employee records including creation, retrieval, updating, and deletion.

## SQL Operations
### 1. Create employee table

```bash
CREATE TABLE "Employees" (
	"emp_id"	INTEGER UNIQUE,
	"emp_name"	TEXT NOT NULL,
	"emp_role"	TEXT NOT NULL,
	"emp_age"	INTEGER NOT NULL,
	"emp_address"	TEXT NOT NULL,
	"emp_phone"	INTEGER NOT NULL,
	"emp_salary"	INTEGER NOT NULL,
	PRIMARY KEY("emp_id" AUTOINCREMENT)
);
```

### 2. Insert employee data
- #### Add employee data

```bash
INSERT INTO Employees (emp_name, emp_role, emp_age, emp_address, emp_phone)
VALUES("Ankit", "Flutter Developer", 18, "Surat, Gujarat", 9328456943, 30000);
```

- #### Add multiple employees data

```bash
INSERT INTO Employees (emp_name, emp_role, emp_age, emp_address, emp_phone) 
VALUES("Ankit", "Flutter Developer", 18, "Surat, Gujarat", 9328456943, 40000),
("Kartik", "Full-Stack Developer", 21, "Surat, Gujarat", 9324865173, 20000),
("Pavan", "UI-UX Designer", 23, "Surat, Gujarat", 8564723985, 60000),
("Parth", "Android Developer", 19, "Surat, Gujarat", 9465238719, 30000);
```

### 3. Retrive employee data
- #### Retrive all employees data

```bash
SELECT * FROM Employees
```

- #### Retrive specific Column of employee data

```bash
SELECT emp_name, emp_role FROM Employees;
```

- #### Retrive employees with a particular role
  
```bash
SELECT * FROM Employees WHERE emp_role = "Flutter Developer";
```

- #### Search employees names which contains "An"
```bash
SELECT * FROM Employees WHERE emp_name like '%An';
```

- #### Find employees older than 25
```bash
SELECT * FROM Employees WHERE emp_age > 25;
```

### 4.Update employee data

- #### Udate employee salary where phone == 9382871562
```bash
UPDATE Employees SET emp_salary = 50000 WHERE emp_phone = 9382871562;
```

### 5. Delete employee data

- #### Delete all employess data
```bash
DELETE FROM Employees;
```

- #### Delete all employees under 20
```bash
DELETE FROM Employees WHERE emp_age < 20;
```

## Table
<img src="https://github.com/user-attachments/assets/36a3909c-e6a7-49f7-980c-70eb840b80f9"/>
