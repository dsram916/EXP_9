# 🔐 JWT Authentication REST API using Spring Boot

This project demonstrates JWT (JSON Web Token) based authentication and authorization using Spring Boot to secure REST APIs.

---

## 📌 Technologies Used
Java  
Spring Boot  
Spring Security  
JWT (JSON Web Token)  
Spring Data JPA (Hibernate)  
MySQL  
Postman  
Apache Tomcat (Embedded Server)  
Eclipse IDE  

---

## 🎯 Aim
To implement JWT authentication and authorize users to access secured APIs.

---

## ⚙️ Project Workflow
Run Spring Boot application → Initialize Tomcat → Connect to database → Store user credentials → Generate JWT token → Access secured APIs using token

---

## 🚀 Tomcat Initialization

<img width="1007" height="279" alt="Screenshot 2026-03-11 095450" src="https://github.com/user-attachments/assets/dc3e5f90-5b99-4963-a211-d4a4f9c4ea47" />


The application started successfully on port **8080** using the embedded Tomcat server.

---

## 🗄️ Database Verification

<img width="435" height="636" alt="Screenshot 2026-03-11 095027" src="https://github.com/user-attachments/assets/1b83fb6c-90cf-4751-8542-532eff5fd893" />


The application is connected to MySQL database **jwtauth** and the required tables are available.

---

## 🔑 Insert User Credentials

<img width="647" height="101" alt="Screenshot 2026-03-11 100717" src="https://github.com/user-attachments/assets/43432b6e-f23a-4c68-a847-e9773a98e080" />


User data is inserted into the database.

---


## 📋 Users Table Data

<img width="445" height="227" alt="Screenshot 2026-03-11 095014" src="https://github.com/user-attachments/assets/7874cdb4-bef4-4aeb-9ced-f78abc7c229a" />



User credentials are stored in the database and fetched successfully.

---



## 🔐 Generate JWT Token (POST)

<img width="1261" height="736" alt="Screenshot 2026-03-11 094958" src="https://github.com/user-attachments/assets/c22c963d-d88d-41fc-8256-093ac7b00f06" />

### Endpoint
POST http://localhost:8080/api/login

### Request Body (x-www-form-urlencoded)
username=ram  
password=1234  

### Response
JWT token is generated successfully.

---

## 🔓 Access Secured API (GET)

<img width="1260" height="770" alt="Screenshot 2026-03-11 094929" src="https://github.com/user-attachments/assets/0f3df3c6-d267-425a-b1f6-38681d2b2473" />


### Header
Authorization: Bearer <JWT_TOKEN>

### Response
Hello! JWT Authentication Successful

---

## 🔗 API Endpoints

| Method | Endpoint        | Description                     |
|--------|---------------|---------------------------------|
| POST   | /api/login     | Generate JWT token              |
| GET    | /api/hello     | Access secured API              |

---

## ✅ Result
JWT authentication was successfully implemented. The user was able to log in, generate a token, and access secured endpoints.

---

## 📚 Learning Outcome
- Implemented JWT authentication using Spring Security  
- Understood token-based authorization  
- Secured REST APIs using Bearer Token  
- Learned how authentication flow works  
- Tested APIs using Postman  

---
