# Final Lab Task 2 - Transforming ER Model to Relational Tables

## Student Table:
- **username**: String (VARCHAR),up to 50 characters.
## Assignment Table:
- **shortname**: String (VARCHAR),up to 50 characters.
- **due_date**: Date, cannot be null.
- **url**: String (VARCHAR),up to 255 characters, can be null.
## Submission Table:
- **username**: String (VARCHAR),up to 50 characters.
- **shortname**: String (VARCHAR),up to 50 characters.
- **version**: Integer, represents the version of the submission.
- **submit_date**: Date, cannot be null.
- **data**: Text.
## Query Statements & Table Structure:
### Student:
#### Query:
![screenshot](image/Student.png)
#### Table:
![screenshot](image/Student_tbl.png)
### Assignment:
#### Query:
![screenshot](image/Assignment.png)
#### Table:
![screenshot](image/Assignment_tbl.png)
### Submission:
#### Query:
![screenshot](image/Submission.png)
#### Table:
![screenshot](image/Submission_tbl.png)
## ER Diagram:
![screenshot](image/ER-DIAGRAM.png)
