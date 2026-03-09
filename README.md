MicroGoals – Secure Goal Management Backend API
1. Project Abstract
MicroGoals is a secure backend RESTful API designed for managing personal goals digitally. The system is developed using Node.js, Express.js, and MongoDB. It allows users to register, log in, and manage their personal goals through Create, Read, Update, and Delete (CRUD) operations.
The application implements JSON Web Token (JWT) authentication to ensure secure access to protected routes. Each user can only manage their own goals, ensuring privacy and data protection.
The main purpose of this project is to develop a scalable and secure backend system that demonstrates REST API development, authentication, database integration, and middleware handling.
2. Introduction
Goal management is an important part of personal productivity. Many people track goals digitally to improve their efficiency and monitor progress.
The MicroGoals API provides a backend system where users can:
Register an account
Log into the system
Create and manage goals
Update goal completion status
Delete goals
The system uses JWT authentication to protect routes and ensures that users only access their own data.
This project also follows the MVC (Model-View-Controller) architecture, which improves maintainability, scalability, and code organization.
3. Objectives of the Project
The main objectives of the project are:
To develop a secure RESTful API
To implement user authentication using JWT
To allow users to manage personal goals
To perform CRUD operations on goals
To ensure secure and user-specific data access
To demonstrate backend development using Node.js and MongoDB
4. Tools and Technologies Used
Tool / Technology
Purpose
Node.js
Runtime environment
Express.js
Backend framework
MongoDB
Database
Visual Studio Code
Code editor
Thunder Client
API testing
JWT (JSON Web Token)
Authentication
Mongoose
MongoDB object modeling
5. System Architecture
The system follows a REST API architecture with MVC pattern.
Components
Client
Sends HTTP requests to the API.
Server
Built using Node.js and Express.js.
Handles routing, authentication, and logic.
Database
MongoDB stores users and goals.
Middleware
Authentication middleware for verifying JWT tokens.
Error middleware for centralized error handling.
6. ER Diagram
Entities
User
_id
name
email
password
Goal
_id
title
completed
userId (Reference to User)
Relationship
One User → Many Goals
7. Project Modules
1. User Authentication Module
This module manages user registration and login.
Functions:
User signup
Password hashing
Login verification
JWT token generation
2. Goal Management Module
This module handles CRUD operations for user goals.
Functions:
Create goal
View goals
Update goal status
Delete goals
Each goal is linked to a specific user.
3. Authorization Module
This module ensures that only authenticated users can access protected routes.
Features:
JWT verification
Token validation
User-specific access control
4. Error Handling Module
This module manages runtime errors and invalid requests.
Features:
Centralized error handling
Standard HTTP status responses
Error logging
8. Project Features
User Registration
Secure Login
JWT Authentication
Goal Creation
Goal Updating
Goal Deletion
User-specific goal viewing
Protected routes
Centralized error handling
9. Project Folder Structure
Copy code

MicroGoals/
│
├── middleware/
│   ├── authMiddleware.js
│   └── errorMiddleware.js
│
├── models/
│   ├── userModel.js
│   └── goalModel.js
│
├── routes/
│   ├── authRoutes.js
│   └── goalRoutes.js
│
├── Schema/
│   ├── User.js
│   └── GoalSchema.js
│
├── .env
├── index.js
└── package.json
10. Project Workflow
User registers an account
User logs into the system
Server generates a JWT token
Token is sent with API requests
Authentication middleware verifies the token
User accesses protected routes
User performs CRUD operations on goals
11. Roles and Responsibilities
Role
Responsibility
User
Register, login, and manage goals
Developer
Design, develop, and test APIs
12. Project Execution Steps
Start MongoDB database
Run the Node.js server
Test APIs using Thunder Client
Register a new user
Login and receive JWT token
Use token for protected routes
Perform CRUD operations on goals
13. Conclusion
The MicroGoals Backend API successfully demonstrates the development of a secure RESTful backend system using Node.js and MongoDB. The system provides authentication, goal management, and secure user-specific data handling.
This project highlights important backend development concepts such as:
REST API development
JWT authentication
Database integration
Middleware implementation
MVC architecture
The system can be further enhanced by adding a frontend interface and additional features like goal reminders and analytics.
