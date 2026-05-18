# Product Management System Backend

This is a Spring Boot backend project for a Product Management System. It provides REST APIs for product CRUD operations, user registration, login workflow, and MySQL database persistence using Spring Data JPA.

## Tech Stack

- Java
- Spring Boot
- Spring Web
- Spring Data JPA
- Hibernate
- MySQL
- Maven

## Features

- Create, read, update, and delete products
- Retrieve all products
- Retrieve a product by ID
- User registration workflow
- User login workflow
- MySQL database persistence
- Repository-based database access using JpaRepository

## Backend Structure

```text
ProductApplication
        ↓
Controller
        ↓
Service
        ↓
Repository
        ↓
Model / Entity
        ↓
Database
```

## Main Components

### ProductController

Handles REST API requests for product operations.

### Product

Represents the product entity mapped to the database table.

### ProductRepo

Provides database access for product records using JpaRepository.

### RegistrationController

Handles user registration, login, update, delete, and user lookup APIs.

### RegistrationService

Handles user-related business logic.

### RegistrationRepo

Provides database access for user registration records and custom login lookup methods.

## API Endpoints

### Product APIs

```text
GET     /product/prd
POST    /product/prd
GET     /product/prd/{id}
PUT     /product/prd/{id}
DELETE  /product/prd/{id}
```

### User APIs

```text
POST    /all/users
GET     /all/users
POST    /all/userLogin
GET     /all/user/{id}
PUT     /all/user/{id}
PATCH   /all/user/{id}
DELETE  /all/user/{id}
```

## Database

The project uses MySQL with Spring Data JPA and Hibernate for database persistence.

Main entities:

- Product
- Registration

## Notes

This repository currently contains the Spring Boot backend only. An Angular frontend can be connected later through REST API integration.

## Future Improvements

- Add a ProductService layer between ProductController and ProductRepo
- Add Spring Security
- Hash passwords using BCrypt
- Add stronger validation
- Add Swagger/OpenAPI documentation
- Add Docker support
