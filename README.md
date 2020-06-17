# Project School

A project demonstrating Knowledge of Java Spring MVC, Java REST API, and custome exception handling.

## Introduction

This is a standard database scheme with courses, students, and instructors. This Java Spring REST API application will provide endpoints for clients to perform the various CRUD operations on data sets contained in the application's data.

### Database layout



![School Database Layout](schooldb.png)

All tables contain the following auditing fields

created_by - user name who created the row. Should default to SYSTEM
created_date - date field when the row was created
last_modified_by - user name who last changed data in the row. Should default to SYSTEM
last_modified_date - date field when the data in the row was last changed

Table Relationships include

* Courses table is the driving table.
* Instructors have a Many-To-One relationship with Courses. Each instructor can teach many courses but each course will have only one instructor.
* Students have a Many-To-Many relationship with Courses. Students can take multiple courses and each course will have multiple students.

The starting application is not meant to be a complete, stand-alone application. The application has enough to complete the project but is missing many key endpoints such as endpoints related to instructors, PATCH endpoints, and a variety of necessary updates and deletes relating to many to many relationships.

For those available endpoints, using the provided seed data, this application returns the following data. Expand the section of the endpoint to see the data that is returned.

###End Points


GET 2019/courses/courses
Provides list of all courses

GET 2019/courses/courses/{id}
Provides a specific course object

POST 2019/courses/course
Adds new course object to end.

GET 2019/students/students
Provides list of all students and courses they are enlisted in.

GET 2019/students/student/{studentid}
Provides student and course list.

POST 2019/students/student
Adds new student object to end.





### Custom exception handling
  * **Title** - The title of the exception
  * **Status** - Http Status Code
  * **detail** - Detailed message for the client
  * **timestamp** - date and time of the exception
  * **developer** -  message for developers about this error message, things like class and code causing the error
  * **List of Validation Errors** - If data validation errors caused this error, the list of them will appear here

