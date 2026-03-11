# 🔐 JWT Authentication using Spring Boot

This project demonstrates the implementation of **JWT (JSON Web Token) authentication** using **Spring Boot, Spring Security, MySQL, and Postman**.

The system verifies user credentials from the database and generates a **JWT token** upon successful login. This token is then used to access protected API endpoints.

---

# Technologies Used

- Java
- Spring Boot
- Spring Security
- JWT (JSON Web Token)
- MySQL
- Postman
- Eclipse IDE

---

# Project Workflow

1. Run the Spring Boot application
2. Create and configure the MySQL database
3. Insert user credentials into the database
4. Authenticate the user using Postman
5. Generate JWT token
6. Use the token to access protected API endpoints

---

# Step 1: Running the Spring Boot Application

The JWT Authentication application was executed as a **Java Application** in Eclipse.  
After running the project successfully, the **embedded Tomcat server started on port 8080**.

<img width="1007" height="279" alt="Screenshot 2026-03-11 095450" src="https://github.com/user-attachments/assets/86b3d449-234b-4d82-be23-f4b191e992b2" />


---

# Step 2: Creating the Database

A new database named **jwtauth** was created in MySQL to store user authentication details.

<img width="435" height="636" alt="Screenshot 2026-03-11 095027" src="https://github.com/user-attachments/assets/75998d74-05c3-4df5-8c5c-70a8f23d04b8" />
.

---

# Step 3: Creating Users Table

Inside the **jwtauth database**, a table named **users** was created to store login credentials such as username and password.

Example structure:

| id | username | password |
|----|----------|----------|
| 1  | ram      | 1234     |

<img width="647" height="101" alt="Screenshot 2026-03-11 100717" src="https://github.com/user-attachments/assets/c02aa049-1d98-4ea3-b5f8-a093aa100ba1" />
<img width="445" height="227" alt="Screenshot 2026-03-11 095014" src="https://github.com/user-attachments/assets/3f745089-ac5e-4a24-b71b-f4a89e0c11c0" />

---

# Step 4: Login Request using Postman

A **POST request** was sent using Postman to authenticate the user.

API Endpoint:

POST http://localhost:8080/api/login

Parameters sent:

username = ram  
password = 1234

If the credentials are valid, the server generates a **JWT token**.

<img width="1261" height="736" alt="Screenshot 2026-03-11 094958" src="https://github.com/user-attachments/assets/974cfadf-cf7a-465c-82ab-840e929b9507" />


---

# Step 5: Accessing the Protected API

The generated JWT token was copied and added to the **Authorization header** in Postman using the Bearer token format.

Authorization Header Format:

Authorization: Bearer <JWT Token>

Then a **GET request** was sent to the protected API endpoint.

API Endpoint:

GET http://localhost:8080/api/hello

If the token is valid, the server verifies it and returns a success message.

<img width="1260" height="770" alt="Screenshot 2026-03-11 094929" src="https://github.com/user-attachments/assets/1c757586-1dd0-4114-96e2-8b2ffb789c24" />


---

# API Endpoints

| Method | Endpoint | Description |
|------|------|------|
| POST | /api/login | Authenticate user and generate JWT token |
| GET | /api/hello | Protected API that requires JWT token |

---

# Result

JWT Authentication was successfully implemented using Spring Boot and Spring Security.  
The application generated a valid JWT token after login and allowed access to secured API endpoints using the token.

---

# Learning Outcome

- Learned how JWT authentication works
- Implemented secure REST APIs using Spring Boot
- Integrated Spring Boot with MySQL database
- Tested APIs using Postman
