# Task Manager App

Task Manager app is built on NodeJS runtime that performs CRUD operations on users,tasks.
Each user has a set of tasks and one user cannot access another user's tasks.
## Dependencies
- Security implemented via JWT(to maintain sessions) and BcryptJS(one way hashable password security). 
- Used npm module sendgrid to send welcome email (on creation of user) and unsubscribe email (on deletion of user)
- Database: MongoDB and corresponding Mongoose npm module for interaction via code.
- Robo3T for db manipulations.
- Multer for file uploads.
## Deployment
- Deployed on Heroku at https://task-manager-api-nancy-pitta.herokuapp.com
- This app doesnt yet have GUI to interact with yet.
## Usage
To use:
1. Create a user in Postman by providing the following in body and route:
    ```POST {{url}}/users/create```
  ```
  {
    "name":"<Your name>",
    "age":<Age>,
    "email":"<Valid Email>",
    "password":"<password>"
  }
  ```
  This enables user to login.
2. Create a task in a similar manner at ```POST {{url}}/tasks/create```
  ```
  {
    "description":"<Some description>",
    "completed":false
  }
  ```
3. List tasks created by user at ```GET {{url}}/tasks?completed=false&sortBy=createdAt:desc```
4. Read user info at ```GET {{url}}/users/me```
5. Update user,Update Task , Delete User,Delete Task

## To-Do
- Enable user to upload profile picture.
- GUI to interact with
