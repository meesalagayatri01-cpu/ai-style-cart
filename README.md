# AI Style Cart — Spring Boot Backend

Starter REST API for the AI Style Cart fashion shopping frontend.

## Requirements
- Java 21
- Maven 3.9+
- Optional: MySQL 8

## Run locally
From this `backend` folder:
```bash
mvn spring-boot:run
```
API starts at `http://localhost:8080`.

## Endpoints
- `GET /api/health` — status check
- `POST /api/style-advice` — demo outfit suggestion
  ```json
  {"occasion":"college fest"}
  ```
- `POST /api/orders` — validates and returns a demo order number. It does **not** store orders in a database or collect payment.

## MySQL
A MySQL database is not required for the demo endpoints. To enable MySQL, create database `ai_style_cart`, set `DB_URL`, `DB_USERNAME`, and `DB_PASSWORD` as environment variables, then uncomment the datasource/JPA lines in `src/main/resources/application.properties`. Database entities and persistent order storage still need to be implemented before claiming orders are saved.

## Important
The style advice is a rule-based demo, not a live AI model. Add a server-side AI provider integration to enable real AI suggestions. Never commit API keys or passwords.
