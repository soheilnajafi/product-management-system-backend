# Product Management System Backend

This is a Spring Boot backend project for a Product Management System. It provides REST APIs for product CRUD operations, user registration, login workflows, and MySQL database persistence using Spring Data JPA and Hibernate.

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
- REST API integration support for an Angular frontend

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

## Configuration

The backend runs on port:

```properties
server.port=8090
```

Example database configuration:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/product_database?useSSL=false
spring.datasource.username=root
spring.datasource.password=your_password
spring.jpa.hibernate.ddl-auto=update
```

## Related Frontend Repository

This backend is designed to work with the Angular frontend repository:

```text
product-management-system-frontend
```

The Angular frontend connects to this backend using REST APIs such as:

```text
http://localhost:8090/product/prd
http://localhost:8090/all/users
http://localhost:8090/all/userLogin
```

## Notes

This repository contains the Spring Boot backend for the Product Management System. The frontend is maintained separately in the Product Management System frontend repository.

## Future Improvements

- Add a ProductService layer between ProductController and ProductRepo
- Add Spring Security
- Hash passwords using BCrypt
- Add stronger validation
- Add Swagger/OpenAPI documentation
- Add Docker support
