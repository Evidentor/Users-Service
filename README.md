# Users-Service

## About
The Users Service manages user-related data and access control. 
It stores core user information such as first name, last name, 
and email, as well as each user's room access permissions. 
This service provides the foundation for identity and authorization 
across the system.

## System Requirements

- Java 21
- Apache Maven 3.9.9
- Docker (if running the service within the Docker container)

## Configuration

### Database
Configure database connection in `application.yaml` file:
```yaml
spring:
  datasource:
    url: jdbc:postgresql://localhost:5432/evidentor
    driverClassName: org.postgresql.Driver
    username: postgres
    password: postgres
```

## How to Install?

### 1. Clone the repository
```shell
git clone https://github.com/Evidentor/Users-Service.git
cd Users-Service
```

### 2. Install dependencies
```shell
mvn clean install
```

## How to Run?

### Run with java
```shell
java --enable-preview -jar target/*.jar
```

### Run with docker
#### 1. Build the docker image
```shell
docker build -t users-service .
```

#### 2. Create the docker container
```shell
docker run -d --network host --name users-service users-service:latest
```

#### 3. Stop the docker container
```shell
docker stop users-service
```

#### 4. Start the docker container
```shell
docker start users-service
```

## How to Test?
```shell
mvn test
```
