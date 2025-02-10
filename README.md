# Spring Gradle REST API Exercise 🌱

## Description

This project demonstrates a basic Spring Boot REST API implementation with Gradle. It includes a simple Hello World controller with two endpoints that handle GET requests with different parameter passing methods (RequestParam and PathVariable).

## Technical Requirements

- Java JDK 11 or higher
- Gradle
- Spring Boot (latest stable version)
- IDE
- Postman for testing

## Configuration

### Dependencies

- Spring Boot DevTools
- Spring Web

### Application Properties

The application runs on port 9001:
```properties
server.port=9001
```

## API Endpoints

### 1. Hello World with RequestParam

```http
GET /HelloWorld
GET /HelloWorld?nom=YourName
```

- Default value for "name" parameter: "UNKNOWN"
- Returns: "Hello, {name}. You are executing a Gradle project!"

### 2. Hello World with PathVariable

```http
GET /HelloWorld2
GET /HelloWorld2/{name}
```

- Optional "name" parameter
- Returns: "Hello again, {name}. You are executing a Gradle project!"

## Testing with Postman

### Environment Setup

1. Create two environments:
   - Project Maven
   - Project Gradle

2. Configure variables for each environment:
   - Server: http://localhost
   - Port: 9000 (Maven) / 9001 (Gradle)

### Test Endpoints

Make sure the application is running, then test using Postman:

1. Using RequestParam:
   - `{{Server}}:{{Port}}/HelloWorld`
   - `{{Server}}:{{Port}}/HelloWorld?name=YourName`

2. Using PathVariable:
   - `{{Server}}:{{Port}}/HelloWorld2`
   - `{{Server}}:{{Port}}/HelloWorld2/YourName`
