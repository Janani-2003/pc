# pc
```
List the details of the books whose quantity below 15 and year of publication is below 2015 b) List the details of book whose publication is not equal to W3school c) Arrange the book by Ascending order d) Create List all the books name in decending order of year_of_publication e) Delete the details of the book whose author is dennis. /*Create Table*/CREATE DATABASE  book_store;CREATE TABLE  book(bookid int,  title varchar(50),author varchar(50),publication varchar(50),year int,price int,  qty int);INSERT INTO  book VALUES(101,'Harry Potter','J.K.Rowling','W3School',2010,500,5);INSERT INTO  book VALUES(102,'Summer I Turned Pretty','Jenny Han','W3School',2018,300,18);INSERT INTO  book VALUES(103,'It Ends with Us','Coolen Hoover','JavaTpoint',2012,700,12);INSERT INTO  book VALUES(104,'Phoebe Buffay','dennis','F.R.I.E.N.D.S',2000,1700,2);SELECT * FROM  book;/*Books whose quantity below 15 and year of publication is below 2015*/SELECT * FROM  book WHERE  qty<15 and year<2015;/*Book whose publication is not equal to W3school*/SELECT * FROM  book WHERE  publication!='W3School';/*Arrange the book by Ascending order*/SELECT * FROM  book ORDER BY  title;/*Arrange the book by Descending order - Year*/SELECT * FROM  book ORDER BY year DESC;/*Delete book whose author is dennis*/DELETE FROM  book WHERE  author='dennis';SELECT * FROM  book;DROP TABLE  book;/*Delete Database*/DROP DATABASE  book_store; a) Delete the table b) Delete the database c) Rename the database d) Modify the column price from integer to float in book table. e) Modify the price value & Book title /*Create Table*/CREATE DATABASE  book_store;CREATE TABLE  book(bookid int,  title varchar(50),  price int,  qty int);INSERT INTO  book VALUES(101,'Harry Potter',500,5);INSERT INTO  book VALUES(102,'Summer I Turned Pretty',300,10);INSERT INTO  book VALUES(103,'It Ends with Us',700,3);SELECT * FROM  book;/*Modify price column from int to float*/ALTER TABLE  book ALTER COLUMN  price float;/*Rename Database*/ALTER DATABASE  book_store MODIFY NAME =  bookshop;/*Modify price & book title*/UPDATE  book SET  title = 'Harry Potter: Prisoner of Azkaban' WHERE  bookid=101;UPDATE  book SET  price =  550 WHERE  bookid =  101;SELECT * FROM  book;/*Delete Table*/DROP TABLE  book;/*Delete Database*/DROP DATABASE  bookshop; a) Create an employee table with attributes empid,name,experience,salary,city b) Add age column inside the table c) List the details of the employee whose salary is greater than 50000 d) List the details of the employee whose city is Chennai e) Delete the table /*Create Table*/CREATE TABLE  emp(empid int, name varchar(60),  experience float,  salary float,  city varchar(20));/*Add Entries*/INSERT INTO  emp VALUES(101,'aaa',5.5,55000.0,'Chennai');INSERT INTO  emp VALUES(102,'bbb',10.0,75000.0,'Erode');INSERT INTO  emp VALUES(103,'ccc',0.5,3500.0,'Chennai');SELECT * FROM  emp;/*Add age column*/ALTER TABLE  emp ADD  age int;UPDATE  emp SET  age =  30 WHERE  empid =  101;UPDATE  emp SET  age =  45 WHERE  empid =  102;UPDATE  emp SET  age =  25 WHERE  empid =  103;SELECT * FROM  emp /*List details of emp whose salary > 50000*/SELECT * FROM  emp WHERE  salary>50000;/*List detials of emp whose city in Chennai*/SELECT * FROM  emp WHERE  city='Chennai';DROP TABLE  emp;EMPLOYEES (Employee_Id, First_Name, Last_Name, Email, Phone_Number, Hire_Date, Job_Id, Salary, Commission_Pct, Manager_Id, Department_Id) a) List out the employees who works under manager 100 b) Find the names of the employees who have a salary greater than or equal to 4800 c) List out the employees whose last name is ‘AUSTIN’ d) Find the names of the employees who works in departments 60,70 and 80 e) Display the unique Manager_Id. -- Create the EMPLOYEES tableCREATE TABLE  EMPLOYEES ( Employee_Id INT, First_Name VARCHAR(50), Last_Name VARCHAR(50), Email VARCHAR(100), Phone_Number VARCHAR(20), Hire_Date DATE, Job_Id VARCHAR(20), Salary FLOAT, Commission_Pct FLOAT, Manager_Id INT, Department_Id INT);-- Insert sample values into the EMPLOYEES tableINSERT INTO  EMPLOYEES (Employee_Id,  First_Name,  Last_Name,  Email,  Phone_Number,  Hire_Date,  Job_Id,Salary,  Commission_Pct,  Manager_Id,  Department_Id)VALUES(1, 'John', 'Doe', 'john.doe@example.com', '1234567890', '2022-01-01', 'JOB1',  5000,  0.1,  100,  60),(2, 'Jane', 'Smith', 'jane.smith@example.com', '9876543210', '2022-02-01', 'JOB2',  5500,  0.15,  100,70),(3, 'Mike', 'Johnson', 'mike.johnson@example.com', '5555555555', '2022-03-01', 'JOB3',  6000,  0.2,200,  80),(4, 'Emily', 'Austin', 'emily.austin@example.com', '9999999999', '2022-04-01', 'JOB4',  4800,  0.1,100,  60),(5, 'David', 'Austin', 'david.austin@example.com', '1111111111', '2022-05-01', 'JOB5',  5200,  0.12,200,  70),(6, 'Sarah', 'Williams', 'sarah.williams@example.com', '2222222222', '2022-06-01', 'JOB6',  5300,0.08,  200,  80);-- a) List out the employees who work under manager 100:SELECT * FROM  EMPLOYEES WHERE  Manager_Id =  100;-- b) Find the names of the employees who have a salary greater than or equal to 4800:SELECT  First_Name,  Last_Name FROM  EMPLOYEES WHERE  Salary >=  4800;-- c) List out the employees whose last name is 'AUSTIN':SELECT * FROM  EMPLOYEES WHERE  Last_Name = 'AUSTIN';-- d) Find the names of the employees who work in departments 60, 70, and 80:SELECT  First_Name,  Last_Name FROM  EMPLOYEES WHERE  Department_Id IN (60,  70,  80);-- e) Display the unique Manager_Id:SELECT DISTINCT  Manager_Id FROM  EMPLOYEES;DROP TABLE  EMPLOYEES; 5. Create Client_master with the following fields(ClientNO, Name, Address, City, State, bal_due) (a) Insert five records (b) Find the names of clients whose bal_due> 5000 . (c) Change the bal_due of ClientNO “ C123” to Rs. 5100 (d) Change the name of Client_master to Client12 . (e) Display the bal_due heading as “BALANCE” CREATE TABLE  Client_master ( ClientNO VARCHAR(10),Name VARCHAR(50),Address VARCHAR(100), City VARCHAR(50),State VARCHAR(50), bal_due DECIMAL(10,  2));-- a) INSERT FIVE RECORDSINSERT INTO  Client_master (ClientNO, Name, Address,  City, State,  bal_due)VALUES('C123', 'John Doe', '123 Main St', 'New York', 'NY',  1000),('C124', 'Jane Smith', '456 Elm St', 'Los Angeles', 'CA',  6000),('C125', 'Mike Johnson', '789 Oak St', 'Chicago', 'IL',  2000),('C126', 'Sarah Williams', '321 Pine St', 'Houston', 'TX',  8000),('C127', 'David Brown', '654 Cedar St', 'Miami', 'FL',  3000);SELECT * FROM  Client_master;-- b) Find the names of clients whose bal_due is greater than 5000SELECT NameFROM  Client_master WHERE  bal_due >  5000;-- c) Change the bal_due of ClientNO "C123" to Rs. 5100UPDATE  Client_master SET  bal_due =  5100 WHERE  ClientNO = 'C123';SELECT * FROM  Client_master;-- d) Change the name of the Client_master table to Client12EXEC sp_rename 'Client_master', 'Client12';-- e) Display the bal_due heading as "BALANCE"SELECT  bal_due AS  BALANCE FROM  Client12;DROP TABLE  Client12;6. Create Sales table with the following fields( Sales No, Salesname, Branch, Salesamount, DOB) (a) Insert five records (b) Calculate total salesamount in each branch (c) Calculate average salesamount in each branch . (d) Display all the salesmen, DOB who are born in the month of December as day in character format i.e. 21-Dec-09 (e) Display the name and DOB of salesman in alphabetical order of the month. -- Create the Sales tableCREATE TABLE  Sales ( SalesNo INT, Salesname VARCHAR(50), Branch VARCHAR(50), Salesamount DECIMAL(10,  2), DOB DATE);-- a) Insert five records into the Sales tableINSERT INTO  Sales (SalesNo,  Salesname,  Branch,  Salesamount,  DOB) VALUES(1, 'John Doe', 'Branch A',  1000.00, '1990-05-15'),(2, 'Jane Smith', 'Branch B',  1500.00, '1985-12-10'),(3, 'Mike Johnson', 'Branch A',  2000.00, '1992-02-20'),(4, 'Sarah Williams', 'Branch C',  1800.00, '1991-12-05'),(5, 'David Brown', 'Branch B',  1200.00, '1988-09-30');-- b) Calculate total sales amount in each branchSELECT  Branch, SUM(Salesamount) AS  TotalSalesAmount FROM  Sales GROUP BY  Branch;-- c) Calculate average sales amount in each branchSELECT  Branch, AVG(Salesamount) AS  AverageSalesAmount FROM  Sales GROUP BY  Branch;-- d) Display salesmen and DOB born in December (formatted as "DD-Mon-YY")SELECT  Salesname, CONVERT(VARCHAR(11),  DOB,  106) AS  FormattedDOB FROM  Sales WHERE MONTH(DOB) =  12;-- e) Display the name and DOB of salesmen in alphabetical order of the monthSELECT  Salesname, CONVERT(VARCHAR(11),  DOB,  106) AS  FormattedDOB FROM  Sales ORDER BY MONTH(DOB),  Salesname;-- 106 is the display style dor the given format DROP TABLE  Sales; 7. (EmpNo, EmpName, Job,Basic, DA, HRA,PF, GrossPay, NetPay) (Calculate DA as 30% of Basic and HRA as 40% of Basic) ( a ) Insert Five Records and calculate GrossPay and NetPay. ( b ) Display the employees whose Basic is lowest in each department . ( c ) If NetPay is less than <Rs. 10,000 add Rs. 1200 as special allowances . ( d ) Display the employees whose GrossPay lies between 10,000 & 20,000 ( e ) Display all the employees who earn maximum salary -- Creating the employee tableCREATE TABLE  Employee ( EmpNo INT PRIMARY KEY, EmpName VARCHAR(100), Job VARCHAR(100),Basic DECIMAL(10,  2), DA DECIMAL(10,  2), HRA DECIMAL(10,  2), PF DECIMAL(10,  2), GrossPay DECIMAL(10,  2), NetPay DECIMAL(10,  2));-- Inserting five recordsINSERT INTO  Employee (EmpNo,  EmpName,  Job, Basic)VALUES(1, 'John Doe', 'Manager',  5000),(2, 'Jane Smith', 'Developer',  4000),(3, 'Mike Johnson', 'Analyst',  6000),(4, 'Sarah Davis', 'Designer',  4500),(5, 'Robert Wilson', 'Tester',  5500);-- Updating DA and HRA based on BasicUPDATE  Employee SET  DA = Basic *  0.30, HRA = Basic *  0.40;-- Calculating GrossPay and NetPayUPDATE  Employee SET  GrossPay = Basic +  DA +  HRA, NetPay =  GrossPay -  PF;-- Displaying employees with lowest Basic in each departmentSELECT  E1.*FROM  Employee E1 INNER JOIN (SELECT  Job, MIN(Basic) AS  LowestBasic FROM  Employee GROUP BY  Job )  E2 ON  E1.Job =  E2.Job AND  E1.Basic =  E2.LowestBasic;-- Updating NetPay if less than 10,000UPDATE  Employee SET  NetPay =  NetPay +  1200 WHERE  NetPay <  10000;-- Displaying employees with GrossPay between 10,000 and 20,000SELECT * FROM  Employee WHERE  GrossPay BETWEEN  10000 AND  20000;-- Displaying employees with maximum salarySELECT * FROM  Employee WHERE  GrossPay = (SELECT MAX(GrossPay) FROM  Employee);8. An Enterprise wishes to maintain a database to automate its operations. Enterprise is divided into certain departments and each department consists of employees. The following two tables describes the automation schemas Dept (deptno, dname, loc) Emp (empno, ename, job, mgr, hiredate, sal, comm, deptno) a) Update the employee salary by 15%, whose experience is greater than 10 years. b) Delete the employees, who completed 30 years of service. c) Display the manager who is having maximum number of employees working under him? d) Create a view, which contain employee names and their manage CREATE TABLE  Dept (deptno INT,dname VARCHAR(255),loc VARCHAR(255));CREATE TABLE  Emp (empno INT,ename VARCHAR(255),job VARCHAR(255),mgr INT,hiredate DATE,sal DECIMAL(10,2),comm DECIMAL(10,  2),deptno INT);INSERT INTO  Dept (deptno,  dname,  loc) VALUES(10, 'Finance', 'New York'),(20, 'Marketing', 'Los Angeles'),(30, 'HR', 'Chicago');INSERT INTO  Emp (empno,  ename,  job,  mgr,  hiredate,  sal,  comm,  deptno) VALUES(1001, 'John Doe', 'Manager', NULL, '2010-01-01',  5000.00, NULL,  10),(1002, 'Jane Smith', 'Assistant Manager',  1001, '2012-05-15',  3500.00, NULL,  10),(1003, 'Michael Johnson', 'Clerk',  1002, '2015-03-10',  2500.00, NULL,  10),(2001, 'Robert Williams', 'Manager', NULL, '2008-07-01',  5500.00, NULL,  20),(2002, 'Emily Davis', 'Clerk',  2001, '2013-11-20',  3000.00, NULL,  20),(3001, 'Daniel Brown', 'Manager', NULL, '2005-03-15',  6000.00, NULL,  30),(3002, 'Olivia Wilson', 'Assistant Manager',  3001, '2010-08-10',  4000.00, NULL,  30),(3003, 'Sophia Taylor', 'Clerk',  3001, '2016-02-05',  2800.00, NULL,  30);SELECT * FROM  Emp;-- a) Update the employee salary by 15% whose experience is greater than 10 years:UPDATE  Emp SET  sal =  sal *  1.15 WHERE DATEDIFF(YEAR,  hiredate, GETDATE()) >  10;SELECT * FROM  Emp;-- b) Delete the employees who completed 30 years of service:DELETE FROM  Emp WHERE DATEDIFF(YEAR,  hiredate, GETDATE()) >=  30;SELECT * FROM  Emp;-- c) Display the manager who is having the maximum number of employees working under him:SELECT  e1.ename AS  manager_name, COUNT(e2.empno) AS  num_employees FROM  Emp e1 LEFT JOIN  Emp e2 ON  e1.empno =  e2.mgr GROUP BY  e1.ename ORDER BY  num_employees DESC;-- d) Create a view that contains employee names and their managers:CREATE VIEW  EmployeeManagers ASSELECT  e1.ename AS  employee_name,  e2.ename AS  manager_name FROM  Emp e1 LEFT JOIN  Emp e2 ON  e1.mgr =  e2.empno;GOSELECT * FROM  EmployeeManagers;DROP TABLE  Dept;DROP TABLE  Emp; 9. Using Employee Database perform the following queries a) Determine the names of employee, who earn more than their managers. b) Determine the names of employees, who take highest salary in their departments. c) Determine the employees, who are located at the same place. d) Determine the employees, whose total salary is like the minimum Salary of any department. e) Determine the department which does not contain any employees 10. Using the tables “DEPARTMENTS” and “EMPLOYEES” perform the following Queries a) Display the employee details, departments that the departments are same in both the emp and dept. b) Display the employee name and Department name by implementing a left outer join. c) Display the employee name and Department name by implementing a right outer join. d) Display the details of those who draw the salary greater than the average salary. -- Create tableCREATE TABLE  DEPARTMENTS (department_id INT,department_name VARCHAR(50));CREATE TABLE  EMPLOYEES (employee_id INT,employee_name VARCHAR(50),department_id INT,salary FLOAT);-- Insert data into tablesINSERT INTO  DEPARTMENTS VALUES (1, 'Sales');INSERT INTO  DEPARTMENTS VALUES (2, 'Marketing');INSERT INTO  DEPARTMENTS VALUES (3, 'Human Resources');INSERT INTO  EMPLOYEES VALUES (1, 'John Doe',  1,  5000.00);INSERT INTO  EMPLOYEES VALUES (2, 'Jane Smith',  2,  6000.00);INSERT INTO  EMPLOYEES VALUES (3, 'Mike Johnson',  1,  5500.00);INSERT INTO  EMPLOYEES VALUES (4, 'Emily Williams',  4,  4500.00);INSERT INTO  EMPLOYEES VALUES (5, 'David Brown',  2,  7000.00);/*SELECT * FROM DEPARTMENTS;SELECT * FROM EMPLOYEES;*/-- Display the employee details and departments where the department IDs match in both the "EMPLOYEES" and "DEPARTMENTS" tables:SELECT  E.employee_id,  E.employee_name,  D.department_name FROM  EMPLOYEES E INNER JOIN  DEPARTMENTS D ON  E.department_id =  D.department_id;-- Display the employee name and department name using a left outer join, including all employees even if they don't have a department:SELECT  E.employee_name,  D.department_name FROM  EMPLOYEES E LEFT OUTER JOIN  DEPARTMENTS D ON  E.department_id =  D.department_id;-- Display the employee name and department name using a right outer join, including all departments even if they don't have employees:SELECT  E.employee_name,  D.department_name FROM  EMPLOYEES E RIGHT OUTER JOIN  DEPARTMENTS D ON  E.department_id =  D.department_id;-- Display the details of employees who earn a salary greater than the average salarySELECT  E.employee_id,  E.employee_name,  D.department_name,  E.salary FROM  EMPLOYEES E INNER JOIN  DEPARTMENTS D ON  E.department_id =  D.department_id WHERE  E.salary > (SELECT AVG(salary) FROM  EMPLOYEES);DROP TABLE  DEPARTMENTS;DROP TABLE  EMPLOYEES;
```
