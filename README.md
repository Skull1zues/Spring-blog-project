# Spring-blog-project

A simple Blog API built with Spring — allows users to register, authenticate, create posts, and post comments. The project includes user authentication and authorization.

## Features
- RESTful API for posts and comments
- User registration and authentication
- Authorization for protected actions (create/edit/delete)
- Commenting on posts via API
- Input validation and basic error handling

## Technologies
- Java (17+ recommended)
- Spring Boot (Web, Security, Data JPA)
- Persistence: H2 (for development) or relational DB (Postgres/MySQL) in production
- Build: Maven or Gradle

## Getting started

Prerequisites:
- Java 17+ installed
- Maven or Gradle installed
- (Optional) PostgreSQL / MySQL if not using H2

Run with Maven:
```bash
./mvnw spring-boot:run
# or
mvn spring-boot:run
```

Run with Gradle:
```bash
./gradlew bootRun
# or
gradle bootRun
```

## Configuration
Configure database and other settings in `src/main/resources/application.properties` (or `application.yml`). For quick local development you can use the embedded H2 database. To use a production DB, set the datasource URL, username, and password accordingly.

## Typical endpoints (adjust to your implementation)
- POST /api/auth/register — register a new user
- POST /api/auth/login — authenticate and receive a token
- GET /api/posts — list posts
- GET /api/posts/{id} — get a post
- POST /api/posts — create a post (authenticated)
- PUT /api/posts/{id} — update a post (authorized)
- DELETE /api/posts/{id} — delete a post (authorized)
- POST /api/posts/{id}/comments — add a comment to a post (authenticated)
- GET /api/posts/{id}/comments — list comments for a post

Note: Endpoint paths and auth method (JWT, sessions, etc.) depend on the current code — update these examples to match your controllers and security configuration.

## Running tests
Run unit and integration tests with:
```bash
./mvnw test
# or
mvn test


## Development tips
- Use application-dev.properties (or a Spring profile) for local settings.
- Enable H2 console for quick DB inspection (if H2 is used).
- Add Postman/HTTP collection for easier API testing.

## Contributing
PRs are welcome. Please open issues for bug reports or feature requests.

## License
Add your license here (e.g., MIT).
