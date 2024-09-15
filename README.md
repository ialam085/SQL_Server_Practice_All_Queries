# 🔳 Practice All Important Basic SQL Queries ${\color{green}(using\ SQL\ SERVER)}$

# ${\color{red}Click\ the\ links\ below\ to\ navigate\ directly\ to\ the\ Desired\ SQL\ commands}$ 
👉 [CREATE](https://github.com/ialam085/SQL_Server_Practice_All_Queries/blob/main/README.md#-colorbluecreate)     👉 [ALTER](https://github.com/ialam085/SQL_Server_Practice_All_Queries/blob/main/README.md#-colorbluealter)     👉 [DROP](https://github.com/ialam085/SQL_Server_Practice_All_Queries/blob/main/README.md#-colorbluedrop)     👉 [TRUNCATE](https://github.com/ialam085/SQL_Server_Practice_All_Queries/blob/main/README.md#-colorbluetruncate)

🔗 [USE](https://github.com/ialam085/SQL_Server_Practice_All_Queries/blob/main/README.md#-colorblueuse)

🔗 [INSERT](https://github.com/ialam085/SQL_Server_Practice_All_Queries/blob/main/README.md#-colorblueinsert)

🔗 [UPDATE](https://github.com/ialam085/SQL_Server_Practice_All_Queries/blob/main/README.md#-colorblueupdate)

🔗 [DELETE](https://github.com/ialam085/SQL_Server_Practice_All_Queries/blob/main/README.md#-colorbluedelete)

🔗 [SELECT](https://github.com/ialam085/SQL_Server_Practice_All_Queries/blob/main/README.md#-colorblueselec-t)

🔗 [WILDCARDS](https://github.com/ialam085/SQL_Server_Practice_All_Queries/blob/main/README.md#-colorbluewildcards)

🔗 [AGGREGATE FUNCTIONS](https://github.com/ialam085/SQL_Server_Practice_All_Queries/blob/main/README.md#-colorblueaggregate-functions)

🔗 [CLAUSES](https://github.com/ialam085/SQL_Server_Practice_All_Queries/blob/main/README.md#-colorblueclauses)

🔗 [JOINS](https://github.com/ialam085/SQL_Server_Practice_All_Queries/blob/main/README.md#-colorbluejoins)

🔗 [GRANT](https://github.com/ialam085/SQL_Server_Practice_All_Queries/blob/main/README.md#-colorbluegrant)

🔗 [REVOKE](https://github.com/ialam085/SQL_Server_Practice_All_Queries/blob/main/README.md#-colorbluerevoke)

🔗 [COMMIT](https://github.com/ialam085/SQL_Server_Practice_All_Queries/blob/main/README.md#-colorbluecommit)

🔗 [ROLLBACK](https://github.com/ialam085/SQL_Server_Practice_All_Queries/blob/main/README.md#-colorbluerollback)

🔗 [SAVEPOINT](https://github.com/ialam085/SQL_Server_Practice_All_Queries/blob/main/README.md#-colorbluesavepoint)

🔗 [SET TRANSACTION](https://github.com/ialam085/SQL_Server_Practice_All_Queries/blob/main/README.md#-colorblueset-transaction)

## ◻️ Objective

- The objective of the SQL report is to understand all the **Basic SQL-Server Queries** as well as all kind of **String Functions**.

## ◻️ Tech Stack

- SQL Server

## ◻️ Steps includes

- Creating a Database `FSA`
- Creating two Tables `Student` and `Exams`
- Applying all categories of SQL Commands
     
   - **DDL**: Defines Database structures.
 
   - **SCL**: Manages the Database Session.
 
   - **DML**: Manipulates Data.
 
   - **DQL**: Queries and Retrieves data.

   - **DCL**: Manages access Permissions.

   - **TCL**: Controls Transactions.
 
   - **SFL**: Manipulate and Transform String Data.

## ◻️ Categories of applied SQL Commands
```diff

- DDL (Data Definition Language): DDL changes the structure of the table like creating a table, deleting a table, altering a table, etc. All the command of DDL are auto-committed that means it permanently save all the changes in the database.

+ CREATE [Define DATA TYPES here]
+ ALTER (Rename)
+ DROP
+ TRUNCATE

- SCL (Session Control Language): SCL is used to select a specific database to work with in a session.

+ USE

- DML (Data Manipulation Language): DML commands are used to modify the database. The command of DML is not auto-committed that means it can't permanently save all the changes in the database. They can be rollback.

+ INSERT
+ UPDATE [mostly OPERATORS used here]
+ DELETE

- DQL (Data Query Language): DQL is used to fetch the data from the database.

+ SELECT
+ AGGREGATE functions [SUM(), COUNT(), AVG(), MIN(), MAX()]
+ CLAUSES [where, group by, having, order by, limit]
+ JOINS [(inner) join, left join, right join, outer join, self join, cross join]

- DCL (Data Control Language): DCL commands are used to Grant and Revoke (take back) authority from any database user.

+ GRANT
+ REVOKE

- TCL (Transaction Control Language): TCL commands can only use with DML commands like INSERT, DELETE and UPDATE only.

+ BEGIN TRANSACTION
+ COMMIT
+ ROLLBACK
+ SAVEPOINT

- SFL (String Function Language): It is a CONCEPTUAL category. SFL commands are used to manipulate and transform string data.

+ CONCAT()
+ SUBSTRING() / MID()
+ CHAR_LENGTH() / LENGTH()
+ UPPER() / LOWER()
+ TRIM()
+ REPLACE() / STUFF()
+ LEFT() / RIGHT()
+ REVERSE
+ REPLICATE
+ FORMAT
```

## ◻️ Detailed view of all *SQL-Server* Commands with `Queries` and `Examples`

![image](https://github.com/user-attachments/assets/954153d9-17e8-420c-b9cc-825ddc07c1da)

![image](https://github.com/user-attachments/assets/b47f47f7-2f58-4be3-89cb-b544bf52b9b6)


# 📗 DDL (_Data Definition Language_)

🔗 [Home](https://github.com/ialam085/SQL_Server_Practice_All_Queries/blob/main/README.md#-practice-all-important-basic-sql-queries-colorgreenusing-sql-server)
## 🔘 ${\color{blue}CREATE}$
```diff
+ It is used to Create new Databases, Tables, Constraints, Views, Indexes.
```
### 🔸 Create a new `DATABASE` named 'FSA'
```sql
      CREATE DATABASE FSA;
```
### 🔸 Create a new `TABLE` named 'STUDENT'
```sql
      CREATE TABLE STUDENT (
      Adm_No VARCHAR(20) PRIMARY KEY,
      DOJ DATE,
      Stud_Name VARCHAR(50),
      Gender CHAR(10),
      Guardian_Name VARCHAR(50),
      Address VARCHAR(150),
      Contact_Number BIGINT,
      Class INT,
      Fee DECIMAL(10, 2)
      );
```
### 🔸 Create the Table Student with `CONSTRAINTS` (inline)
- **SQL `CONSTRAINTS` are used to specify `rules` for the data in a table. Constraints are used to `limit` the type of data that can go into a table.**
```sql
      CREATE TABLE STUDENT (
      Adm_No VARCHAR(10) PRIMARY KEY,                    -- Primary key constraint on Admission number
      DOJ DATE NOT NULL,                                 -- Date of Joining, NOT NULL constraint
      Stud_Name VARCHAR(50) NOT NULL,                    -- Student Name, NOT NULL constraint
      Gender CHAR(1) CHECK (Gender IN ('M', 'F')),       -- CHECK constraint ensuring Gender is either 'M' or 'F'
      Guardian_Name VARCHAR(50) NOT NULL,                -- Guardian Name, NOT NULL constraint
      Address VARCHAR(100),                              -- Address
      Contact_Number VARCHAR(15),                        -- Contact Number
      Class INT CHECK (Class BETWEEN 1 AND 12),          -- CHECK constraint ensuring Class is between 1 and 12
      Fee DECIMAL(10, 2) CHECK (Fee > 0)                 -- CHECK constraint ensuring Fee is positive
      );
```
### 🔸 Create a `VIEW` named `Class10_Students`
- **SQL `VIEWS` are simplified data access, minimize the Query. It is also known as `Virtual Table` or `Query Table` because it does not store the rows and columns on the disk. It can lead to performance issues because it is not actual table**
```sql
      CREATE VIEW Class10_Students AS
      SELECT Adm_No, Stud_Name, Gender, Guardian_Name, Contact_Number, Fee
      FROM STUDENT
      WHERE Class = 10;
```
- **Query to check the `VIEWS` in a Table**
```sql
      SELECT * FROM Class10_Students;
```
### 🔸 Create an `INDEX` `idx_StudName`
- **An Index in SQL is like a table of contents in a book. It helps SQL Server quickly locate and retrieve the data from a table without having to scan the entire table.**
```sql
      CREATE INDEX idx_StudName
      ON STUDENT (Stud_Name);
```
- **Query to check the `INDEXES` in a Table**
```sql
      EXEC sp_helpindex 'STUDENT';
```
![image](https://github.com/user-attachments/assets/7b6a57fc-0b20-4b4e-b912-d84ee18f6013)

- **Without an Index (_Left side_)**: SQL Server `searches the whole table` (**slow**).
- **With an Index (_Right side_)**: SQL Server `jumps directly to the rows` you're looking for (**fast**).


## 🔘 ${\color{blue}ALTER}$
```diff
+ It is used to Alter (change) the structure of the Table and the name of the Database.
```
### 🔹 Alter a `DATABASE` _FSA_ to 'FSA_new'
```sql 
      ALTER DATABASE FSA
      Modify Name = FSA_new;
```
### 🔹 Rename a `Table` _STUDENTS_ to 'STUDENT'
```sql      
      EXEC sp_rename 'Students', 'Student';
```
### 🔹 Rename a Table `Column` _Contact_No_ to 'Contact_Number'
```sql      
      EXEC sp_rename 'student.Contact_No', 'Contact_Number';
```
### 🔹 Add a new `column` 'Email' to table _Student_
```sql      
      ALTER TABLE STUDENT
      ADD Email VARCHAR(100);
```
### 🔹 Modify a `column (change data type)` _BIGINT_ to 'VARCHAR' for `Contact_Number` column
```sql      
      ALTER TABLE STUDENT
      ALTER COLUMN Contact_Number VARCHAR(20);
```
### 🔹 Modify a `column (change length of data type)` _VARCHAR(50)_ to 'VARCHAR(100)' for `Stud_Name` column
```sql      
      ALTER TABLE STUDENT
      ALTER COLUMN Stud_Name VARCHAR(100);
```
### 🔹 Drop a column 'Email' from table _Student_
```sql      
      ALTER TABLE STUDENT
      DROP COLUMN Email;
```
### 🔹 Add a default value of `300` to 'Fee' column
```sql      
      ALTER TABLE STUDENT
      ADD CONSTRAINT DF_Fee DEFAULT 300 FOR Fee;
```

## 🔘 ${\color{blue}DROP}$
```diff
+ It is used to Delete/Remove the objects from the Database completely.
```
### 🔸 Drop the `Database` 'FSA'
```sql      
      DROP DATABASE FSA;
```
### 🔸 Drop the `Table` 'Student'
```sql      
      DROP TABLE STUDENT;
```
### 🔸 Drop an `Index` 'idx_StudName'
```sql      
      DROP INDEX idx_StudName ON STUDENT;
```

## 🔘 ${\color{blue}TRUNCATE}$
```diff
+ It is used to Remove/Delete all records (rows) from a table, but the table structure (Column names/headings) remains.
```
### 🔹 Truncate the `Table` 'Student'
```sql      
      TRUNCATE TABLE STUDENT;
```

# 📗 SCL (_Session Control Language_)

## 🔘 ${\color{blue}USE}$
```diff
+ It is used to select a specific Database to work with in a session.
```
### 🔸 Using an Existing `DATABASE` named 'FSA'
```sql      
      USE FSA;
```

# 📗 DML (_Data Manipulation Language_)

## 🔘 ${\color{blue}INSERT}$
```diff
+ It is used to Add new data/values into a table.
```
- **'Column names' `must match the order` of the values.**
- **'Dates' should be provided in `YYYY-MM-DD` format.**
- **The 'Adm_No' is the `primary key` and must be `unique` for each row.**
  
### 🔹 Insert Data/Values (_single record_) into a Table `Student`
```sql      
      INSERT INTO STUDENT (Adm_No, DOJ, Stud_Name, Gender, Guardian_Name, Address, Contact_Number, Class, Fee)
      VALUES ('ROSE00023', '2021-10-01', 'Abu Talha', 'M', 'Md Fareed', 'Khiripaghar', '7903077297', 10, 400);
```
### 🔹 Insert Data/Values (_Multiple records_) into a Table `Student`
```sql      
      INSERT INTO STUDENT (Adm_No, DOJ, Stud_Name, Gender, Guardian_Name, Address, Contact_Number, Class, Fee)
      VALUES 
      ('ROSE00023', '2021-10-01', 'Abu Talha', 'M', 'Md Fareed', 'Khiripaghar', '7903077297', 10, 400),
      ('ROSE00024', '2021-10-01', 'Abu Salesh', 'M', 'Md Fareed', 'Khiripaghar', '7903077297', 8, 450),
      ('ROSE00040', '2021-10-01', 'Md Neyamul', 'M', 'Md Shamsuddin', 'Gauripur', '9661194838', 7, 350),
      ('ROSE00041', '2021-06-08', 'Ruba Parveen', 'F', 'Md Parwez', 'Khiripaghar', '9693461570', 5, 275),
      ('ROSE00058', '2021-10-02', 'Md Muntazeem', 'M', 'Md Naimuddin', 'Rajapur', '8292149189', 10, 325),
      ('ROSE00102', '2021-10-29', 'Mantasha Khatoon', 'F', 'Hasnain', 'Nayadih', '9709148101', 6, 250),
      ('ROSE00144', '2021-12-01', 'Arju Kumar', 'M', 'Ranjit Kumar Sah', 'Chilmil', '6206863026', 8, 300),
      ('ROSE00145', '2021-12-01', 'Roji Kumari', 'F', 'Ranjit Kumar Sah', 'Chilmil', '6206863026', 7, 300),
      ('ROSE00172', '2021-12-04', 'Md Azfar', 'M', 'Md Mushtaque', 'Maghota', '7631041561', 10, 300),
      ('ROSE00331', '2023-02-03', 'Juveria Khatoon', 'F', 'Saud Alam', 'Chihar', '7330859950', 8, 300);
```

## 🔘 ${\color{blue}UPDATE}$
```diff
+ It is used to Modify existing data/values within a table.
```
- **The `WHERE` clause ensures that only the specified row (e.g., Adm_No = 'ROSE00023') is updated.**
- **Without `WHERE`, all rows in the table would be updated!**
  
### 🔸 Update (SET) `Single value/row` (_Class_) in a Table 'Student'
```sql     
     UPDATE STUDENT
     SET Class = 9
     WHERE Adm_No = 'ROSE00040';
```
### 🔸 Update (SET) `Multiple (same) values/same Column` (_Gender_) in a Table 'Student' if Column has NULL values
```sql     
     UPDATE STUDENT
     SET Gender = 'M'
     Where Gender IS NULL;
```
### 🔸 Update (SET) `Multiple (different) values/same row` (_Stud_Name, Fee and DOJ_) in a Table 'Student'
```sql     
     UPDATE STUDENT
     SET Stud_Name = 'Abu Talha Khan', Fee = 450, DOJ = '2021-10-04'
     WHERE Adm_No = 'ROSE00023';
```
### 🔸 Update (SET) `Multiple (same) values/same Column` (_Gender_) in a Table 'Student'
```sql     
     UPDATE STUDENT
     SET Gender = 'Fem'
     WHERE Adm_No IN ('ROSE00145', 'ROSE00331', 'ROSE00041');
```
### 🔸 Update (SET with CASE, ELSE, END) `Multiple (different) values/different Column` (_FEE_) in a Table 'Student'
- **for `ELSE` statement when we keep the same column name (i.e. "Fee") as `SET` statement, then Rest columns `value remain same`**
```sql
        UPDATE STUDENT
           SET Fee = CASE
               WHEN Adm_No='ROSE00024' THEN 450
               WHEN Adm_No='ROSE00041' THEN 275
               WHEN Adm_No='ROSE00058' THEN 325
               WHEN Adm_No='ROSE00102' THEN 250
               WHEN Adm_No='ROSE00023' THEN 400
               WHEN Adm_No='ROSE00040' THEN 350
           ELSE Fee                                       -- for ELSE statement when we keep the same column name (i.e. "Fee") as SET statement, then Rest columns value remain same
        END;
```
### 🔸 Update (SET with CASE, ELSE, END) `Multiple (different) values/different Column` (_FEE_) in a Table 'Student'
- **for `ELSE` statement when we keep any value (i.e. "199") different from `SET` statement, then Rest columns take the `default value "199"`**
```sql
        UPDATE STUDENT
           SET Fee = CASE
               WHEN Adm_No='ROSE00024' THEN 450
               WHEN Adm_No='ROSE00041' THEN 275
               WHEN Adm_No='ROSE00058' THEN 325
               WHEN Adm_No='ROSE00102' THEN 250
               WHEN Adm_No='ROSE00023' THEN 400
               WHEN Adm_No='ROSE00040' THEN 350
           ELSE 199                                       -- for ELSE statement when we keep any value (i.e. "199") different from SET statement, then Rest columns take the default value "199"
        END;
```

## 🔘 ${\color{blue}DELETE}$
```diff
+ It is used to Remove data from a table.
```
- **WHERE clause specifies which rows to delete (e.g., rows with Adm_No = 'ROSE00023').**
- **If you omit the WHERE clause, all rows in the table will be deleted!**

### 🔹 Delete single Row/Record from a Table `Student` by the reference of one `Primary-Key` Value
```sql      
      DELETE FROM STUDENT
      WHERE Adm_No = 'ROSE00023';                         -- One Primary-Key Value
```
### 🔹 Delete Multiple Rows/Records from a Table `Student` by the reference of many `Primary-Key` Values
- **The `IN` operator allows you to match multiple values in a column.**
- **This query will delete `Both rows` where Adm_No is either 'ROSE00023' or 'ROSE00024'.**
```sql  
      DELETE FROM STUDENT
      WHERE Adm_No IN ('ROSE00023', 'ROSE00024');         -- Multiple Primary-Key Values by using "IN" operator
```
### 🔹 Delete Multiple Rows/Records from a Table `Student` by the reference of one `Non-Key` Value
```sql      
      DELETE FROM STUDENT
      WHERE Class = 10;                                   -- One Non-Key Value
```


# 📗 DQL (_Data Query Language_)

## 🔘 ${\color{blue}SELEC T}$
```diff
+ It is used to Retrieve/Fetch data from one or more tables.
```
  
### 🔸 Select Current `Date and Time`
```sql
      SELECT Getdate() AS [Current Date and Time];             -- To check Current DATE and TIME
```
```sql
      SELECT Sysdatetime() AS [Current Date and Time];         -- To check Current DATE and TIME
```
```sql      
      SELECT Cast(Getdate() AS Date) AS [Current Date];        -- To check Current DATE only
```
```sql      
      SELECT Cast(Sysdatetime() AS Date) AS [Current Date];    -- To check Current DATE only
```
### 🔸 Select `All Databases` of SQL-Server
```sql      
      SELECT * FROM sys.databases;
```
### 🔸 Select `All Tables` from a current session Database
```sql      
      SELECT * FROM sys.tables;
```
### 🔸 Select `All Columns` from a Table 'Student'
```sql      
      SELECT * FROM STUDENT;
```
### 🔸 Select `All Columns` from a Table 'Exams'
```sql      
      SELECT * FROM EXAMS;
```
### 🔸 Select `Specific Columns` from a Table 'Student'
```sql      
      SELECT Adm_No, Stud_Name, Class, Fee 
      FROM EXAMS;
```
### 🔸 Select Records with a `Condition` (`Comparison Operators`: =, >, <, >=, <=, !=, <>)
```sql      
      SELECT * FROM STUDENT
      WHERE Class = 10;                     -- Return all records from STUDENT Table for 10th Class
```
```sql
      SELECT * FROM STUDENT
      WHERE Class <> 5;                     -- Return all records from STUDENT Table for all classes EXCEPT 5th Class [Class not equal to (<> or !=) 5]
```
```sql
      SELECT * FROM STUDENT
      WHERE Fee >= 350;                     -- Return all records from STUDENT Table for those whose Fee more than or equal to 350
```
### 🔸 Select Records with `Multiple Conditions` (`Logical Operators`: AND, OR, NOT, IN, BETWEEN, LIKE)
```sql      
      SELECT * FROM STUDENT
      WHERE Fee > 300 AND Class = 8;        -- Return all records from STUDENT Table for 8th Class whose Fee more than 300
```
```sql
      SELECT * FROM STUDENT
      WHERE Class = 10 OR Class = 9;         -- Return all records from STUDENT Table for 8th Class whose Fee more than 300
```
```sql
      SELECT * FROM STUDENT
      WHERE NOT Fee > 350 AND Gender = 'F';   -- Return all records from STUDENT Table whose fee not more than 350 for Females
```
```sql
      SELECT * FROM STUDENT
      WHERE DOJ BETWEEN '2021-10-01' AND '2021-12-04';                 -- Return all records from STUDENT Table who joined between date range
```
```sql
      SELECT * FROM STUDENT
      WHERE Stud_Name LIKE 'Ru%' OR Stud_Name LIKE '%oon';             -- Used 'WILDCARD %' here
```
```sql
      SELECT * FROM EXAMS
      WHERE Subject_Name IN('Science', 'English', 'Computer') AND Marks_Obtained > 90;    -- Return all records from EXAMS Table who get marks above 90 in Science, English and Computer
```

### 🔸 Select Records with `NESTED Queries/SUBqueries`
```sql      
      SELECT * FROM EXAMS
      WHERE Marks_Obtained > (SELECT AVG(Marks_Obtained) FROM EXAMS);        -- Return all records greater than average marks
```
### 🔸 Select Records with `Order/Sorting` (ASC or DESC)
```sql      
      SELECT * FROM STUDENT
      ORDER BY Stud_Name ASC;
```
```sql
      SELECT * FROM STUDENT
      ORDER BY Class DESC;
```

## 🔘 ${\color{blue}WILDCARDS}$
```diff
+ It is used to search for patterns with LIKE clause within string data.
```

### 🔹 Select Records with `Wildcard %`
```sql      
      SELECT * FROM STUDENT
      WHERE Guardian_Name LIKE 'M%';        -- Return all records from STUDENT Table where Guardian Name STARTS with letter 'M'
```
```sql
      SELECT * FROM EXAMS
      WHERE Subject_Name LIKE '%e';         -- Return all records from EXAMS Table where Subject Name ENDS with letter 'e'
```
```sql
      SELECT * FROM EXAMS
      WHERE Subject_Name LIKE 'M%s';        -- Return all records from EXAMS Table where Subject name STARTS with letter 'M' and ENDS with letter 's'
```
```sql
      SELECT * FROM EXAMS
      WHERE Addres LIKE '%ur%';             -- Return all records from EXAMS Table where Addres CONTAINS phrase 'ur'
```

### 🔹 Select Records with `Wildcard _`
```sql      
      SELECT * FROM STUDENT
      WHERE Addres LIKE '_hilmil';           -- Return all records from STUDENT Table where Addres STARTS with ANY ONE character, FOLLOWED "hilmil"
```
```sql
      SELECT * FROM EXAMS
      WHERE Subject_Name LIKE 'Englis_';     -- Return all records from EXAMS Table where subject name STARTS with "Englis", ENDS with ANY ONE character
```
```sql
      SELECT * FROM EXAMS                    -- Return all records from EXAMS Table where subject name STARTS with ANY 2 characters....
      WHERE Subject_Name LIKE '__gl___';     -- FOLLOWED by "gl" and ENDS with ANY 3 characters
```
```sql
      SELECT * FROM EXAMS                    -- Return all records from EXAMS Table where subject code starts with "S"....
      WHERE Subject_Code LIKE 'S__002';      -- followed by any 2 characters and ends with '002'
```
```sql
      SELECT * FROM STUDENT
      WHERE Addres LIKE '_a%';               -- Return all records from STUDENT Table where addres starts with any one character, 'a' at 2nd position
```

### 🔹 Select Records with `Wildcard []`
```sql      
      SELECT * FROM STUDENT
      WHERE Addres LIKE '[a-g]%';            -- Return all records from STUDENT Table where Addres starts with any one letter "from 'a' to 'g'" (a,b,c,d,e,f OR g)
```
```sql
      SELECT * FROM STUDENT
      WHERE Stud_Name LIKE 'A[nr]%'          -- Matches names starting with "An" or "Ar"
```
```sql
      SELECT * FROM STUDENT
      WHERE Guardian_Name LIKE '[rhs]%';    -- Return all records from STUDENT Table where Guardian Name STARTS with letter 'r' or 'h' or 's'
```
```sql
      SELECT * FROM STUDENT
      WHERE Guardian_Name LIKE '[^rhs]%';    -- Return all records from STUDENT Table where Guardian Name NOT STARTS with letter 'r' or 'h' or 's'
```

## 🔘 ${\color{blue}AGGREGATE\ FUNCTIONS}$
```diff
+ It is used to perform a calculation on multiple rows and returns a single value. It is commonly used to summarize or analyze data.
```

### 🔸 Select Records using `COUNT`
```sql      
      SELECT COUNT(*) AS TotalStudents
      FROM STUDENT;                          -- Count the total number of records/rows from student table
```
### 🔸 Select Records using `SUM`
```sql      
      SELECT SUM(Fee) AS TotalFees
      FROM STUDENT;                          -- Calculate the total fees of all students from student table
```
### 🔸 Select Records using `AVG`
```sql      
      SELECT AVG(Fee) AS AverageFee
      FROM STUDENT;                          -- Calculate the average fee of students from student table
```
### 🔸 Select Records using `MIN`
```sql      
      SELECT MIN(Fee) AS MinimumFee
      FROM STUDENT;                          -- Find the minimum fee paid by a student from student table
```
### 🔸 Select Records using `MAX`
```sql      
      SELECT MAX(Fee) AS MinimumFee
      FROM STUDENT;                          -- Find the maximum fee paid by a student from student table
```
### 🔸 Select Records using `COUNT` with GROUP BY and HAVING clauses
```sql      
      SELECT Class, COUNT(*) AS NumberOfStudents
      FROM STUDENT
      GROUP BY Class
      HAVING COUNT(*) > 2;                   -- Find classes with more than 2 students
```

## 🔘 ${\color{blue}CLAUSES}$
```diff
+ It is used to specify conditions or actions to be applied to the data. Clauses help to filter, group, sort, or limit the results of a query.
```

### 🔹 Select Records using `WHERE`
- **`WHERE` clause: `Filter rows` based on a condition before grouping.**
```sql
       SELECT * FROM STUDENT
       WHERE Class = 8;                                      -- Retrieve all students in Class 8
```
### 🔹 Select Records using `ORDER BY`
- **`ORDER BY` clause: `Sort` the result set.**
```sql
       SELECT * FROM STUDENT
       ORDER BY Stud_Name ASC;                               -- Retrieve all students sorted by Stud_Name in ascending order
```
```sql
       SELECT * FROM STUDENT
       WHERE Gender = 'M'
       ORDER BY Stud_Name ASC;                               -- Retrieve all male students sorted by Stud_Name in ascending order
```

### 🔹 Select Records using `GROUP BY`
- **`GROUP BY` clause: `Group rows` based on one or more columns.**
```sql
       SELECT Class, SUM(Fee) AS [Total Fee by Class]
       FROM STUDENT
       GROUP BY Class;                                       -- Sum the fee of students in each class
```
```sql
       SELECT Class, SUM(Fee) AS [Total Fee by Class]
       FROM STUDENT
       WHERE Fee > 300                                       -- Filters rows where Fee is greater than 300
       GROUP BY Class
       ORDER BY Class DESC;                                  -- Sum the fee of students in each class whose fee more than 300 sorted by Class in Descending order
```

### 🔹 Select Records using `HAVING`
- **`HAVING` clause: `Filter groups` after Grouping to filter results on Aggregation.**
```sql
       SELECT Class, COUNT(*) AS NumberOfStudents
       FROM STUDENT
       GROUP BY Class
       HAVING COUNT(*) > 2;                                  -- Find classes with more than 2 students
```
```sql
       SELECT Class, SUM(Fee) AS [Total Fee by Class]
       FROM STUDENT
       GROUP BY Class
       HAVING SUM(Fee) > 500                                 -- Filters groups where the total Fee is greater than 500
       ORDER BY Class DESC;
```

### 🔹 Select Records using `LIMIT/TOP`
- **`TOP` clause: `Limit` the number of rows returned.**
```sql
       SELECT TOP 5 * FROM STUDENT
       ORDER BY Fee DESC;                                    -- Retrieve the top 5 students by Fee in descending order
```
```sql
       SELECT TOP 5 Adm_No, Stud_Name FROM STUDENT
       ORDER BY Fee DESC;                                    -- Retrieve the top 5 students table Adm_No and Stud_Name columns by Fee in descending order
```

### 🔹 Select Records using `DISTINCT`
- **`DISTINCT` clause: Select `unique` values only.**
```sql
       SELECT DISTINCT Class FROM STUDENT;                   -- Retrieve the distinct classes of students
```
```sql
       SELECT DISTINCT Class FROM STUDENT
       WHERE Fee > 300;                                      -- Retrieve the distinct classes of students where student fee more than 300
```

### 🔹 Select Records using `JOIN`
- **`JOIN` clause: Combines rows from two or more tables.**
```sql
       SELECT S.*, E.Subject_Name, E.Marks_Obtained          -- Fetch all columns (*) from Student Table and Subject & Marks obtained from Exams Table
       FROM STUDENT S
       INNER JOIN EXAMS E
       ON S.Adm_No = E.Adm_No;
```

## 🔘 ${\color{blue}JOINS}$
```diff
+ It is used to combine rows from two or more tables, based on a related column between them.
```

### 🔸 Fetch Student Records using `INNER JOIN`
- **`(INNER) JOIN`: Returns records that have MATCHING VALUES IN BOTH TABLES.**
```sql
      SELECT S.Stud_Name, E.Subject_Name, E.Marks_Obtained
      FROM STUDENT S
      INNER JOIN EXAMS E
      ON S.Adm_No = E.Adm_No;                             -- Returns the student names along with the subjects and marks they obtained in the exams
```
```sql
      SELECT S.Stud_Name, E.Subject_Name, E.Marks_Obtained
      FROM STUDENT S
      INNER JOIN EXAMS E
      ON S.Adm_No = E.Adm_No
      WHERE S.Class = 10;                                 -- Returns the students of class 10 and their respective exam marks
```
```sql
      SELECT S.Stud_Name, E.Subject_Name, E.Marks_Obtained
      FROM STUDENT S
      INNER JOIN EXAMS E
      ON S.Adm_No = E.Adm_No
      WHERE E.Marks_Obtained > 85;                        -- Fetches students who scored more than 85 marks in any exam
```

### 🔸 Fetch Student Records using `LEFT JOIN`
- **`LEFT (OUTER) JOIN`: Returns all records from the LEFT TABLE, and the matched records from the RIGHT TABLE.**
```sql
      SELECT S.Stud_Name, E.Subject_Name, E.Marks_Obtained
      FROM STUDENT S
      LEFT JOIN EXAMS E
      ON S.Adm_No = E.Adm_No;           -- Fetches all students, including those who may not have appeared in any exams
```

### 🔸 Fetch Student Records using `RIGHT JOIN`
- **`RIGHT (OUTER) JOIN`: Returns all records from the RIGHT TABLE, and the matched records from the LEFT TABLE.**
```sql
      SELECT S.Stud_Name, E.Subject_Name, E.Marks_Obtained
      FROM STUDENT S
      RIGHT JOIN EXAMS E
      ON S.Adm_No = E.Adm_No;           -- Fetches all exam records, even if some students may not exist in the STUDENT table (Null Values for Marks_Obtained)
```

### 🔸 Fetch Student Records using `OUTER JOIN`
- **`FULL (OUTER) JOIN`: Returns all records when there is a match in either LEFT or RIGHT TABLE.**
```sql
      SELECT S.Stud_Name, E.Subject_Name, E.Marks_Obtained
      FROM STUDENT S
      OUTER JOIN EXAMS E
      ON S.Adm_No = E.Adm_No;           -- Fetches all exam records, even if some students may not exist in the STUDENT table (Null Values)
```

### 🔸 Fetch Student Records using `SELF JOIN`
- **`SELF JOIN`: A self join is when a table is joined with itself. It is useful for hierarchical or recursive data structures. Let's say we want to find students from the same address (students who live in the same location).**
```sql
      SELECT S1.Stud_Name AS Student1, S2.Stud_Name AS Student2, S1.Addres
      FROM STUDENT S1
      INNER JOIN STUDENT S2
      ON S1.Addres = S2.Addres
      WHERE S1.Adm_No <> S2.Adm_No;    -- This query matches students who live at the same address but ensures they are not the same student by using S1.Adm_No <> S2.Adm_No
```
  
### 🔸 Fetch Student Records using `CROSS JOIN`
- **`CROSS JOIN`: It combines every row of the first table with every row of the second table. `Example`: Cross join students with their subjects.**
```sql
      SELECT S.Stud_Name, E.Subject_Name
      FROM STUDENT S
      CROSS JOIN EXAMS E;              -- Pairs every student with every subject, producing a large set of combinations
```

### 🔸 Fetch Student Records using `UNION`
- **`UNION`: It Combines the results of two or more SELECT statements. The UNION operator only returns distinct records.**
```sql
      SELECT Adm_No FROM STUDENT
      UNION
      SELECT Guardian_Name FROM STUDENT;
```

# 📗 DCL (_Data Control Language_)

## 🔘 ${\color{blue}GRANT}$
```diff
+ It is used to give a user access rights to the database.
```
  
### 🔹 Grant `SELECT` Permission on a Table
```sql      
      GRANT SELECT ON STUDENT TO UserA;                      -- Gives the user 'UserA' the ability to perform SELECT queries on the STUDENT table
```

### 🔹 Grant `INSERT` and `UPDATE` Permissions on a Table
```sql      
      GRANT INSERT, UPDATE ON STUDENT TO UserA;              -- Allows UserA to insert new records and update existing ones in the STUDENT table
```

## 🔘 ${\color{blue}REVOKE}$
```diff
+ It is used to remove access rights from the database which is granted to a user.
```

### 🔸 Revoke `SELECT` Permission on a Table
```sql      
      REVOKE SELECT ON STUDENT TO UserA;                      -- Removes the SELECT permission, so UserA can no longer query data from the STUDENT table
```

### 🔸 Revoke `INSERT` and `UPDATE` Permissions on a Table
```sql      
      REVOKE INSERT, UPDATE ON STUDENT TO UserA;              -- Removes the ability for UserA to insert new records or update existing ones in the STUDENT table
```

# 📗 TCL (_Transaction Control Language_)

## 🔘 ${\color{blue}COMMIT}$
```diff
+ It is used to save the current transaction permanently in the database. Once a COMMIT is executed, the changes are made permanent and cannot be rolled back.
```
  
### 🔹 Insert a Record and `Commit` the Transaction
```sql      
      BEGIN TRANSACTION;

      INSERT INTO STUDENT (Adm_No, DOJ, Stud_Name, Gender, Guardian_Name, Address, Contact_Number, Class, Fee)
      VALUES ('ROSE00332', '2023-09-15', 'John Doe', 'M', 'Richard Doe', 'Greenfield', '1234567890', 8, 350);

      COMMIT;
```

## 🔘 ${\color{blue}ROLLBACK}$
```diff
+ It is used to Undo changes made in the current transaction.
```
  
### 🔸 Insert a Record, but `Rollback` the Transaction
```sql      
      BEGIN TRANSACTION;

      INSERT INTO STUDENT (Adm_No, DOJ, Stud_Name, Gender, Guardian_Name, Address, Contact_Number, Class, Fee)
      VALUES ('ROSE00333', '2023-09-15', 'Jane Smith', 'F', 'John Smith', 'Blueville', '9876543210', 7, 300);

      ROLLBACK;                                                                      -- If something goes wrong, rollback the transaction
```

## 🔘 ${\color{blue}SAVEPOINT}$
```diff
+ It is used to set a point within a transaction to which you can roll back later.
```
  
### 🔹 Using `SAVEPOINT` in a Transaction
```sql      
      BEGIN TRANSACTION;

      INSERT INTO STUDENT (Adm_No, DOJ, Stud_Name, Gender, Guardian_Name, Address, Contact_Number, Class, Fee)
      VALUES ('ROSE00334', '2023-09-15', 'Alice Brown', 'F', 'Sam Brown', 'Redtown', '1122334455', 6, 250);

      SAVEPOINT Save1;

      INSERT INTO STUDENT (Adm_No, DOJ, Stud_Name, Gender, Guardian_Name, Address, Contact_Number, Class, Fee)
      VALUES ('ROSE00335', '2023-09-15', 'Bob White', 'M', 'Jim White', 'Greenville', '5566778899', 5, 275);

      ROLLBACK TRANSACTION Save1;                                                  -- Something goes wrong, rollback to the savepoint

      COMMIT;                                                                      -- Now commit the first insert, but not the second
```

## 🔘 ${\color{blue}SET\ TRANSACTION}$
```diff
+ It is used to specify characteristics for the transaction (e.g., isolation level).
```
  
### 🔸 Using `SET TRANSACTION ISOLATION LEVEL`
```sql      
      SET TRANSACTION ISOLATION LEVEL READ COMMITTED;

      BEGIN TRANSACTION;
                                                                                           -- Query or Insert/Update/Delete operations                                                      

      INSERT INTO STUDENT (Adm_No, DOJ, Stud_Name, Gender, Guardian_Name, Address, Contact_Number, Class, Fee)
      VALUES ('ROSE00336', '2023-09-15', 'Charlie Green', 'M', 'Paul Green', 'Bluefield', '9988776655', 9, 400);

      COMMIT;
```
