# SqlTopics
🔥 Most Important SQL Topics (Asked Very Frequently)

SELECT Queries (Basic to Advanced)

JOINS (INNER, LEFT, RIGHT, FULL)

GROUP BY & HAVING

Aggregate Functions (COUNT, SUM, AVG, MIN, MAX)

Subqueries

Window Functions (ROW_NUMBER, RANK, DENSE_RANK)

Indexes

Normalization (1NF, 2NF, 3NF)

Primary Key & Foreign Key

Constraints (NOT NULL, UNIQUE, CHECK, DEFAULT)

Views

Stored Procedures

Triggers

Transactions (ACID properties)

Difference: DELETE vs TRUNCATE vs DROP

Difference: WHERE vs HAVING

Difference: INNER JOIN vs OUTER JOIN

Query Optimization Basics

Self Join

Top N / Nth Highest Salary Problems

////////////////////////////////////////////////////////////////////////////



⚡ Less Important (But Still Useful)

Cursors

Temporary Tables

SQL Injection Basics

Partitioning

Sharding Concept

Execution Plan

Materialized Views

Functions (User Defined Functions)

XML/JSON Handling in SQL

Database Architecture Basics


//////////////////////////////////////////////////////////////

✅ 1️⃣ Order of Writing the Query (Syntax Order)
SELECT
FROM
JOIN
WHERE
GROUP BY
HAVING
ORDER BY
LIMIT
/////////////////////////////////////////////////


🔥 2️⃣ Actual Order of Execution (Very Important for Interviews)

FROM

JOIN

WHERE

GROUP BY

HAVING

SELECT

ORDER BY

LIMIT / OFFSET



//////////////////////////////////////////////// 
#Question  

View:  A view is a virtual table created from a query.
permanently rename table:
ALTER TABLE employees_details
RENAME TO employee_detail;

Temporary Rename use As Alice
SELECT *
FROM employees_details AS employee_detail;

# Window Function (Easy Meaning)
“Window functions perform calculations across rows without grouping them, and RANK assigns ranking based on column values.”
Easy Difference:

ROW_NUMBER() → Always unique number
RANK() → Same rank for same values (skips next)
DENSE_RANK() → Same rank but no skipping

✅ What is RANK() ?
👉 RANK() gives ranking based on a column value.
Example:
If salaries are:
Salary
10000
9000
9000
8000

Using RANK():
Salary	Rank
10000	1
9000	2
9000	2
8000	4


Cursor → row-by-row processing
Temp Table → temporary storage
SQL Injection → security attack
Partitioning → splitting large table
Execution Plan → how database runs query


1Nf  No duplicate groups
2Nf  No partical dependency
3Nf No transetive dependecy. 

