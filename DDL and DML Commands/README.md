
### Data Definition Language (DDL)
**Definition**: DDL is a subset of SQL used to define and manage database objects such as tables, indexes, and schemas. DDL statements are used to create, alter, and delete these objects.

**Common Commands**:
- **CREATE**: Creates a new table, view, index, or other database object.
- **ALTER**: Modifies an existing database object, such as adding or dropping a column in a table.
- **DROP**: Deletes a database object.
- **TRUNCATE**: Removes all rows from a table without logging the individual row deletions.

**Example**:
```sql
CREATE TABLE employees (
    emp_id INT PRIMARY KEY,
    name VARCHAR(50),
    department VARCHAR(50)
);

ALTER TABLE employees ADD COLUMN salary DECIMAL(10, 2);

DROP TABLE employees;
```

### Data Manipulation Language (DML)
**Definition**: DML is a subset of SQL used to retrieve, insert, update, and delete data within database tables. DML statements are concerned with manipulating the data itself.

**Common Commands**:
- **SELECT**: Retrieves data from one or more tables.
- **INSERT**: Adds new rows to a table.
- **UPDATE**: Modifies existing rows in a table.
- **DELETE**: Removes existing rows from a table.

**Example**:
```sql
SELECT * FROM employees;

INSERT INTO employees (emp_id, name, department, salary)
VALUES (1, 'John Doe', 'HR', 50000);

UPDATE employees
SET salary = 55000
WHERE emp_id = 1;

DELETE FROM employees
WHERE emp_id = 1;
```
