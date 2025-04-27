# Finals Lab Task 2. Transforming ER Model to Relational Tables
For this task, we are given an ER diagram representing student assignment submissions, which we need to convert into MySQL tables.

Here’s the Query Statements

Fisrt, a command that create a database as the active database, so subsequent SQL operations will be performed within that specific database.
```sql
CREATE DATABASE student_submissions;
SHOW DATABASES;

USE student_submissions;
```
### Student Query Statements
```sql
CREATE TABLE students_tbl (
    username VARCHAR(50) PRIMARY KEY
);

DESCRIBE students_tbl;
```
### Assignment Query Statements
```sql
CREATE TABLE assignments_tbl (
    shortname VARCHAR(50) PRIMARY KEY,
    due_date DATE NOT NULL,
    url VARCHAR(255)
);

DESCRIBE assignments_tbl;
```
### Submission Query Statements
```sql
CREATE TABLE submission_tbl (
    username VARCHAR(50),
    shortname VARCHAR(50),
    version INT,
    submit_date DATE NOT NULL,
    data TEXT,
    PRIMARY KEY (username, shortname, version),
    FOREIGN KEY (username) REFERENCES student_tbl(username)
        ON DELETE CASCADE
        ON UPDATE CASCADE,
    FOREIGN KEY (shortname) REFERENCES assignment_tbl(shortname)
        ON DELETE CASCADE
        ON UPDATE CASCADE
);

DESCRIBE submission_tbl;
```

Here's the screenshot of Table Structure (See screenshots)

### Student table

  
![Sample Output](Images/student2.png)

### Assignment table

  
![Sample Output](Images/assignment3.png)

### Submission table

  
![Sample Output](Images/submission3.png)

Here's the ER Diagram or Relational Schema

![Sample Output](Images/ERD7.png)
