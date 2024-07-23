# Hands-on-Lab-on-Creating-Tables-using-SQL-Scripts-and-Loading-Data-into-Tables-in-PgAdmin-4

This is a hands-on project on creating Tables using SQL Scripts and Loading Data into Tables in PgAdmin 4

# Software Used in this Lab

PgAdmin 4 (PostgreSQL 15)

# Database Used in this Lab

The database used in this lab is an internal database belonging to IBM; a sample HR database. This is an HR database schema that consists of 5 tables called EMPLOYEES, JOB_HISTORY, JOBS, DEPARTMENTS and LOCATIONS. Each table has a few rows of sample data. The following diagram shows the tables for the HR database:

![image](https://github.com/user-attachments/assets/067a7925-0c1d-4a68-a62f-6f9879919301)

# Objectives

The objectives of this project were to:

1. Create a database.
2. Create tables using SQL scripts
3. Load data into tables

# Task A: Creating tables using SQL scripts

In this task, I created my new database named "HR DB" in PgAdmin and then executed the script containing the CREATE TABLE commands for all the tables rather than create each table manually by typing the DDL commands in the SQL editor.

The HR_Database_Create_Tables_Script.sql is available here: https://drive.google.com/file/d/1DOUzVXi-jsWBHR6CLNhAFQYUXdPjKFf7/view?usp=sharing

I downloaded the script file to my computer and uploaded it on my query editor of the HR DB I have initially created.

![image](https://github.com/user-attachments/assets/ebfef8e5-dbae-400c-a72f-260e281a6c94)


# Task B: Loading data into tables

In this task, I loaded all the data into the HR DB Database from .CSV files.

I downloaded the 5 .csv files below to my local computer:

Departments.csv - file is available here: https://drive.google.com/file/d/16srI4TCFh_O8VGfrhd3q-msbFp_472zu/view?usp=sharing
Employees.csv - file is available here: https://drive.google.com/file/d/1LLGie9dXrR9WiFYE7t0vyD0eVCRajRtI/view?usp=sharing
Jobs.csv - file is available here: https://drive.google.com/file/d/1qLTJiiOUfgZ9sk8RIFV_6PlSM66pjUTR/view?usp=sharing
Locations.csv - file is available here: https://drive.google.com/file/d/1WHQja5oaxKn7EqWB0sOSD1sHGZnagSBh/view?usp=sharing
JobsHistory.csv - file is available here: https://drive.google.com/file/d/1-IZUPqwPlkU3BdMV5EW2zZl0tg7jZs7C/view?usp=sharing

To load each table, I did the following steps.

I right-clicked on each table and selected Import tab.

Chose the csv file and clicked on OK to load the csv file.

# Task C: Exploring the Tables

To explore each table in the database, I right-clicked on each table and selected view/edit data to view "All Rows" 

1. Dapartment Table

   ![image](https://github.com/user-attachments/assets/f35245c5-9a25-4c18-a06a-333e9a4fadd8)

3. Employees Table

   ![image](https://github.com/user-attachments/assets/f83d2120-5fb2-486f-857b-9c27353832b2)

5. Jobs Table

   ![image](https://github.com/user-attachments/assets/a9e3931b-0fdd-4949-834c-4297808923d3)

7. Locations Table

   ![image](https://github.com/user-attachments/assets/f75e89be-93ec-4b7d-ac16-63b5368bd9e7)

8. JobsHistory Table

   ![image](https://github.com/user-attachments/assets/5bcc6784-ba60-4089-b2b9-21a45554683c)

# Task D: Solving SQL problems Using String Patterns

1. Retrieve all employees whose address is in Elgin,IL.

   In solving this problem, I used the following SQL statement:

   SELECT f_name , l_name, address
   FROM employees
   WHERE address LIKE '%Elgin,IL%';

   ![image](https://github.com/user-attachments/assets/826786a6-d39d-4d31-9131-39de9ae37f74)

2. Retrieve all employees who were born during the 1970’s.

   In solving this problem, I used the following SQL statement:
   
   SELECT f_name, l_name, b_date
   FROM employees
   WHERE EXTRACT(YEAR FROM b_date) BETWEEN 1970 AND 1979;

   ![image](https://github.com/user-attachments/assets/91941af7-3bef-47f2-b78a-733c645f7a1e)

4. Retrieve all employees in department 5 whose salary is between 60000 and 70000.

   In solving this problem, I used the following SQL statement:
   
   SELECT f_name, l_name, salary
   FROM employees
   WHERE dep_id = '5' AND (salary BETWEEN 60000 AND 70000);

   ![image](https://github.com/user-attachments/assets/985e5027-f0df-41fa-ae7a-8c93d90dcaf0)

# Task E: Solving SQL problems Using Sorting.

1. Retrieve a list of employees ordered by department ID.

  In solving this problem, I used the following SQL statement:

  SELECT f_name, l_name, dep_id
  FROM employees
  ORDER BY dep_id

  ![image](https://github.com/user-attachments/assets/e165e404-766f-4cd0-8053-31f3a2cffddd)

2. Retrieve a list of employees ordered in descending order by department ID and within each department ordered alphabetically in descending order by last name.

   In solving this problem, I used the following SQL statement:

   SELECT f_name, l_name, dep_id
   FROM employees
   ORDER BY dep_id DESC, l_name DESC

  ![image](https://github.com/user-attachments/assets/0fb566d7-a1a0-43d9-b2b1-a4c6c9454514)

4. Retrieve a list of employees ordered by department name, and within each department ordered alphabetically in descending order by last name.

   In solving this problem, I used the following SQL statement:
   
   SELECT d.dep_name , e.f_name, e.l_name
   FROM employees as e, departments as d
   WHERE e.dep_id = d.dep_id_dep
   ORDER BY d.dep_name, e.l_name DESC;

   ![image](https://github.com/user-attachments/assets/8179984f-d5ad-4d80-b61d-f01d4b80f622)

# Task F: Solving SQL problems on Grouping

1. Retrieve the average salary for all employees in the EMPLOYEES table.

   In solving this problem, I issued the following SQL statement:
   
   SELECT AVG(salary) FROM employees

   ![image](https://github.com/user-attachments/assets/771bd759-9fef-4155-bc57-251de2345a9d)

2. For each department ID retrieve the number of employees in the department.

   In solving this problem, I issued the following SQL statement:

   SELECT dep_id, COUNT(*)
   FROM employees
   GROUP BY dep_id;

   ![image](https://github.com/user-attachments/assets/14a658b9-0ccf-44fc-adde-9392b1f9123c)

3. For each department retrieve the number of employees in the department, and the average employee salary in the department.

   In solving this problem, I issued the following SQL statement:

   SELECT dep_id, AVG(salary), COUNT (*)
   FROM employees
   GROUP BY dep_id

   ![image](https://github.com/user-attachments/assets/44238761-deb8-4cb4-a13b-ddb37634fe27)


4. Label the computed columns in the result set of SQL NO. 3 (Task F NO. 3) as NUM_EMPLOYEES and AVG_SALARY.

   In solving this problem, I issued the following SQL statement:

   SELECT AVG(salary) AS AVG_SALARY, COUNT (*) AS NUM_EMPLOYEES, dep_id
   FROM employees
   GROUP BY dep_id

   ![image](https://github.com/user-attachments/assets/4649806a-5d29-440e-8a12-f075ce14a0a6)

5. In SQL NO. 4 (Task F NO. 4), order the result set by Average Salary.

   In solving this problem, I issued the following SQL statement:

   SELECT dep_id, AVG(salary) AS AVG_SALARY, COUNT (*) AS NUM_EMPLOYEES
   FROM employees
   GROUP BY dep_id
   ORDER BY AVG_SALARY

   ![image](https://github.com/user-attachments/assets/0a91145d-b1bc-4ee3-9bea-2fe1cdbf6fcd)

6. In SQL NO. 5 (Task F NO. 5), limit the result to departments with fewer than 4 employees.

   In solving this problem, I issued the following SQL statement:

   SELECT dep_id, AVG(salary) AS AVG_SALARY, COUNT (*) AS NUM_EMPLOYEES
   FROM employees
   GROUP BY dep_id
   HAVING COUNT(*) < 4
   ORDER BY AVG_SALARY

   ![image](https://github.com/user-attachments/assets/447e3fd3-5f17-4251-b2cb-41cfe6994f48)

   
