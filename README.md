# Final-Task-2

This portfolio demonstrates my understanding of MySQL database creation using a simplified student assignment submission system. It goes over how to create tables that show students, assignments, and their contributions step-by-step. In order to create a completely effective relational schema, this exercise uses data types, relationships, and constraints such as primary keys, foreign keys, and composite keys.

## 1. Create the student table:
- Define username as a VARCHAR(50)
- Set username as the Primary Key

## 2. Create the assignment table:
-- Define shortname as a VARCHAR(50) and set it as the Primary Key
- Define due_date as a DATE NOT NULL
- Define url as a VARCHAR(255), which can be null

## 3. Create the submission table:
- Define username and shortname both as VARCHAR(50)
- Define version as an INT
- Define submit_date as a DATE NOT NULL
- Define data as TEXT
- Set a composite primary key of (username, shortname, version)
- Add foreign keys referencing the student and assignment tables

# Table Relationships

## 1. student table
- Primary Key: username
- Relationships:
- One-to-Many with submission: One student (username) can have many submissions.

## 2. assignment table
- Primary Key: shortname
- Relationships:
- One-to-Many with submission: One assignment (shortname) can have many submissions.

## 3. submission table
- Composite Primary Key: (username, shortname, version)
- Relationships:
- Many-to-One with student: Each submission belongs to one student.
- Many-to-One with assignment: Each submission is for one assignment.
- This models a Many-to-Many relationship between students and assignments, with version tracking multiple submissions.


## Screenshots

## student Table Sql Code 
![task2 create studenttbl](https://github.com/user-attachments/assets/5818ba5e-3541-418e-a28e-a78ad4be563c)
 
## student Table Output
![task2 studenttbl](https://github.com/user-attachments/assets/1b6f5b9c-dbaf-4e20-8ee6-9338919f16ed)



## assignment Table Sql Code  
![task2 create assignmenttbl](https://github.com/user-attachments/assets/353096d5-d488-4eae-b517-1958501d888d)
## assignment Table Output
![task 2 assignmenttbl](https://github.com/user-attachments/assets/0292fb00-2c55-4300-8f90-24d9d62c3848)



## submission Table Sql Code  
![task2 create submissiontbl](https://github.com/user-attachments/assets/9700303e-3940-434a-aa11-2577712a557c)
## submission Table Output
![task2 submissiontbl](https://github.com/user-attachments/assets/28fe66a3-d24d-4112-b95d-6a8e12c9d257)


## EER Diagram 
![EERD TASK 2](https://github.com/user-attachments/assets/b8aa8cc0-bc89-41e3-a5c9-d9dfc2da7f96)


## Sql Code 
![final2](https://github.com/user-attachments/assets/f61d8dde-263d-401c-a10a-3b43c96bb6a6)








