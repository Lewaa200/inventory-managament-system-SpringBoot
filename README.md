# Inventory Management System

This project consists of two applications: a JavaFX frontend for user interaction and a Spring Boot backend for managing inventory data through a RESTful API.

## Table of Contents
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Architecture](#architecture)
- [Screenshots](#screenshots)
- [Installation](#installation)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)
- [Acknowledgements](#acknowledgements)

## Features
- **Frontend (JavaFX)**
  - User-friendly graphical interface
  - Add, update, delete, and search inventory items

- **Backend (Spring Boot)**
  - RESTful API for inventory management
  - CRUD operations
  - Database integration with JPA/Hibernate

## Technologies Used
- **Frontend**
  - Java
  - JavaFX
  - FXML

- **Backend**
  - Java
  - Spring Boot
  - Spring Data JPA
  - Hibernate
  - MySQL 
  - Maven

## Architecture
- **JavaFX Frontend**: Handles the user interface and interacts with the backend API.
- **Spring Boot Backend**: Provides RESTful services to manage inventory data, with database integration for persistence.

## Screenshots


## Installation

### Prerequisites
- Java Development Kit (JDK) 11 or later
- Maven
- MySQL (or another relational database)

### Backend Setup (Spring Boot)
1. **Clone the Repository**:
    ```sh
    git clone https://github.com/yourusername/inventory-management-system.git
    ```

2. **Navigate to the Backend Directory**:
    ```sh
    cd inventory-management-system/backend
    ```

3. **Configure the Database**:
   - Update the `application.properties` file (located in `src/main/resources`) with your database configuration:
     ```properties
     spring.datasource.url=jdbc:mysql://localhost:3306/inventory_db
     spring.datasource.username=your_db_username
     spring.datasource.password=your_db_password
     spring.jpa.hibernate.ddl-auto=update
     ```

4. **Build and Run the Backend Application**:
    ```sh
    mvn spring-boot:run
    ```

### Frontend Setup (JavaFX)
1. **Navigate to the Frontend Directory**:
    ```sh
    cd inventory-management-system/frontend
    ```

2. **Open the Project in Your IDE**:
   - Open your favorite IDE (like IntelliJ IDEA, Eclipse, or NetBeans).
   - Import the project as a Maven project if applicable.

3. **Run the Frontend Application**:
   - Locate the `Main` class and run it.

## Usage

### Running the Applications
1. **Start the Backend**:
   - Ensure the backend application is running (see Backend Setup).
2. **Start the Frontend**:
   - Run the JavaFX application (see Frontend Setup).

### Interacting with the API
Use tools like Postman or curl to test the backend API endpoints.

#### Example API Endpoints
- **GET /api/items**: Retrieve all inventory items
- **POST /api/items**: Add a new inventory item
- **PUT /api/items/{id}**: Update an existing inventory item
- **DELETE /api/items/{id}**: Delete an inventory item

#### Example curl Commands
1. **Retrieve All Items**:
    ```sh
    curl -X GET http://localhost:8080/api/items
    ```

2. **Add a New Item**:
    ```sh
    curl -X POST http://localhost:8080/api/items -H "Content-Type: application/json" -d '{"name":"ItemName","quantity":10,"price":100.0}'
    ```

3. **Update an Item**:
    ```sh
    curl -X PUT http://localhost:8080/api/items/1 -H "Content-Type: application/json" -d '{"name":"UpdatedItemName","quantity":20,"price":200.0}'
    ```

4. **Delete an Item**:
    ```sh
    curl -X DELETE http://localhost:8080/api/items/1
    ```

## Contributing
Contributions are welcome! Please fork the repository and create a pull request with your changes.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.


## Acknowledgements
- Special thanks to the Spring Boot and JavaFX communities for their resources and support.
