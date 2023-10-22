## Project Overview

The Quora Project is a modular application built on Spring Boot that simulates a simplified version of the Quora platform. It consists of several microservices, including the Quora app, Quora Moderator app, Eureka server for service discovery, an Admin app for managing users, and an API Gateway for routing requests to the appropriate services.

## Project Structure

The project is organized into several modules:

1. **Quora**
   - This is the main Quora application module, responsible for user registration, posting and answering questions, and user interactions.

2. **Quora Moderator App**
   - A module for managing user-reported content and ensuring community guidelines are followed.

3. **Eureka Server**
   - A service registry and discovery server that helps microservices locate and communicate with each other.

4. **Admin App**
   - An administrative application for managing users, their roles, and permissions.

5. **API Gateway**
   - A module that acts as an entry point for all client requests, routing them to the appropriate microservices.

## Prerequisites

Before you begin, ensure you have met the following requirements:

- Java Development Kit (JDK) 11 or higher.
- Maven build tool installed.
- Docker (for running services as containers).
- Your favorite IDE with Spring Boot support (e.g., IntelliJ IDEA, Eclipse).
- Git for version control (optional).

## Getting Started

Follow these steps to set up and run the Quora Project:

1. Clone the project from the repository:

   ```bash
   git clone <repository_url>
   ```

2. Build and package the individual modules using Maven.

   ```bash
   cd quora
   mvn clean install
   cd ../quora-moderator-app
   mvn clean install
   # Repeat for other modules
   ```

3. Start the Eureka Server first to enable service discovery:

   ```bash
   cd eureka-server
   mvn spring-boot:run
   ```

4. Launch the individual modules in separate terminals:

   ```bash
   cd quora
   mvn spring-boot:run
   # Repeat for other modules
   ```

5. Access the Quora app via the API Gateway: `http://localhost:8080/api/quora`

6. Access the Eureka Server dashboard: `http://localhost:8761`

## Configuration

Each module may have its own configuration files, including database settings and service ports. Review the `application.properties` or `application.yml` files within each module to customize configuration settings.

## Documentation

- **API Documentation:** Detailed API documentation for each module can be found in the respective module's README or on the API Gateway.

## Contact

- [Siddhant Kamat](mailto:siddhantkamat892@gmail.com)
