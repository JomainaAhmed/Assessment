# Advanced Java Assessments (Week 1–4)

## Overview
This repository contains the implementation of **four weekly backend development assessments** focusing on **Spring Framework, Spring Boot, REST APIs, and Microservices architecture**.

Each assessment demonstrates backend development concepts such as **data persistence, REST API design, security, caching, file handling, and microservice communication**.

---

# Week 1 – TechEdge University Management System

## Description
The **TechEdge University System** manages departments and students within a university.  
The system replaces manual spreadsheet management with a **Java application using Spring Core and Hibernate (JPA)** for efficient academic data management.

## Technologies Used
- Java
- Spring Core
- Hibernate (JPA)
- Maven
- PostgreSQL
- Ehcache

## Entities

### Department
- id
- name
- students

### Student
- id
- name
- email
- department

### Relationship
```
One Department -> Many Students  
Many Students -> One Department
```

## Features
- Add new departments
- Add students
- Assign students to departments
- View students by department
- Update student details
- Delete students or departments
- Hibernate Lazy Loading
- Second-Level Cache using Ehcache

## Core Operations
- `addDepartment()`
- `addStudent()`
- `assignStudentToDepartment()`
- `getDepartmentById()`
- `viewStudentsByDepartment()`
- `updateStudent()`
- `deleteStudent()`
- `deleteDepartment()`

---

# Week 2 – Spring Boot Employee API

## Description
This assessment involves building a **RESTful Employee Management API using Spring Boot**.  
The system allows administrators to manage employee records using REST endpoints.

## Technologies Used
- Spring Boot
- Spring Data JPA
- REST APIs
- Maven
- PostgreSQL

## Employee Entity

- id
- name
- phone
- email
- salary
- department

## API Endpoints

| Method | Endpoint | Description |
|------|------|------|
| POST | `/api/employees` | Add new employee |
| GET | `/api/employees` | Retrieve all employees |
| GET | `/api/employees?id=10` | Retrieve employee by ID |
| DELETE | `/api/employees?id=10` | Delete employee |
| GET | `/api/employees/search?name=Ravi` | Search by name |
| GET | `/api/employees/search?department=Testing` | Search by department |
| GET | `/api/employees/search?phone=9876543210` | Search by phone |
| GET | `/api/employees/search?email=ravi@gmail.com` | Search by email |

## Optional Features
- Update employee details
- Search employees within salary range
- Find employee with maximum salary
- Find employee with minimum salary

---

# Week 3 – Student Management System (SMS)

## Description
The **Student Management System** is a Spring Boot REST API designed to manage student records securely.  
It supports advanced features such as **file upload, pagination, caching, security, and monitoring**.

## Technologies Used
- Spring Boot
- Spring Data JPA
- Spring Security
- Spring Cache
- Multipart File Upload
- Spring Boot Actuator
- PostgreSQL

## Student Entity

| Field | Description |
|------|------|
| id | Student ID |
| name | Student name |
| email | Email |
| course | Course enrolled |
| marks | Student marks |
| profileImage | Stored as binary |
| assignmentFile | Stored as binary |

## Features

### CRUD Operations
- Create student
- Retrieve student by ID
- Retrieve all students
- Update student details
- Delete student

### Pagination and Sorting
Retrieve student records in paginated and sorted format.

### File Handling
- Upload student profile image
- Upload student assignment file
- Download stored files

### Security Features
- Spring Security Basic Authentication
- Password encryption
- Role-based authorization

### Roles
- ADMIN
- USER

### Method-Level Security
- `@PreAuthorize`
- `@PostAuthorize`

### Additional Features
- Spring Cache for optimized performance
- CORS configuration
- Spring Boot Actuator for application monitoring

---

# Week 4 – BookStore Microservices System

## Description
The **BookStore System** is implemented using **Spring Cloud Microservices architecture**.  
The system consists of multiple services that communicate with each other using **Feign Client and Service Discovery**.

## Technologies Used
- Spring Boot
- Spring Cloud
- Eureka Server
- API Gateway
- OpenFeign
- Spring Data JPA
- PostgreSQL
- Maven

## Microservices Architecture

| Service | Port | Responsibility |
|------|------|------|
| Eureka Server | 8761 | Service registry |
| API Gateway | 8080 | Entry point for all client requests |
| Book Service | 8081 | Manage book catalog |
| Order Service | 8082 | Manage customer orders |

## Book Entity
- id
- title
- author
- isbn
- price
- quantity
- category

## Order Entity
- id
- bookId
- customerName
- quantity
- totalPrice
- status
- orderDate

## Key Features
- Service discovery using Eureka
- API Gateway for centralized routing
- Inter-service communication using Feign Client
- Separate databases for each service
- Full CRUD operations for books and orders
- Microservice architecture implementation

---

# How to Run the Projects

## Clone the Repository
```bash
git clone https://github.com/your-username/repository-name.git
```

## Navigate to the Project
```
cd repository-name
```

## Build the Project
```
mvn clean install
```

## Run the Application
```
mvn spring-boot:run
```

---

# Learning Outcomes

These assessments demonstrate practical knowledge of:

- Spring Framework
- Spring Boot application development
- REST API design
- Database integration with JPA
- File upload and handling
- Security implementation with Spring Security
- Pagination and caching
- Microservices architecture using Spring Cloud
- Service discovery and API gateway configuration

---

# Author
**Jomaina Ahmed**

Advanced Java Assessments Repository
