# Aggregate-function-in-SQL
## AIM:
To create asql program in aggregate function in SUM(),COUNT(),AVG() OPERATIONS.
## ALGORITHM:
Initialize the accumulator variable(s) based on the type of aggregate functioN
Retrieve the data from the table or source based on the query's filtering conditions, if any.
Iterate over the retrieved data.
For each row:
Update the accumulator variable(s) based on the type of aggregate function
For SUM(): Add the value of the selected column to the sum variable.
For COUNT(): Increment the count variable by one.
For AVG(): Add the value of the selected column to the sum variable and increment the count variable by one.
After iterating over all the row
Display or use the result of the aggregate function as needed.
## PROGRAM:
~~~
java

-- Create the table
CREATE TABLE Worker (
  WORKER_ID INT NOT NULL PRIMARY KEY,
  FIRST_NAME CHAR(25),
  LAST_NAME CHAR(25),
  SALARY INT(15),
  JOINING_DATE DATETIME,
  DEPARTMENT CHAR(25)
);

-- Insert values into the table
INSERT INTO Worker (WORKER_ID, FIRST_NAME, LAST_NAME, SALARY, JOINING_DATE, DEPARTMENT)
VALUES
  (1, 'Monika', 'Arora', 100000, '2020-02-14 09:00:00', 'HR'),
  (2, 'Niharika', 'Verma', 80000, '2021-06-11 09:00:00', 'Admin'),
  (3, 'Vishal', 'Singhal', 300000, '2020-02-14 09:00:00', 'HR'),
  (4, 'Amitabh', 'Singh', 500000, '2020-02-14 09:00:00', 'Admin'),
  (5, 'Vivek', 'Bhati', 500000, '2021-06-11 09:00:00', 'Admin'),
  (6, 'Vipul', 'Diwan', 200000, '2021-06-11 09:00:00', 'Account'),
  (7, 'Satish', 'Kumar', 75000, '2020-01-20 09:00:00', 'Account'),
  (8, 'Geetika', 'Chauhan', 90000, '2021-04-11 09:00:00', 'Admin');

-- Display the table
SELECT * FROM Worker;

-- Perform the SUM(), COUNT(), and AVG() operations
SELECT SUM(SALARY) AS sum_of_total_salary FROM Worker;
SELECT COUNT(*) AS count_of_total_workers FROM Worker;
SELECT AVG(SALARY) AS average_salary FROM Worker;
~~~
OUTPUT:
TABLE FOR WORKERS:
![image](https://github.com/SdMdZahi7/Aggregate-function-in-SQL/assets/94187572/f7bf366b-bd51-4eab-b18e-a6ba0b797822)

SUM(),COUNT(),AVG():
![image](https://github.com/SdMdZahi7/Aggregate-function-in-SQL/assets/94187572/563d04e5-9d06-461a-be77-ecbfd88636e3)

RESULT:
Thus we have successfully obtained the required result using the above-given code.
