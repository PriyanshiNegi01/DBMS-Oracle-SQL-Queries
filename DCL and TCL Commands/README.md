
### Data Control Language (DCL)
**Definition**: DCL is a subset of SQL used to control access to data in a database. DCL statements are used to grant and revoke permissions and access rights to database objects.

**Common Commands**:
- **GRANT**: Gives a user or role specific privileges.
- **REVOKE**: Removes previously granted privileges from a user or role.

**Example**:
```sql
GRANT SELECT, INSERT ON employees TO user1;

REVOKE INSERT ON employees FROM user1;
```

### Transaction Control Language (TCL)
**Definition**: TCL is a subset of SQL used to manage transactions in a database. Transactions are sequences of one or more SQL operations treated as a single unit. TCL statements control the execution of transactions to ensure data integrity.

**Common Commands**:
- **COMMIT**: Saves all changes made in the current transaction.
- **ROLLBACK**: Undoes all changes made in the current transaction.
- **SAVEPOINT**: Sets a savepoint within a transaction to which a transaction can be partially rolled back.
- **SET TRANSACTION**: Sets transaction properties such as isolation level.

**Example**:
```sql
BEGIN;

INSERT INTO employees (emp_id, name, department, salary)
VALUES (2, 'Jane Smith', 'Finance', 60000);

SAVEPOINT save1;

UPDATE employees
SET salary = 62000
WHERE emp_id = 2;

ROLLBACK TO save1;

COMMIT;
```

- **Explanation**: The `BEGIN` starts a transaction. The `INSERT` statement adds a new employee, and the `SAVEPOINT` creates a point to which the transaction can be rolled back. The `UPDATE` changes the salary, but the `ROLLBACK TO save1` undoes the `UPDATE` without affecting the `INSERT`. Finally, the `COMMIT` saves the changes made by the `INSERT`.
