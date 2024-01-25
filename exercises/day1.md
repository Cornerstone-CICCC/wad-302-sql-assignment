# Exercise - SQL Assignment - Day 1

# Instructions

This assignment has tests to verify if your answers are right.
It's necessary to install the libraries to use the tests.

To do that, install all dependencies using the command below:

```bash
npm install
```

Before running the test you need to set up your environment variable (.env).

Create a file .env in the root of the project and add the follow variables:

```json
    DB_USER= 'your psql user'
    DB_HOST= 'localhost'
    DB_DATABASE= 'name of your database'
    DB_PASSWORD= ''
    DB_PORT=5432
```

To run all the tests you need to use the script test:

```bash
npm run test
```

If you want to run a specific test use the follow command:

```bash
npm test <file>
```

Follow the steps to do the assignment.

Please note that the exercise assumes that your `psql` is already up and running.

1. Create a new database called `week_assignment` or whatever you want to call our app using `psql`.

2. Create the tables for our `students` and `classes` entities.

   - Create a folder called `migrations` within the `week_assignment` folder.
   - Inside `migrations`, create a file called `01_students_classes.sql`.
   - Write the SQL queries to create the tables for the `students` and `classes` entities. Use the ERD to help (README.MD in the root).
   - From your psql session, type `\i migrations/students_classes.sql` to execute the file.
   - Now enter `\dt` into your psql session to make sure the two tables have been created.

   Obs.: use the command `\cd + path of the project` to change the directory and then you can use the `\i` to execute the file.

3. Import the students' and classes' data from the `seeds` folder into the database.

   - From your psql session, type `\i seeds/students_seeds.sql` to execute the file.
   - Do the same for classes.
   - Now enter `SELECT count(*) FROM students;` and `SELECT count(*) FROM classes;` into your psql session to make sure the students and classes have been imported.

4. Commit all your changes and push them to GitHub.

5. Get all students without a Github username.

   - Create a file called `01_get_students_without_github.sql` in the `queries` folder.
   - Show only `id`, `name`, `email` and `class_id` columns.
   - Order them by `class_id`.
   - Execute the file and check the results.

   > Remember to create a new file for each query.

6. Get all students in a specific class.

   - Create a file called `02_get_students_in_class.sql` in the `queries` folder.
   - Show only `id` and `name` columns.
   - Order them by their name in alphabetical order.
   - Since this query needs to work with any specific class, just use any number for the class_id.
   - Execute the file and check the results.

7. Select the total number of students who were in the first 3 classes.

8. Get all of the students that don't have an email or phone number.

9. Get all of the students without a `gmail.com` account and a phone number.

10. Get all of the students currently enrolled.

    - Get their `name`, `id` and `class_id`.
    - Order them by `class_id`.

11. Get all graduates without a linked Github account.

    - Get their `name`, `email` and `phone`.

12. Write the CREATE TABLE statements for the assignments and a assignment_submissions tables.

    - Create a file called `02_assignments_assignment_submissions.sql` in the `migrations` folder.
    - Write the SQL queries to create the tables for the `assignments` and `assignment_submissions` entities. Use the ERD to help.
    - From your psql session, type `\i migrations/assignments.sql` to execute the file.
    - Now enter `\dt` into your psql session to make sure the two tables have been created.

13. Import the assignments' and assignment submissions' data from the `seeds` folder into the database.

    - From your psql session, type `\i seeds/assignments_seeds.sql` to execute the file.
    - Do the same for assignment submissions.
    - Now enter `SELECT count(*) FROM assignments;` and `SELECT count(*) FROM assignment_submissions;` into your psql session to make sure the students and classes have been imported.

14. Commit and push your changes to GitHub.
