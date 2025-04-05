# SQL
This repository contains a comprehensive collection of **SQL interview questions** to help you prepare for technical interviews. These questions cover a wide range of topics, 
from basics to advanced concepts, ensuring you're well-prepared for your next interview.

---

## 🚀 Table of Contents

Here’s the full categorized list of 100 questions with linked titles for your GitHub `README.md` file:

---

### 🎯 SQL Fundamentals
1. [What is Angular and what are its key features?](#1-what-is-angular-and-what-are-its-key-features)  


## 📘 Introduction

Welcome to the **.SQL Interview Questions** repository! Whether you're a beginner or an experienced developer, this repository will help you solidify your knowledge of SQL and 
related technologies. 

### What You'll Find Here:
- Questions categorized by topic for easy navigation.
- Comprehensive answers to help you understand concepts better.
- Code examples for practical understanding.

Feel free to contribute to this repository and make it even more valuable for the community!

---

## 🎯 SQL Fundamentals

### 1. What is SQL and what is it used for?  
**SQL** stands for **Structured Query Language**. It is the standard language used to communicate with **relational databases**. Using SQL, we can perform various operations such as **storing, retrieving, updating, and deleting data** in a database. 

Think of SQL as a way to "ask questions" or "give commands" to a database. Whether you want to find specific information, add new records, or make changes to existing data, SQL is the tool you use.

**What is SQL Used For?**

- **Creating and managing databases and tables** – defining the structure where data will be stored.
- **Inserting data** – adding new rows of information to tables.
- **Querying data** – extracting specific information using conditions.
- **Updating data** – changing values in existing records.
- **Deleting data** – removing records from tables.
- **Managing permissions** – controlling who can access or modify the data.
- **Creating stored procedures, views, and triggers** – automating and organizing database operations.

**Example**

To get all employees’ names from an `Employees` table:
```sql
SELECT Name FROM Employees;
```

To insert a new employee:
```sql
INSERT INTO Employees (Name, Position) VALUES ('John Doe', 'Manager');
```

**Answer Summary:**

- SQL = Structured Query Language  
- Used to interact with relational databases  
- Can **insert, update, delete, and fetch** data  
- Also used for **database structure and user management**

<br>

### 2. Describe the difference between SQL and NoSQL databases.  
SQL and NoSQL are two different types of database systems, and they serve different purposes depending on the type of data and application needs.

**SQL Databases (Relational Databases)**

- Use structured query language (SQL) for defining and manipulating data.
- Data is stored in **tables** with predefined **schemas** (fixed structure of columns and data types).
- Data is related across tables using **foreign keys** and **joins**.
- Best suited for applications where data integrity and relationships are important (e.g., banking, ERP systems).

**Examples:** MySQL, PostgreSQL, SQL Server, Oracle

**NoSQL Databases (Non-relational or Not Only SQL)**

- Use various data models like **document**, **key-value**, **column-family**, or **graph**.
- Data is stored in a **flexible format**, often without a fixed schema.
- Allows for fast scalability and handles large volumes of **unstructured** or **semi-structured** data.
- Ideal for big data, real-time web apps, and applications with rapidly changing requirements.

**Examples:** MongoDB (document), Redis (key-value), Cassandra (column-family), Neo4j (graph)

**Key Differences**

| Feature              | SQL (Relational)                   | NoSQL (Non-relational)                        |
|----------------------|------------------------------------|-----------------------------------------------|
| Schema               | Fixed and structured               | Dynamic and flexible                          |
| Data Storage         | Tables with rows and columns       | Documents, key-value pairs, graphs, etc.      |
| Relationships        | Supports complex joins             | Limited or no joins                           |
| Scalability          | Vertical (adding power to one server) | Horizontal (adding more servers)            |
| Use Case             | Structured data, strong consistency | Big data, high speed, flexible data structure |

**Answer Summary:**

- SQL: Structured, relational, uses tables and fixed schema  
- NoSQL: Flexible, non-relational, stores unstructured data  
- SQL is best for **data integrity**, NoSQL for **scalability and flexibility**  
- SQL uses **joins**; NoSQL often avoids them for speed  
- Choose based on project needs: structure vs. flexibility

---
<br>

### 3. What are the different types of SQL commands?  
SQL commands are categorized based on the type of operation they perform on the database. Each category serves a specific purpose and helps manage data and database structures efficiently.

**1. DDL (Data Definition Language)**  
These commands define the structure of the database, such as tables and schemas.

- `CREATE` – creates a new table or database  
- `ALTER` – modifies an existing table structure  
- `DROP` – deletes a table or database  
- `TRUNCATE` – removes all records from a table but keeps the structure

**2. DML (Data Manipulation Language)**  
These commands are used to manipulate the data inside the database.

- `SELECT` – retrieves data from one or more tables  
- `INSERT` – adds new records into a table  
- `UPDATE` – modifies existing records  
- `DELETE` – removes existing records

**3. DCL (Data Control Language)**  
These commands handle the permissions and access control.

- `GRANT` – gives a user access rights to the database  
- `REVOKE` – removes access rights

**4. TCL (Transaction Control Language)**  
These commands manage transactions to ensure data integrity.

- `COMMIT` – saves all changes made in the current transaction  
- `ROLLBACK` – undoes changes made in the current transaction  
- `SAVEPOINT` – sets a point in a transaction to which you can roll back  
- `SET TRANSACTION` – sets properties for the transaction

**5. DQL (Data Query Language)**  
Sometimes considered separately, though part of DML, it mainly includes:

- `SELECT` – used to query and fetch data from the database

**Answer Summary:**

- **DDL** – Defines structure (`CREATE`, `ALTER`, `DROP`, `TRUNCATE`)  
- **DML** – Manages data (`SELECT`, `INSERT`, `UPDATE`, `DELETE`)  
- **DCL** – Controls access (`GRANT`, `REVOKE`)  
- **TCL** – Handles transactions (`COMMIT`, `ROLLBACK`, `SAVEPOINT`)  
- **DQL** – Queries data (`SELECT`)

---
<br>

### 4. Explain the purpose of the SELECT statement.  
The `SELECT` statement is one of the most important and commonly used SQL commands. Its main purpose is to **retrieve data** from one or more tables in a database. It allows you to choose **what data you want**, **how you want it**, and **from where**.

You can use `SELECT` to fetch all columns, specific columns, filter data using conditions, sort the result, group data, and even join data from multiple tables.

**Basic Syntax:**
```sql
SELECT column1, column2 FROM table_name;
```

**Examples:**

- Get all data from a table:
  ```sql
  SELECT * FROM Employees;
  ```

- Get specific columns:
  ```sql
  SELECT Name, Department FROM Employees;
  ```

- Filter results using `WHERE`:
  ```sql
  SELECT * FROM Employees WHERE Department = 'HR';
  ```

- Sort results:
  ```sql
  SELECT * FROM Employees ORDER BY Name ASC;
  ```

- Group results:
  ```sql
  SELECT Department, COUNT(*) FROM Employees GROUP BY Department;
  ```

**Key Features of SELECT:**

- Retrieves data from one or more tables  
- Can apply filters using `WHERE`  
- Supports sorting using `ORDER BY`  
- Allows grouping using `GROUP BY`  
- Can join multiple tables  
- Supports aggregate functions like `SUM`, `AVG`, `COUNT`, etc.

**Answer Summary:**

- `SELECT` is used to **fetch data** from the database  
- Can retrieve all or specific columns  
- Supports **filtering**, **sorting**, **grouping**, and **joining**  
- Works with **aggregate functions** for summaries and reports

---
<br>

### 5. What is the difference between WHERE and HAVING clauses?  
Both `WHERE` and `HAVING` are used to filter records in SQL, but they are used **at different stages** and serve **different purposes**.

**WHERE Clause**

- Used to **filter rows before** any grouping is done.
- Works on **individual rows** of the table.
- Can be used with `SELECT`, `UPDATE`, and `DELETE` statements.
- Cannot be used with aggregate functions like `SUM()`, `AVG()`, etc.

**Example:**
```sql
SELECT * FROM Employees
WHERE Department = 'HR';
```

**HAVING Clause**

- Used to **filter groups after** the `GROUP BY` operation.
- Works on **aggregated data** (i.e., groups).
- Can be used **only** with `SELECT` statements that include `GROUP BY`.
- **Supports aggregate functions** like `SUM()`, `COUNT()`, etc.

**Example:**
```sql
SELECT Department, COUNT(*) AS TotalEmployees
FROM Employees
GROUP BY Department
HAVING COUNT(*) > 5;
```

**Key Differences**

| Feature            | WHERE                          | HAVING                         |
|--------------------|----------------------------------|---------------------------------|
| Filters            | Rows (before grouping)          | Groups (after grouping)         |
| Used With          | SELECT, UPDATE, DELETE          | SELECT with GROUP BY            |
| Aggregate Functions| Not allowed                     | Allowed                         |
| Execution Order    | Before grouping                 | After grouping                  |

**Answer Summary:**

- `WHERE`: Filters individual **rows** before grouping; can’t use aggregates  
- `HAVING`: Filters **groups** after grouping; used **with aggregate functions**  
- `WHERE` comes **before** `GROUP BY`, `HAVING` comes **after**

---
<br>

### 6. Define what a JOIN is in SQL and list its types.  
**JOIN in SQL and Its Types**

A `JOIN` in SQL is used to **combine rows from two or more tables** based on a related column between them—usually a **foreign key** in one table that matches a **primary key** in another.

JOINs are useful when data is split across multiple tables but you want to fetch it together in a single result set.

**Example:**
```sql
SELECT Employees.Name, Departments.DepartmentName
FROM Employees
JOIN Departments ON Employees.DeptID = Departments.ID;
```

This query fetches employee names along with their department names by joining the `Employees` and `Departments` tables.

---

**Types of JOINs in SQL**

1. **INNER JOIN**
   - Returns only the matching rows from both tables.
   - Non-matching rows are excluded.
   - Most commonly used join type.

   ```sql
   SELECT * FROM A
   INNER JOIN B ON A.ID = B.AID;
   ```

2. **LEFT JOIN (LEFT OUTER JOIN)**
   - Returns all rows from the **left** table and matched rows from the right.
   - If there is no match, NULLs are shown for the right table.

   ```sql
   SELECT * FROM A
   LEFT JOIN B ON A.ID = B.AID;
   ```

3. **RIGHT JOIN (RIGHT OUTER JOIN)**
   - Returns all rows from the **right** table and matched rows from the left.
   - If there is no match, NULLs are shown for the left table.

   ```sql
   SELECT * FROM A
   RIGHT JOIN B ON A.ID = B.AID;
   ```

4. **FULL JOIN (FULL OUTER JOIN)**
   - Returns all rows when there is a match in **either** table.
   - Non-matching rows from both sides get NULLs for the missing columns.

   ```sql
   SELECT * FROM A
   FULL OUTER JOIN B ON A.ID = B.AID;
   ```

5. **CROSS JOIN**
   - Returns the **Cartesian product** of both tables.
   - Every row from the first table is combined with every row from the second.

   ```sql
   SELECT * FROM A
   CROSS JOIN B;
   ```

6. **SELF JOIN**
   - A table is joined with **itself**.
   - Useful for comparing rows within the same table.

   ```sql
   SELECT A.Name, B.ManagerName
   FROM Employees A, Employees B
   WHERE A.ManagerID = B.EmployeeID;
   ```

**Answer Summary:**

- A `JOIN` combines rows from multiple tables based on a related column.
- **INNER JOIN** – only matching rows  
- **LEFT JOIN** – all left + matching right  
- **RIGHT JOIN** – all right + matching left  
- **FULL JOIN** – all matching and non-matching rows  
- **CROSS JOIN** – all combinations (Cartesian product)  
- **SELF JOIN** – join table to itself for comparison

---
<br>

### 7. What is a primary key in a database?  
**What is a Primary Key in a Database?**

A **primary key** is a column (or combination of columns) in a table that **uniquely identifies each row** in that table. It ensures that **no two rows have the same value** for that column and that the value is **never null**.

Think of it like a unique ID for every record—just like a student roll number or an employee ID.

**Key Characteristics:**

- **Uniqueness:** Each value must be unique. No duplicates allowed.
- **Not Null:** Every row must have a value for the primary key.
- **Only one per table:** A table can have only one primary key, though it can consist of multiple columns (composite key).

**Example:**
```sql
CREATE TABLE Students (
    StudentID INT PRIMARY KEY,
    Name VARCHAR(100),
    Class VARCHAR(20)
);
```
Here, `StudentID` is the primary key. You can’t have two students with the same ID or a student with no ID.

**Composite Primary Key Example:**
```sql
CREATE TABLE Enrollments (
    StudentID INT,
    CourseID INT,
    PRIMARY KEY (StudentID, CourseID)
);
```
This uses a combination of `StudentID` and `CourseID` to uniquely identify each row.

**Why Primary Keys Matter:**

- They prevent duplicate records.
- Help maintain data integrity.
- Are used in **relationships** with other tables (foreign keys refer to them).
- Speed up searching and indexing.

**Answer Summary:**

- Uniquely identifies each row  
- Cannot be null or duplicated  
- Only one primary key per table  
- Can be a single or multiple columns (composite key)

---
<br>

### 8. Explain what a foreign key is and how it is used.  
**What is a Foreign Key and How Is It Used?**

A **foreign key** is a column (or set of columns) in one table that is used to **link it to another table**. It creates a relationship between two tables by referencing the **primary key** of another table.

It ensures **referential integrity**, meaning you can’t add a value in the foreign key column that doesn’t exist in the referenced primary key column.

**Example:**

Imagine two tables:

```sql
CREATE TABLE Departments (
    DeptID INT PRIMARY KEY,
    DeptName VARCHAR(100)
);

CREATE TABLE Employees (
    EmpID INT PRIMARY KEY,
    EmpName VARCHAR(100),
    DeptID INT,
    FOREIGN KEY (DeptID) REFERENCES Departments(DeptID)
);
```

In this example:
- `Departments.DeptID` is the primary key.
- `Employees.DeptID` is a **foreign key** that refers to `Departments.DeptID`.

So every employee must belong to a department that already exists in the `Departments` table.

---

**How Foreign Keys Are Used:**

- To **link tables** and model real-world relationships (e.g., employee–department, order–customer)
- To **enforce valid data** (e.g., prevent assigning an employee to a non-existent department)
- Often used when performing **JOINs** to combine related data from multiple tables

**Important Points:**

- A foreign key can reference **only columns with unique values** (usually primary keys or unique keys).
- A table can have **multiple foreign keys**.
- Foreign key values can be **null** (if the relationship is optional).
- You can define rules for what happens when the referenced data is updated or deleted:
  - `ON DELETE CASCADE` – delete related rows automatically
  - `ON UPDATE CASCADE` – update related rows automatically

**Answer Summary:**

- A foreign key creates a **link between two tables**
- It references a **primary key** in another table
- Ensures **data consistency** and **referential integrity**
- Used to model **relationships** (e.g., one-to-many, many-to-one)
- Helps with **JOIN operations** to fetch related data

---
<br>

### 9. How can you prevent SQL injections?  
**How Can You Prevent SQL Injections?**

SQL injection is a **security vulnerability** where attackers insert malicious SQL code into a query, often through user input, to **access or manipulate your database** in unintended ways. This can lead to **data leaks, unauthorized access, or even full database deletion**.

To protect your application, it's important to follow best practices and use secure coding techniques.

---

**Ways to Prevent SQL Injection**

1. **Use Parameterized Queries (Prepared Statements)**  
   - This is the most effective method.
   - Instead of embedding user input directly in SQL, placeholders are used and values are bound later.

   ✅ *Example in SQL Server (C#)*:
   ```csharp
   SqlCommand cmd = new SqlCommand("SELECT * FROM Users WHERE Username = @username", conn);
   cmd.Parameters.AddWithValue("@username", userInput);
   ```

   ✅ *Example in MySQL (PHP)*:
   ```php
   $stmt = $pdo->prepare("SELECT * FROM Users WHERE username = ?");
   $stmt->execute([$userInput]);
   ```

2. **Use Stored Procedures (with parameters)**
   - Stored procedures are safer than inline SQL **only when parameters are used properly**.
   - Avoid building SQL dynamically inside procedures.

   ```sql
   CREATE PROCEDURE GetUserByID (@ID INT)
   AS
   SELECT * FROM Users WHERE UserID = @ID;
   ```

3. **Input Validation and Sanitization**
   - Check for allowed data types, lengths, and formats.
   - Reject suspicious or unexpected input.
   - **Never trust user input** (even from form fields or query strings).

4. **Use ORM (Object-Relational Mapping) Frameworks**
   - Frameworks like Entity Framework, Hibernate, and Django ORM **handle SQL safely** behind the scenes.
   - They generate safe queries automatically.

5. **Limit Database Permissions**
   - Use **least privilege access**. Don’t give apps or users more rights than they need.
   - A login screen should not have permission to drop tables!

6. **Avoid Dynamic SQL**
   - Don’t build queries by string concatenation with user input.
   - If dynamic SQL is required, use proper escaping and input sanitization.

7. **Regularly Monitor and Patch**
   - Keep your database, application, and libraries **updated**.
   - Use security scanners and penetration testing tools.

---

**Example of Vulnerable vs. Safe Code**

🚨 *Vulnerable:*
```sql
SELECT * FROM Users WHERE Username = '" + userInput + "'";
```

If `userInput` is:  
`' OR 1=1 --`,  
the query becomes:  
```sql
SELECT * FROM Users WHERE Username = '' OR 1=1 --'
```

✅ *Safe (Parameterized):*
```sql
SELECT * FROM Users WHERE Username = @username
```

---

**Answer Summary:**

- Use **parameterized queries** (most important)
- Avoid dynamic SQL with user input
- Validate and sanitize all user input
- Use **stored procedures** securely
- Limit database privileges
- Keep systems patched and secure

Remember: **Never trust user input**—always prepare for the worst and code defensively.

---
<br>

### 10. What is normalization? Explain with examples.  
**What is Normalization?**

**Normalization** is the process of organizing data in a database to **reduce redundancy** (repeating data) and **improve data integrity**. It breaks large, complex tables into smaller, related tables and defines relationships between them using keys (like primary and foreign keys).

By normalizing data, we avoid problems like **update anomalies**, **insertion anomalies**, and **deletion anomalies**.

---

**Why Normalize?**

- To avoid storing the same information in multiple places  
- To make the database easier to maintain and update  
- To ensure data is stored logically and efficiently

---

**Normalization Forms (Levels)**

Normalization is usually done in steps, called **normal forms (NF)**. Each step reduces more redundancy and improves structure.

Let’s go through the most common ones with an example.

---

### 1. **Unnormalized Table (Before Normalization)**

| StudentID | StudentName | Course1  | Course2  |
|-----------|-------------|----------|----------|
| 1         | Alice       | Math     | English  |
| 2         | Bob         | Science  | NULL     |

Problems:
- Repeated columns for courses  
- Hard to add more than two courses per student  
- Wasted space with NULLs

---

### 2. **First Normal Form (1NF)**  
**Rule:** Remove repeating groups – Each column must contain **atomic (indivisible)** values.

| StudentID | StudentName | Course   |
|-----------|-------------|----------|
| 1         | Alice       | Math     |
| 1         | Alice       | English  |
| 2         | Bob         | Science  |

Now each record contains only one course per row—data is atomic.

---

### 3. **Second Normal Form (2NF)**  
**Rule:** Be in 1NF and move **partial dependencies** to separate tables. Every non-key column must depend on the **entire primary key**.

Separate students and courses:

**Students Table:**

| StudentID | StudentName |
|-----------|-------------|
| 1         | Alice       |
| 2         | Bob         |

**Enrollments Table:**

| StudentID | Course   |
|-----------|----------|
| 1         | Math     |
| 1         | English  |
| 2         | Science  |

This avoids repeating student names for every course.

---

### 4. **Third Normal Form (3NF)**  
**Rule:** Be in 2NF and remove **transitive dependencies**—non-key columns should not depend on other non-key columns.

Let’s say we had:

| StudentID | StudentName | Department | DeptHead |
|-----------|-------------|------------|----------|

Here, `DeptHead` depends on `Department`, not on `StudentID`. So we separate:

**Departments Table:**

| Department | DeptHead     |
|------------|--------------|
| CS         | Dr. Smith    |
| Physics    | Dr. Johnson  |

And link it via foreign key in Students table.

---

**Answer Summary:**

- **Normalization** = Structuring data to avoid duplication and ensure integrity  
- Involves breaking tables into smaller ones and connecting them with relationships  
- **1NF:** Remove repeating groups  
- **2NF:** Remove partial dependencies  
- **3NF:** Remove transitive dependencies  
- Results in a cleaner, more efficient, and more maintainable database design

A well-normalized database is easier to scale, update, and protect from data inconsistency.
<br>

### 11. Describe the concept of denormalization and when you would use it.  
**What is Denormalization and When Is It Used?**

**Denormalization** is the process of **reversing normalization** by **combining tables** or **adding redundant data** to improve **read performance**. It trades off some data integrity and storage efficiency for faster query results—especially in **read-heavy** applications.

Think of it like this: normalization keeps data neat and tidy, but denormalization lets you **skip some steps** to get answers faster.

---

**Why Use Denormalization?**

In real-world applications—especially in reporting, analytics, and dashboards—joining multiple normalized tables can slow things down. Denormalization reduces the need for complex joins, which can significantly **speed up query performance**.

---

**Example:**

Let’s say you have a normalized setup:

**Customers Table:**

| CustomerID | Name    |
|------------|---------|
| 1          | Alice   |

**Orders Table:**

| OrderID | CustomerID | OrderDate |
|---------|------------|-----------|
| 100     | 1          | 2023-01-01 |

To get customer names with order details, you’d need a JOIN:

```sql
SELECT o.OrderID, o.OrderDate, c.Name  
FROM Orders o  
JOIN Customers c ON o.CustomerID = c.CustomerID;
```

With denormalization, you might just store the customer's name **directly in the Orders table**:

**Orders Table (Denormalized):**

| OrderID | CustomerID | CustomerName | OrderDate |
|---------|------------|--------------|-----------|
| 100     | 1          | Alice        | 2023-01-01 |

Now you don’t need a JOIN to get the customer name—faster, but more redundant.

---

**When to Use Denormalization**

✅ Use when:
- You have **performance issues** with complex JOINs  
- The database is **read-heavy**, like in **reporting systems**, **data warehouses**, or **BI tools**  
- You want to **pre-compute** and store derived or aggregated values  
- Data is **rarely updated**, and real-time consistency isn’t critical

❌ Avoid when:
- Your application is **write-heavy** (more inserts/updates/deletes)
- You need **high consistency** (redundant data is harder to maintain)
- You’re dealing with **frequent changes** (more places to update the same data)

---

**Trade-Offs of Denormalization:**

| Advantage                   | Disadvantage                          |
|----------------------------|---------------------------------------|
| Faster reads               | Data redundancy and larger storage    |
| Fewer joins in queries     | Risk of data inconsistency            |
| Better performance for BI  | Harder to update/maintain             |

---

**Answer Summary:**

- **Denormalization** adds redundancy to improve **query speed**
- Common in **analytics, dashboards**, or **read-heavy** systems
- Speeds up reads by reducing JOINs  
- Comes with risks: **data inconsistency**, more storage, and **maintenance effort**
- Should be used **strategically** based on the application's needs

It's all about the **balance between speed and structure**—denormalization makes things faster, but messier.
<br>

### 12. What are indexes and how can they improve query performance?  
**What Are Indexes and How Can They Improve Query Performance?**

An **index** in SQL is like a **table of contents** in a book. Instead of flipping through every page to find a topic, you jump straight to the page using the index. Similarly, in a database, an index helps the system **locate rows faster** without scanning the entire table.

Indexes are created on one or more columns of a table to **speed up SELECT queries** and sometimes to **enforce uniqueness** (like with primary keys).

---

**How Indexes Improve Performance**

Without an index, SQL performs a **full table scan**—checking every row to find matches. This is slow for large datasets.

With an index, SQL can jump directly to the rows it needs, just like looking up a word in a dictionary.

---

**Example:**

Assume a table `Employees` with 1 million rows:

```sql
SELECT * FROM Employees WHERE LastName = 'Smith';
```

- ❌ *Without index:* SQL checks every row to see if `LastName = 'Smith'` (slow)
- ✅ *With index on LastName:* SQL uses the index to find all rows with `Smith` quickly

---

**Types of Indexes**

1. **Single-Column Index**  
   Created on one column.  
   ```sql
   CREATE INDEX idx_lastname ON Employees(LastName);
   ```

2. **Composite Index (Multi-column)**  
   Covers more than one column.  
   ```sql
   CREATE INDEX idx_name_dept ON Employees(LastName, Department);
   ```

3. **Unique Index**  
   Ensures that the indexed values are unique (automatically created with PRIMARY KEY or UNIQUE constraints).

4. **Clustered Index**  
   - Sorts the actual table rows physically.  
   - Only **one** clustered index per table.
   - Automatically created on the **primary key**.

5. **Non-Clustered Index**  
   - Stores a separate structure with pointers to the actual data.
   - You can create **multiple** non-clustered indexes.

---

**When to Use Indexes**

✅ Ideal for:
- Columns used frequently in **WHERE**, **JOIN**, **ORDER BY**, and **GROUP BY**
- Searching and filtering large datasets
- Enforcing **uniqueness** (e.g., emails or usernames)

❌ Avoid on:
- Columns that are rarely used in search
- Tables with **frequent INSERT/UPDATE/DELETE** (indexes slow down write operations)
- Very small tables (full scan is already fast)

---

**Downsides of Indexes**

- **Slower inserts and updates** (because indexes also need to be updated)
- **More storage space** required
- **Too many indexes** can confuse the query optimizer and actually hurt performance

---

**Answer Summary:**

- **Indexes** speed up data retrieval by allowing SQL to **find rows quickly**
- They work like a **lookup guide** for large datasets
- Best used on **frequently searched or sorted columns**
- **Types include:** clustered, non-clustered, unique, composite
- Trade-off: improved read performance, but **slower writes and more storage**

Use indexes **wisely**—they're powerful tools for performance tuning when used on the right columns.
<br>

### 13. Explain the purpose of the GROUP BY clause.  
**What Is the Purpose of the GROUP BY Clause?**

The **`GROUP BY`** clause in SQL is used to **group rows that have the same values** in specified columns into **summary rows**. It's commonly used with **aggregate functions** like `COUNT()`, `SUM()`, `AVG()`, `MAX()`, and `MIN()` to perform calculations **per group** rather than on the entire dataset.

---

**Why Use GROUP BY?**

- To **summarize** large sets of data  
- To perform **calculations per category or group**  
- To make reports like:  
  - Total sales per region  
  - Average salary per department  
  - Number of students per class

---

**Example:**

Suppose you have a `Sales` table:

| Region   | Amount |
|----------|--------|
| North    | 100    |
| South    | 200    |
| North    | 150    |
| East     | 300    |

To get total sales per region:

```sql
SELECT Region, SUM(Amount) AS TotalSales
FROM Sales
GROUP BY Region;
```

**Result:**

| Region | TotalSales |
|--------|------------|
| North  | 250        |
| South  | 200        |
| East   | 300        |

Now instead of showing individual sales, it summarizes them **per region**.

---

**Important Rules for GROUP BY:**

- All **non-aggregated columns** in the `SELECT` must appear in the `GROUP BY` clause  
- You can **filter groups** using the `HAVING` clause (not `WHERE`)

---

**Using GROUP BY with HAVING:**

To get only regions with sales above 250:

```sql
SELECT Region, SUM(Amount) AS TotalSales
FROM Sales
GROUP BY Region
HAVING SUM(Amount) > 250;
```

---

**Real-World Uses:**

- Count of orders per customer  
- Average marks per student  
- Number of logins per day  
- Sales totals per product category

---

**Answer Summary:**

- `GROUP BY` groups rows with the same value into **summary rows**  
- Often used with **aggregate functions** like `SUM()`, `COUNT()`, `AVG()`  
- Helps generate **reports** and **summary data**  
- Use `HAVING` to filter grouped results  
- Essential for analyzing and organizing large amounts of data by category

It's like sorting data into buckets and then running calculations **inside each bucket**.
<br>

### 14. What is a subquery, and when would you use one?  
<br>

### 15. Describe the functions of the ORDER BY clause.  
<br>

### 16. What are aggregate functions in SQL?  
<br>

### 17. Explain the differences between INNER JOIN, LEFT JOIN, RIGHT JOIN, and FULL JOIN.  
<br>

### 18. How do you insert a new row into a database table?  
<br>

### 19. Explain how to update records in a database table.  
<br>

### 20. What is a SQL View and what are its advantages?  
<br>

---

## 🧩 SQL Data Types and Operators

### 21. List the different data types available in SQL.  
<br>

### 22. What are the differences between CHAR, VARCHAR, and TEXT data types?  
<br>

### 23. How do you use the BETWEEN operator in SQL?  
<br>

### 24. Describe the use of the IN operator.  
<br>

### 25. Explain the use of wildcard characters in SQL.  
<br>

### 26. What is the purpose of the LIKE operator?  
<br>

### 27. How do you handle NULL values in SQL?  
<br>

### 28. What does the COALESCE function do?  
<br>

### 29. What is the difference between UNION and UNION ALL?  
<br>

### 30. Describe the use of arithmetic operators in SQL queries.  
<br>

---

## 🧠 SQL Advanced Queries

### 31. Explain how to use the CASE statement in SQL.  
<br>

### 32. How would you perform a self JOIN?  
<br>

### 33. What is a cross JOIN and when would you use it?  
<br>

### 34. How to implement pagination in SQL queries?  
<br>

### 35. Explain the concept of Common Table Expressions (CTEs) and recursive CTEs.  
<br>

### 36. What are window functions and how are they used?  
<br>

### 37. How can you concatenate column values in SQL?  
<br>

### 38. What is the PIVOT operation and how would you apply it?  
<br>

### 39. Explain the process of combining a query that uses a GROUP BY with one that uses ORDER BY.  
<br>

### 40. How would you find duplicate records in a table?  
<br>

---

## 🏗️ Database Design & Architecture

### 41. What is the Entity-Relationship Model?  
<br>

### 42. Explain the different types of database schema.  
<br>

### 43. What are Stored Procedures and how are they beneficial?  
<br>

### 44. What is a trigger in SQL and when should it be used?  
<br>

### 45. Describe the concept of ACID in databases.  
<br>

### 46. What is database sharding?  
<br>

### 47. How do database indexes work and what types are there?  
<br>

### 48. Describe the process of data warehousing.  
<br>

### 49. Explain the difference between OLTP and OLAP systems.  
<br>

### 50. What are materialized views and how do they differ from standard views?  
<br>

---

## ⚙️ SQL Optimization and Performance

### 51. How do you identify and optimize slow-running queries?  
<br>

### 52. What is query execution plan in SQL?  
<br>

### 53. Explain how to use EXPLAIN or EXPLAIN ANALYZE.  
<br>

### 54. How can indexing affect performance both positively and negatively?  
<br>

### 55. Describe how to measure the performance of SQL queries.  
<br>

### 56. How would you rewrite a query to improve its performance?  
<br>

### 57. What are partitioned tables and how can they optimize performance?  
<br>

---

## 🔐 SQL Security

### 58. How do you implement database encryption in SQL?  
<br>

### 59. What are roles and how do they manage database access?  
<br>

### 60. Explain the concept of row-level security.  
<br>

### 61. Describe how to create and use user-defined functions (UDFs).  
<br>

---

## 🧮 SQL Functions and Expressions

### 62. Describe scalar-valued and table-valued functions.  
<br>

### 63. How would you define a stored procedure with input and output parameters?  
<br>

### 64. What is the difference between a function and a stored procedure?  
<br>

### 65. How do you use the CAST and CONVERT functions?  
<br>

---

## 🔄 Transaction Control and Locking

### 66. What is a database transaction?  
<br>

### 67. Explain the concept of locking and its types in SQL databases.  
<br>

### 68. What are the properties of transactions?  
<br>

### 69. How do you manage transaction isolation levels?  
<br>

### 70. What does it mean to commit or roll back a transaction?  
<br>

---

## ☁️ SQL and Modern Data Ecosystems

### 71. How can SQL be integrated with big data technologies?  
<br>

### 72. Discuss the interoperability of SQL with cloud-based data stores.  
<br>

### 73. What is Data Lake and how can SQL interact with it?  
<br>

### 74. Explain the interaction between SQL and NoSQL within the same application.  
<br>

### 75. How does SQL work within a microservices architecture?  
<br>

---

## 📏 SQL Best Practices and Standards

### 76. What are some common SQL coding practices you follow?  
<br>

### 77. How can you ensure the portability of SQL scripts across different database systems?  
<br>

### 78. What methods do you use for version controlling SQL scripts?  
<br>

### 79. What are the benefits of using stored procedures instead of embedding SQL queries in code?  
<br>

### 80. How do you document SQL code effectively?  
<br>

---

## 📊 Analytical SQL

### 81. How would you find the Nth highest salary from a table?  
<br>

### 82. How do you count the number of occurrences of a specific value in a column?  
<br>

### 83. How can you calculate running totals in SQL?  
<br>

### 84. Explain how to reverse the contents of a column without using a reverse function.  
<br>

### 85. What approach do you use for creating a calendar table, and what are its uses?  
<br>

---

## 🔄 Data Manipulation and ETL

### 86. What is the process of Extract, Transform, Load (ETL)?  
<br>

### 87. How do you import/export data from/to a flat file using SQL?  
<br>

### 88. Explain the steps for a basic ETL process in a data warehousing environment.  
<br>

### 89. How do you cleanse and format data using SQL queries?  
<br>

### 90. What tools do you use for automating data import/export routines?  
<br>

---

## 🧱 Domain-Specific SQL Scenarios

### 91. How would you model a many-to-many relationship in SQL?  
<br>

### 92. Describe how to manage hierarchical data in SQL.  
<br>

### 93. How would you approach writing SQL queries for a reporting application?  
<br>

### 94. Explain how to handle temporal data and time zones in SQL.  
<br>

### 95. How do you use SQL in financial applications for risk and portfolio analysis?  
<br>

---

## 🧩 Troubleshooting and Debugging

### 96. What steps do you take to troubleshoot a failed SQL query?  
<br>

### 97. How can you recover data from a corrupt SQL database?  
<br>

### 98. What methods do you employ to ensure data integrity?  
<br>

### 99. How do you decipher and resolve deadlocks in SQL?  
<br>

### 100. Explain how to use SQL for predictive analysis and machine learning purposes.  
<br>

---

Let me know if you’d like this exported as a markdown file or converted into a presentation format!  

**Summary:**  
Angular is a TypeScript-based framework with features like data binding, dependency injection, components, directives, and reactive programming for scalable SPAs.
<br>
