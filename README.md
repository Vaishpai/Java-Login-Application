# MyWebApp - Simple Login Application

A simple Spring Boot 2.7.18 web application with login and registration functionality.

## Prerequisites

- Java 8+
- Maven 3.6+
- Apache Tomcat 8.5 or 9 (for deployment)

## Project Structure

```
Java-source/
├── pom.xml
└── src/main/
    ├── java/com/edwiki/prod/
    │   ├── MyWebAppApplication.java
    │   ├── ServletInitializer.java
    │   ├── HomeController.java
    │   ├── login.java
    │   └── register.java
    └── resources/
        ├── application.properties
        └── templates/
            ├── home.html
            ├── login.html
            └── register.html
```

## How to Build

```bash
mvn clean package
```

The WAR file is generated at `target/prod-0.0.1-SNAPSHOT.war`.

## How to Run (Standalone)

```bash
mvn spring-boot:run
```

The application starts on `http://localhost:8080`.

## Deploy to Tomcat

1. Build the WAR: `mvn clean package`
2. Copy `target/prod-0.0.1-SNAPSHOT.war` to Tomcat's `webapps/` folder
3. Start Tomcat: `./bin/startup.sh`
4. Access at `http://<server-ip>:8080/prod-0.0.1-SNAPSHOT/`

## Pages

| URL         | Description       |
|-------------|-------------------|
| `/`         | Home page         |
| `/login`    | Login page        |
| `/register` | Registration page |

## Login Credentials

- Username: `admin`
- Password: `password123`
