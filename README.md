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

Triggers :  It executes when the DMl command rund(Insert, update, delete) .

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

1 Nf= No duplicate groups
2 Nf= No partial dependency
2 Nf= No transitive dependecy

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




# ACID Properties (Very Important for Interview)
ACID ensures safe and reliable transactions in a database.

1️⃣ Atomicity
👉 All or nothing
If one query fails, the whole transaction fails.
Example:
Money transfer –
If ₹1000 is deducted but not added → transaction fails completely.

2️⃣ Consistency
👉 Database always moves from one valid state to another.
Rules, constraints, and integrity must be maintained.

3️⃣ Isolation
👉 Multiple transactions should not disturb each other.
If two users transfer money at same time, they should not see half-done results.

4️⃣ Durability
👉 Once transaction is committed, it is permanently saved.
Even if system crashes, data remains safe.

🎯 Easy Trick to Remember:
A → All or nothing
C → Correct state
I → Independent transactions
D → Data permanent

# Index Related ... 
1️⃣ What is an Index?
Answer:
“Index is a database object that improves query performance by reducing data search time.”

2️⃣ Why do we use Index?
Answer:
“To speed up SELECT queries, especially on large tables.”

3️⃣ How does Index improve performance?
Answer:
“It avoids full table scan and directly locates required rows using a data structure like B-Tree.”

3️⃣ How does Index improve performance?
Answer:
“It avoids full table scan and directly locates required rows using a data structure like B-Tree.”

5️⃣ Can we create index on multiple columns?
Answer:
“Yes. It is called Composite Index.”


6️⃣ Types of Index in SQL?
Clustered Index
Non-Clustered Index
Composite Index
Unique Index

7️⃣ Difference between Clustered and Non-Clustered Index?
Clustered:
Data physically sorted
Only one per table

Non-Clustered:
Separate structure
Multiple allowed


1️⃣1️⃣ What is Cardinality?
Answer:
“Number of unique values in a column.”
High cardinality → Good for index.

1️⃣2️⃣ What is Index Selectivity?
Answer:
“How efficiently index filters rows.”


Q: Why is my query slow even after creating index?
Possible reasons:
Wrong column indexed
Function used on indexed column
Low selectivity
Not using proper WHERE condition



1️⃣ Clustered Index
✅ Meaning:

Data in table is physically stored in sorted order based on index column.

👉 Table data itself is arranged.

Important Points:

Only one clustered index per table

Usually created automatically on Primary Key

Interview Line:

“Clustered index defines the physical order of data in the table.”


2️⃣ Non-Clustered Index
✅ Meaning:

It creates a separate structure that stores column values + pointer to actual data.

👉 Table data is NOT physically changed.

Important Points:

Multiple non-clustered indexes allowed

Improves SELECT performance

Interview Line:

“Non-clustered index stores indexed values separately with reference to actual table rows.”



3️⃣ Unique Index
✅ Meaning:

Does not allow duplicate values in a column.

👉 Ensures uniqueness.

Example:

Email column.

Interview Line:

“Unique index enforces unique values in indexed column.”


4️⃣ Composite Index
✅ Meaning:

Index created on multiple columns together.

Example:
(first_name, last_name)

Interview Line:

“Composite index improves performance when query filters multiple columns.”

5️⃣ Full-Text Index
✅ Meaning:

Used for searching words inside large text data.

Example:
Searching in description column.

#
“Indexes improve query performance. Clustered index stores data physically sorted and only one is allowed per table. Non-clustered index stores values separately and multiple can be created. We also have unique and composite indexes based on requirements.”
