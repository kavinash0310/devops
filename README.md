# DevOps Assignment — Spring Boot and Docker

A small Java 17 and Spring Boot starter used to practice packaging a Java application in a Docker image. The repository includes a Dockerfile that runs the built JAR.

## Build and run

Requirements: Java 17, Maven, and Docker.

```bash
mvn clean package
docker build -t devops-assignment .
docker run --rm -p 8080:8080 devops-assignment
```

The Dockerfile expects the packaged JAR at `target/DevOpsAssignment-0.0.1-SNAPSHOT.jar`. Build the project before building the image.

## Project contents

- `src/main/java` — Spring Boot application
- `Dockerfile` — container image definition
- `pom.xml` — Maven build

This is a basic containerization exercise; it does not yet include a deployment pipeline or production operations setup.
