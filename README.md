# Spring Boot JPA Student Management API

A RESTful backend application built using **Spring Boot**, **Spring Data JPA**, and **MySQL** that performs CRUD operations on Student data.  
This project demonstrates clean architecture, JPA entity mapping, and REST API development.

---

## 📌 Project Overview

The **Student Management API** allows users to:
- Add new students
- Retrieve student details
- Update existing student records
- Delete students from the database

The application uses **Hibernate ORM** for database interaction and follows a layered architecture:
Controller → Service → Repository.

---

## 🚀 Features

- RESTful API design
- CRUD operations using Spring Data JPA
- Hibernate ORM for database mapping
- MySQL database integration
- Maven-based project structure
- Clean and modular code

---

## 🛠️ Tech Stack

| Technology | Description |
|---------|-------------|
| Java | Programming Language |
| Spring Boot | Backend Framework |
| Spring Data JPA | ORM & Data Access |
| Hibernate | JPA Implementation |
| MySQL | Relational Database |
| Maven | Dependency Management |
| Git & GitHub | Version Control |

---

## 📂 Project Structure

src/main/java/com/shubh/JPA_Project01
├── controller
│ └── StudentController.java
├── entity
│ └── Student.java
├── repository
│ └── StudentRepo.java
├── service
│ └── StudentService.java
└── JpaProject01Application.java

Copy code
src/main/resources
└── application.properties

yaml
Copy code

---

## ⚙️ Application Configuration

Update `application.properties` with your database credentials:

```properties
spring.application.name=JPA-Project01
server.port=8081

spring.datasource.url=jdbc:mysql://localhost:3306/studentdb1
spring.datasource.username=YOUR_USERNAME
spring.datasource.password=YOUR_PASSWORD
spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
spring.jpa.database-platform=org.hibernate.dialect.MySQL8Dialect
🗄️ Database Schema
The Student entity is mapped using JPA annotations.

java
Copy code
@Entity
public class Student {

    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Integer id;

    private String name;
    private String email;
    private Integer age;
}
Hibernate automatically creates and updates the table in MySQL.

📮 API Endpoints
HTTP Method	Endpoint	Description
POST	/students	Add new student
GET	/students	Get all students
GET	/students/{id}	Get student by ID
PUT	/students/{id}	Update student
DELETE	/students/{id}	Delete student

📥 Sample JSON Request
json
Copy code
{
  "name": "Anand Kumar",
  "email": "anand@gmail.com",
  "age": 20
}
▶️ How to Run the Project
Clone the repository

bash
Copy code
git clone https://github.com/Shubham-22127/JPA-Project01.git
Open the project in IntelliJ IDEA / Eclipse

Configure MySQL database

Run the application

bash
Copy code
mvn spring-boot:run
Access API at

arduino
Copy code
http://localhost:8081
🎯 Learning Outcomes
Understanding Spring Boot project architecture

Working with Spring Data JPA & Hibernate

Mapping Java entities to relational tables

Handling REST API requests

MySQL database integration

Git & GitHub workflow

🔮 Future Enhancements
Exception handling using @ControllerAdvice

Validation using @Valid

Pagination and sorting

Swagger API documentation

Security using Spring Security & JWT

👨‍💻 Author
Shubham Tripathi
B.Tech | Java Backend Developer

🔗 GitHub:
https://github.com/Shubham-22127
