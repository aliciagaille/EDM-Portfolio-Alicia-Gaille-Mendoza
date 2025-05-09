# Finals Lab Task 3.1: Using SELECT CLAUSE
For this task, we are given initial query then perform the SELECT statements required for each problems. To use a SELECT clause in order to specify the names of the fields that have data that want to use in a query. 

## Here’s the Query Statements

Fisrt, a command that create a database, so subsequent SQL operations will be performed within that specific database.
```sql
CREATE DATABASE online_courses;
SHOW DATABASES;

USE online_courses;
```

### TASK 1
```sql
SELECT *
FROM courses_tbl
WHERE students_enrolled < enrollment_limit;
```
### TASK 2
```sql
SELECT category, SUM(students_enrolled) AS total_number_of_students_enrolled
FROM courses_tbl
GROUP BY category;
```

### TASK 3
```sql
SELECT *
FROM courses_tbl
WHERE students_enrolled = enrollment_limit;
```

### TASK 4
```sql
SELECT SUM(students_enrolled) AS total_number_of_students_enrolled
FROM courses_tbl;
```

### TASK 5
```sql
SELECT *
FROM courses_tbl
ORDER BY students_enrolled ASC;
```

## Here's the screenshot of the whole Query Statements and Table Structure (See screenshots)

### TASK 1

![Sample Output](Images/TASK1.png)

### TASK 2

![Sample Output](Images/TASK2.png)

### TASK 3

![Sample Output](Images/TASK3.png)

### TASK 4

![Sample Output](Images/TASK4.png)

### TASK 5

![Sample Output](Images/1TASK5.png)
![Sample Output](Images/2TASK5.png)
