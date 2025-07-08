# AtualizaCliente API

This repository contains the backend for the AtualizaCliente platform, responsible for managing clients, projects, updates, and email notifications.

## Technologies

- Java 17
- Spring Boot
- Spring Data JPA
- PostgreSQL (default, but can be adapted to other relational databases)
- File storage via S3 (compatible)

## Features

- User registration and authentication
- Client management
- Project and project update management
- Attachment upload and download (S3 storage)
- Email notifications (SMTP)
- Access control via tokens

## Project Structure

- `src/main/java`: Main source code (controllers, services, repositories, entities)
- `src/main/resources`: Configurations, email templates, SQL scripts
- `src/test/java`: Automated tests

## How to Run Locally

1. **Prerequisites**:
   - Java 17+
   - Maven
   - PostgreSQL (or another configured relational database)
2. **Configuration**:
   - Edit the `src/main/resources/application.properties` file with your database credentials and email/S3 settings.
3. **Build and Run**:
   ```sh
   ./mvnw spring-boot:run
   ```
   The backend will be available at `http://localhost:8080`.

## Main Endpoints

- `/clientes` — Client management
- `/projetos` — Project and update management
- `/auth` — User authentication
- `/configuracao-email` — SMTP configuration
- `/configuracao-s3` — S3 storage configuration

## Notes

- The system is designed for self-hosted use and does not support multi-company.
- For usage details and payload examples, see the frontend documentation or the project's [main README](../../README.md).

---