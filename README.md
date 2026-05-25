This project is a full-stack Blog Application backend developed using:

* Node.js
* Express.js
* MongoDB
* JWT Authentication
* Middleware Authorization
* REST APIs

The application supports multiple user roles such as:

* Admin
* Author
* User

It provides secure authentication and authorization for managing blog articles and users.

---

# Features

## Authentication System

* User Registration
* User Login
* JWT Token Authentication
* Secure Protected Routes

---

## Role-Based Access Control

Different access permissions for:

* Admin
* Author
* Normal User

---

## Blog Article Management

* Create Articles
* Read Articles
* Update Articles
* Delete Articles

---

## Middleware Security

* Verify JWT Tokens
* Check Author Permissions
* Protect APIs from unauthorized access

---

# Project Structure

```bash
Blog-App/
│
├── APIs/
│   ├── AdminApi.js
│   ├── AuthorApi.js
│   ├── CommonApi.js
│   └── UserApi.js
│
├── Middlewares/
│   ├── CheckAuthor.js
│   └── VerifyToken.js
│
├── Models/
│   ├── Articlemodel.js
│   └── usermodel.js
│
├── Services/
│   └── AuthenticationService.js
│
├── package.json
├── package-lock.json
├── req.http
├── .gitignore
└── server.js
```

---

# Technologies Used

| Technology | Purpose                  |
| ---------- | ------------------------ |
| Node.js    | Runtime Environment      |
| Express.js | Backend Framework        |
| MongoDB    | Database                 |
| Mongoose   | Database Modeling        |
| JWT        | Authentication           |
| Middleware | Authorization & Security |

---

# Core Concepts Used

---

# Node.js

## Definition

Node.js is a JavaScript runtime used to execute JavaScript outside the browser.

### Features

* Fast execution
* Event-driven architecture
* Non-blocking operations

---

# Express.js

## Definition

Express.js is a Node.js framework used to build APIs and backend applications.

### Example

```js
const express = require("express");
const app = express();
```

---

# REST API

## Definition

REST API enables communication between frontend and backend using HTTP requests.

### HTTP Methods

| Method | Purpose     |
| ------ | ----------- |
| GET    | Fetch data  |
| POST   | Create data |
| PUT    | Update data |
| DELETE | Remove data |

---

# MongoDB

## Definition

MongoDB is a NoSQL database that stores data in JSON-like format.

### Advantages

* Flexible schema
* Easy scalability
* High performance

---

# JWT Authentication

## Definition

JWT (JSON Web Token) is used for secure authentication.

### Authentication Flow

```text
User Login
    ↓
Server Verifies Credentials
    ↓
JWT Token Generated
    ↓
Client Stores Token
    ↓
Protected APIs Use Token
```

---

# APIs Folder

---

# AdminApi.js

## Purpose

Handles admin-related operations.

### Features

* Manage users
* Manage articles
* Admin-level access

---

# AuthorApi.js

## Purpose

Handles author operations.

### Features

* Create articles
* Update articles
* Delete own articles

---

# UserApi.js

## Purpose

Handles user-related operations.

### Features

* User registration
* User login
* Profile handling

---

# CommonApi.js

## Purpose

Contains APIs accessible by all users.

### Features

* Fetch articles
* Public blog access

---

# Middlewares

---

# VerifyToken.js

## Purpose

Verifies JWT token before accessing protected APIs.

### Features

* Token validation
* Authentication checking
* Secure routes

### Example

```js
app.use(verifyToken);
```

---

# CheckAuthor.js

## Purpose

Checks whether the logged-in user is the article author.

### Features

* Author verification
* Prevent unauthorized modifications

---

# Models

---

# Articlemodel.js

## Purpose

Defines schema for blog articles.

### Common Fields

* Title
* Content
* Author
* Category
* Created Date

---

# usermodel.js

## Purpose

Defines schema for application users.

### Common Fields

* Username
* Email
* Password
* Role

---

# Services

---

# AuthenticationService.js

## Purpose

Handles authentication logic.

### Features

* Password verification
* Token generation
* User authentication logic

---

# Middleware

## Definition

Middleware functions execute before API routes.

### Uses

* Authentication
* Authorization
* Validation
* Logging

---

# Authorization

## Definition

Authorization checks whether a user has permission to perform an action.

### Example

* Only authors can edit their own articles
* Only admins can manage all users

---

# CRUD Operations

| Operation | Meaning      |
| --------- | ------------ |
| Create    | Add new data |
| Read      | Fetch data   |
| Update    | Modify data  |
| Delete    | Remove data  |

---

# API Workflow

```text
Client Request
      ↓
Express Server
      ↓
Middleware Verification
      ↓
API Route Handler
      ↓
MongoDB Database
      ↓
Response Returned
```

---

# Example API Endpoints

| Method | Endpoint        | Description      |
| ------ | --------------- | ---------------- |
| POST   | `/register`     | Register user    |
| POST   | `/login`        | Login user       |
| GET    | `/articles`     | Get all articles |
| POST   | `/articles`     | Create article   |
| PUT    | `/articles/:id` | Update article   |
| DELETE | `/articles/:id` | Delete article   |

---

# req.http File

## Purpose

Used for API testing directly inside VS Code or REST Client extension.

### Common Tests

* User registration
* Login requests
* Create article
* Fetch articles

---

# How to Run the Project

---

## Step 1: Install Dependencies

```bash
npm install
```

---

## Step 2: Start Server

```bash
node server.js
```

OR

```bash
nodemon server.js
```

---

## Step 3: Open API Client

Examples:

* Postman
* Thunder Client
* REST Client Extension

---

# Learning Outcomes

After completing this project, the following concepts are understood:

* Backend Development
* REST API Design
* MongoDB Integration
* JWT Authentication
* Role-Based Authorization
* Middleware Handling
* CRUD Operations
* Modular Project Structure

---

# Tools Used

* VS Code
* Node.js
* MongoDB Compass
* Postman
* GitHub

---

# Real-World Use Cases

| Feature        | Real-World Example    |
| -------------- | --------------------- |
| Authentication | Login systems         |
| Authorization  | Role-based dashboards |
| Articles       | Blogging platforms    |
| Middleware     | Secure backend APIs   |
| MongoDB        | Content storage       |

---

# Conclusion

This capstone project demonstrates a complete backend architecture for a Blog Application using Node.js, Express.js, MongoDB, and JWT authentication. It includes secure authentication, role-based authorization, middleware protection, and article management functionalities using a modular and scalable backend structure.
