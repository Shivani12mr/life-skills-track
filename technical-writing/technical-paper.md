# Technical Paper: Structured Query Language (SQL)

## Author

Shivani M R

## Overview

Structured Query Language (SQL) is a standard language used to store,
retrieve, manipulate, and manage data stored in relational databases. It
is widely used across multiple database systems such as MySQL,
PostgreSQL, SQL Server, and Oracle.

SQL enables users to perform operations such as inserting data, updating
records, retrieving information, and analyzing large datasets
efficiently.
-------------------------------------------------------------------------
# Understanding SQL: Basics, Joins, and Aggregations

Structured Query Language (SQL) is the standard language for managing
and manipulating relational databases. It allows users to create,
retrieve, update, and delete data efficiently. This report covers the
foundational elements of SQL, how to combine data from multiple tables,
and how to summarize data using aggregations.

------------------------------------------------------------------------

## SQL Basics

SQL operates through simple declarative statements. The most fundamental
operation is retrieving data from a table using the SELECT statement.

-   **SELECT:** Specifies the columns to retrieve.
-   **FROM:** Specifies the table where the data resides.
-   **WHERE:** Filters records based on specific conditions.

### Code Sample: Basic Selection

``` 
-- Selecting specific columns for employees in the 'Sales' department
SELECT first_name, last_name, salary
FROM employees
WHERE department = 'Sales';
```

------------------------------------------------------------------------

## SQL Joins
```
In relational databases, data is often spread across multiple tables to
reduce redundancy. Joins are used to combine rows from two or more
tables based on a related column between them.

-   **INNER JOIN:** Returns records that have matching values in both
    tables.
-   **LEFT JOIN:** Returns all records from the left table and the
    matched records from the right table.
-   **RIGHT JOIN:** Returns all records from the right table and the
    matched records from the left table.

### Code Sample: Inner Join

``` 
-- Combining employee names with their respective department names
SELECT employees.first_name, departments.department_name
FROM employees
INNER JOIN departments ON employees.department_id = departments.department_id;
```

------------------------------------------------------------------------

## SQL Aggregations
```
Aggregations allow you to perform calculations on a set of values to
return a single scalar value. These are essential for data analysis and
reporting.

-   **COUNT():** Returns the number of rows.
-   **SUM():** Returns the total sum of a numeric column.
-   **AVG():** Returns the average value of a numeric column.
-   **GROUP BY:** Groups rows that have the same values into summary
    rows.

### Code Sample: Aggregation with Group By

```  
-- Calculating the total salary expenditure per department
SELECT department_id, SUM(salary) AS total_payroll, COUNT(*) AS employee_count
FROM employees
GROUP BY department_id
HAVING SUM(salary) > 50000;
```

------------------------------------------------------------------------

## References

-   W3Schools SQL Tutorial
-   PostgreSQL Documentation
-   SQL Joins Visual Explanation
-   Technical Communication Guidelines
