# Student Management System

A Spring Boot web application for managing students, courses, and enrollments with authentication and a Thymeleaf-based UI.

## Project Overview

- Java 21
- Spring Boot 4.0.0
- Spring Data JPA
- Spring Security
- Thymeleaf
- MySQL database
- ModelMapper for DTO mapping
- Validation support and custom error handling

## Features

- User login and authentication
- Dashboard summary of students, courses, and enrollments
- Student management: add, edit, view, delete
- Course management: add, edit, view, delete
- Enrollment management: enroll students in courses and view enrolled students
- Thymeleaf templates for UI rendering

## Modules and Packages

- `com.cwm.studentmanagement.controller` - web controllers
- `com.cwm.studentmanagement.dto` - data transfer objects
- `com.cwm.studentmanagement.model` - JPA entity models
- `com.cwm.studentmanagement.repository` - Spring Data JPA repositories
- `com.cwm.studentmanagement.service` - business logic services
- `com.cwm.studentmanagement.config` - application configuration
- `src/main/resources/templates` - Thymeleaf views
- `src/main/resources/static/css` - stylesheet assets

## Prerequisites

- Java 21
- Maven
- MySQL server

## Setup and Run

1. Configure MySQL in `src/main/resources/application.properties`:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/student_mgmt_db?createDatabaseIfNotExist=true&serverTimezone=UTC
spring.datasource.username=root
spring.datasource.password=root
```

2. Build the application:

```bash
./mvnw clean package
```

3. Run the application:

```bash
./mvnw spring-boot:run
```

4. Open a browser and navigate to:

```text
http://localhost:8080
```

## Database

The application uses MySQL and will create or update the schema automatically using:

```properties
spring.jpa.hibernate.ddl-auto=update
```

## Notes

- If you need to change the database name or credentials, update `application.properties`.
- The default database name is `student_mgmt_db`.

## Project Structure

```
src/main/java/com/cwm/studentmanagement
  ├── config
  ├── controller
  ├── dto
  ├── exception
  ├── model
  ├── repository
  └── service
src/main/resources
  ├── templates
  └── static/css
```

## License

This project is provided as-is for learning and demonstration purposes.
