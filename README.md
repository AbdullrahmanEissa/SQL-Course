# SQL Mastery 

Practical SQL labs and notes following the comprehensive FreeCodeCamp SQL Course, containerized with Docker & MySQL.

## Tech Stack
- **Database Engine:** MySQL 8.0
- **Environment:** Docker & Docker Compose
- **Host OS:** Linux Ubuntu

## Project Roadmap

- [ ] **Day 1:** Database Concepts, Tables & Keys Overview
- [ ] **Day 2:** DDL & Constraints (`CREATE`, `INSERT`, `UPDATE`, `DELETE`)
- [ ] **Day 3:** Company Database Setup & Basic Queries
- [ ] **Day 4:** Aggregate Functions & Wildcards
- [ ] **Day 5:** Unions, Joins & Nested Queries
- [ ] **Day 6:** Foreign Key Constraints (`ON DELETE`) & Triggers
- [ ] **Day 7:** ER Diagrams & Schema Normalization

## How to Run Locally

1. Start the database container:
   ```bash
   docker compose up -d


# SQL Basics Mastery Course

SQL (Structured Query Language) is the global standard language used to communicate with Relational Database Management Systems (RDBMS). It goes beyond merely retrieving data; it is the command language that controls building the database structure, managing its data, and maintaining its security.

---

## Module 1: Main Categories of SQL

SQL is divided into main categories based on the purpose of its commands:

### 1. Data Definition Language (DDL)

This is used to build and modify the metadata and the core structure of the database.

* **`CREATE TABLE`**: Used to build a new table structure, defining column names and data types.


* **Constraints**: Strict rules applied to ensure data integrity, including `PRIMARY KEY` (unique identifier), `NOT NULL` (prevents empty values), `UNIQUE` (prevents duplication), `FOREIGN KEY` (links tables), and `DEFAULT` (assigns a default value).


* **`ALTER TABLE`**: Modifies the structure of an existing table (like adding or dropping columns) without losing the existing data.


* **`DROP TABLE`**: Permanently deletes the table structure and all the data contained within it.



### 2. Data Manipulation Language (DML)

This is used to handle the actual data (rows/records) inside the tables (note that `SELECT` is sometimes categorized separately under DQL).

* **`INSERT INTO`**: Adds new rows or records to a table.


* **`UPDATE`**: Modifies existing values in a row; you must always use a `WHERE` clause with it to avoid modifying every row in the table.


* **`DELETE`**: Removes one or more rows; a `WHERE` clause must be used to prevent deleting all data.


* **`SELECT`**: Retrieves and reads data from the database.



---

## Module 2: Filtering and Organizing Data

Extracting data accurately is what separates slow queries from professional ones.

### Filtering and Searching Tools

* **`WHERE`**: Filters records based on specific conditions using comparison operators (`=`, `>`, `<`, `!=`) and logical operators (`AND`, `OR`, `NOT`).


* **`IN`**: A smart alternative to writing multiple `OR` conditions, used to check if a value matches any item in a specified list.


* **`BETWEEN`**: Filters data that falls within a continuous range (like dates or numbers) and includes both the start and end points.


* **`LIKE`**: Enables "pattern matching" using the percent sign `%` (represents any number of characters) and the underscore `_` (represents exactly one character).



### Organization and Formatting Tools

* **`ORDER BY`**: Sorts results in ascending (`ASC`) or descending (`DESC`) order, and multiple columns can be used to break ties.


* **`DISTINCT`**: Cleans up results by removing duplicate data; when applied to multiple columns, it evaluates duplication based on the unique combination of the entire row.


* **`AS` (Column Aliases)**: Gives a column a temporary, readable name in the query result; quotes must be used if the alias contains spaces.



---

## Module 3: Advanced Operations and Combining Data

To create real-world reports, you must be able to summarize millions of records and link data distributed across multiple tables.

### Aggregation

* **Aggregate Functions**: Functions like `SUM`, `COUNT`, `AVG`, `MIN`, and `MAX` perform calculations on a group of rows to return a single summarized value.


* **`GROUP BY`**: Used to apply aggregate functions across different categories (for example, calculating the average salary for each department individually).


* **`HAVING`**: Used to filter grouped data *after* aggregation, unlike the `WHERE` clause which filters individual rows *before* aggregation.



### Combining Tables Horizontally (JOINS)

Used to link two tables together to retrieve integrated data based on a common column.

* **`INNER JOIN`**: Returns only the rows that have an exact match in both tables.


* **`LEFT JOIN / RIGHT JOIN`**: Returns all rows from the primary table (left or right) and only the matched data from the other table, placing `NULL` where there is no match.


* **`FULL OUTER JOIN`**: Returns all records from both tables regardless of a match (in MySQL, this is achieved by combining a `LEFT JOIN` and a `RIGHT JOIN` using `UNION`).


* **Self Join**: A technique for linking a table to itself, frequently used for hierarchical data.



### Combining Results Vertically (UNION)

Used to merge the results of two or more queries, provided they have the same number of columns and compatible data types.

* **`UNION`**: Merges the results and automatically removes any duplicate rows.


* **`UNION ALL`**: Merges the results while keeping all duplicate rows, which makes it faster in performance.
