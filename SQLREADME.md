# STRUCTURED QUERY LANGUAGE (SQL) AS A DATA ANALYSIS TOOL

### WHAT CAN SQL DO?
 - Can execute queries against a database
 - Retrieve data from a database
 - Insert records in a database
 - Create views in a database
 - Update records in a database etc

### TYPES OF SQL COMMAND
 1. DDL - Data Definition Language e.g Create, Alter, Drop ,Truncate
 2. DML - Data Manipulation Language  e.g Insert, Delete, Update
 3. DCL - Data Control Language e.g Grant, Revoke
 4. TCL - Transaction Control Language e.g Commit,Roll back
 5. DQL - Data Query Language e.g Select

### DATATYPE
 1. Binary Datatype e.g YES/NO
 2. Numeric Datatype e.g INT, Float, Decimal, Money
 3. String Datatype e.g Varchar, nvarchar
 4. Date Datatype e.g Date, Datetime

### SQL KEYS
- Primary Key-A Unique Identifier
- Foreign Key-A field in one table that uniquely identifies a row of another table thereby creating a relationship

### SQL STATEMENTS
``` SQL 
SELECT * FROM EMPLOYEE
WHERE Staffid= 'AB401'
```
```SQL
SELECT SUM(Salary) AS TOTALSALARY From Salary
```
```SQL
Update Salary
Set Salary= 7056999.000
Where Staffid= 'AB212'
```
```SQL
Select e.staffid,
       e.firstname,
       e.gender,
       e.hiredate,
       e.state_of_origin,
       s.department,
       s.salary,
from employee e
join salary s
On s.staffid=e.staffid
```       



