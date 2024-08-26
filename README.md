
# Micro-item-service-api

## Project Overview

The Micro Item Service API is a microservice developed using Java and Spring Boot. It is part of a microservices architecture, focusing on the management of items within a system. The service provides endpoints to perform CRUD (Create, Read, Update, Delete) operations for item entities, making it essential for any system that handles product or inventory management.

## Key Features

- **RESTful API**: Exposes endpoints for item management operations.
- **Microservices Architecture**: Designed to work seamlessly in a distributed system.
- **Spring Boot Integration**: Rapid development using the Spring Boot framework.
- **MySQL Database Support**: Stores item data with full relational support.

## Technologies Used

- **Java 17**
- **Spring Boot 3.x**
- **Spring Data JPA**
- **MySQL**
- **Maven**

## Project Structure and Code Explanation

1. **Controller Layer**:
   - Handles HTTP requests for item management.
   ```java
   @RestController
   @RequestMapping("/api/v1/items")
   public class ItemController {
       // CRUD endpoints for items
   }
   ```

2. **Service Layer**:
   - Contains business logic for item-related operations.
   ```java
   @Service
   public class ItemService {
       // Methods for creating, updating, retrieving, and deleting items
   }
   ```

3. **Repository Layer**:
   - Uses Spring Data JPA to interact with the MySQL database.
   ```java
   public interface ItemRepository extends JpaRepository<Item, Long> {
       // Repository for item data operations
   }
   ```

## How to Run the Project

1. Clone the repository:
   ```bash
   git clone https://github.com/MalingaBandara/Micro-item-service-api.git
   ```
2. Configure the MySQL database settings in `application.properties`.
3. Run the application using Maven:
   ```bash
   mvn spring-boot:run
   ```

## API Endpoints

- **POST /api/v1/items**: Create a new item.
- **GET /api/v1/items**: Retrieve all items.
- **GET /api/v1/items/{id}**: Retrieve a specific item by ID.
- **PUT /api/v1/items/{id}**: Update an item.
- **DELETE /api/v1/items/{id}**: Delete an item.

## Purpose and Future Enhancements

This microservice was developed as part of a learning project focused on microservices architecture and Spring Boot. Potential future improvements include adding search functionality, validation, and enhanced error handling.

## License

This project is licensed under the MIT License.
