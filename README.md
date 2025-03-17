# Backend Authentication API

## Overview
This project is a **Node.js-based Authentication & User Management System** built for the **Backend Developer Internship Assignment**. It provides functionalities for user authentication using **JWT** and CRUD operations for user management.

## Features
- **User Authentication**: Signup, Login, Logout using **JWT**.
- **CRUD Operations**: Manage user data.
- **Secure Passwords**: Hashed using **bcrypt**.
- **Middleware Security**: Protect routes using JWT authentication.
- **Database**: Uses **MongoDB**.

## Technologies Used
- **Node.js** & **Express.js** (Backend)
- **MongoDB** & **Mongoose** (Database)
- **JWT** (Authentication)
- **bcrypt** (Password Hashing)
- **dotenv** (Environment Variables)
- **Nodemon** (Development)

## Project Setup
### 1️⃣ Clone the Repository
```bash
git clone https://github.com/your-username/backend-auth-api.git
cd backend-auth-api
```

### 2️⃣ Install Dependencies
```bash
npm install
```

### 3️⃣ Set Up Environment Variables
Create a `.env` file and add:
```
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_secret_key
PORT=5000
```

### 4️⃣ Start the Server
```bash
npm run dev  # Starts in development mode with nodemon
```

## API Documentation
### 🔹 **Authentication APIs**
#### 1️⃣ Signup (Register User)
**Endpoint:** `POST /api/auth/signup`
**Request Body:**
```json
{
  "name": "John Doe",
  "email": "john@example.com",
  "password": "password123"
}
```
**Response:**
```json
{
  "message": "User registered successfully"
}
```

#### 2️⃣ Login
**Endpoint:** `POST /api/auth/login`
**Request Body:**
```json
{
  "email": "john@example.com",
  "password": "password123"
}
```
**Response:**
```json
{
  "token": "your-jwt-token"
}
```

#### 3️⃣ Logout
**Endpoint:** `POST /api/auth/logout`
**Response:**
```json
{
  "message": "Logout successful"
}
```

### 🔹 **User Management APIs**
#### 4️⃣ Get All Users (Protected)
**Endpoint:** `GET /api/users/`
**Headers:**
```
Authorization: Bearer <your-jwt-token>
```

#### 5️⃣ Get Single User (Protected)
**Endpoint:** `GET /api/users/:id`

#### 6️⃣ Update User (Protected)
**Endpoint:** `PUT /api/users/:id`
**Request Body:**
```json
{
  "name": "Updated Name"
}
```

#### 7️⃣ Delete User (Protected)
**Endpoint:** `DELETE /api/users/:id`


