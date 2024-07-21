# Hands-on-Lab-Create-Tables-using-SQL-Scripts-and-Load-Data-into-Tables-in-PgAdmin-4

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

   ![image](https://github.com/user-attachments/assets/e2d7f9e6-0d7a-4b34-aca2-d522a36136d3)

3. Employees Table

   ![image](https://github.com/user-attachments/assets/ddc10e47-bd32-4dc5-95e0-da4fee0919c8)

5. Jobs Table

   ![image](https://github.com/user-attachments/assets/b306122b-9ff0-4f24-8ba6-03e973677c67)

6. Locations Table

   ![image](https://github.com/user-attachments/assets/0e51e444-f6bb-4d9b-941e-9f160a7a00bf)

8. JobsHistory Table

  ![image](https://github.com/user-attachments/assets/99c24977-dffc-4abd-9420-51974c83f087)


