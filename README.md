# sqlorcql

create table employee(employeeId int not null primary key, firstName varchar(100),lastName varchar(100),salary int,joinningDate timestamp,
department varchar(10),gender varchar(10));
desc employee
insert into employee
values(1,'vikas','ahlawat',600000,to_timestamp('2013-02-15 11:16:28','yyyy-mm-dd hh24:mi:ss'),'it','male')
insert into employee
values(2,'nikita','jain',530000,to_timestamp('2014-01-09 17:31:07','yyyy-mm-dd hh24:mi:ss'),'hr','female')
insert into employee
values(3,'ashish','kumar',1000000,to_timestamp('2014-01-09 10:05:07','yyyy-mm-dd hh24:mi:ss'),'it','male')
insert into employee
values(4,'nikhil','sharma',480000,to_timestamp('2014-01-09 09:00:07','yyyy-mm-dd hh24:mi:ss'),'it','male')
insert into employee
values(5,'ansh','kadian',500000,to_timestamp('2014-01-09 09:31:07','yyyy-mm-dd hh24:mi:ss'),'payroll','male')

//1--Write a query to get all employee detail from "Employee" table 
select * from employee

2-- Write a query to get only "FirstName" column from "Employee" table 
SELECT *
FROM employee
WHERE firstName = 'ansh';
3-- Write a query to get FirstName in upper case as "First Name". 
SELECT UPPER(firstName) AS "First Name"
FROM employee;
4--Write a query to get FirstName in lower case as "First Name". 

SELECT LOWER(firstName) AS "First Name"
FROM employee;
5--Write a query for combine FirstName and LastName and display it as "Name" (also include white space between first name & last name)
SELECT firstName || ' ' || lastName AS "Name"
FROM employee;
6--Select employee detail whose name is "Vikas"

SELECT *
FROM employee
WHERE firstName ='vikas'
7--Get all employee detail from Employee table whose "FirstName" start with latter 'a'
SELECT *
FROM employee
WHERE LOWER(firstName) LIKE 'a%'; // % wild card character

8--Get all employee details from Employee table whose "FirstName" contains 'k' 
SELECT *
FROM employee
WHERE firstName LIKE '%k%';
9--Get all employee details from Employee table whose "FirstName" end with 'h' 

SELECT *
FROM employee
WHERE LOWER(firstName) LIKE '%h';
10--Get all employee detail from Employee table whose "FirstName" start with any single character between 'a-p'--
SELECT *
FROM employee
WHERE REGEXP_LIKE(firstName, '^[a-p]', 'i');










