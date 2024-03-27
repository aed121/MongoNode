Features
User authentication with JSON Web Tokens (JWT)
CRUD operations for tasks (Create, Read, Update, Delete)
Querying tasks by status or due date

Requirements
Node.js
MongoDB

Installation
Navigate to the project directory:

cd task-manager-api

markdown
Copy code

Install dependencies:

npm install

markdown
Copy code
Start MongoDB:

mongod

markdown
Copy code

Start the application:

npm start

markdown
Copy code

The application will be running at http://localhost:3000.

API Endpoints
POST /signup: Create a new user account.
POST /login: Authenticate user and generate JWT token.
GET /tasks: Retrieve all tasks.
POST /tasks: Create a new task.
PATCH /tasks/:id: Update an existing task.
DELETE /tasks/:id: Delete a task.
GET /tasks/status/:status: Query tasks by status.
GET /tasks/due/:dueDate: Query tasks by due date.

Authentication
JWT (JSON Web Tokens) are used for user authentication.
All routes, except for /signup and /login, require JWT authentication.

Database Schema
User Schema
username: String, required, unique
password: String, required
email: String, required

Task Schema
title: String, required
description: String
status: String (enum: ['Pending', 'Completed'], default: 'Pending')
dueDate: Date
