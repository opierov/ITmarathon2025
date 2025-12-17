## Application Composition

# Architecture

Overall [architecture diagram](docs/assets/architecture.png)

# Backend

Backed represented as a [.NET application](backend/README.md)

# Frontend

Frontend developed by [React](frontend/react/README.md) and [Angular](frontend/angular/README.md) teams

# Cloud Infrastructure

Provision the cloud infrastructure in AWS using [Terraform](docs/terraform-readme.md)

# Local Development

Bring up an easily manageable infrastructure for local development with [Docker Compose](docs/compose-readme.md)

# Test Automation

Test Automation represented as a [.NET Reqnroll/NUnit API/UI testing framework](testautomation/SecretNick.TestAutomation/README.md)

# Useful commands to run a project after setup

1. Building and running a project in Docker
```
docker compose down -v
docker system prune -a
docker compose build --no-cache
docker compose up
```
2. After launching the project, check if all links are working.
```
http://localhost:8081
http://localhost:8082
http://localhost:8080/swagger/index.html
```
3. Next, you can run autotests.
```
cd testautomation/SecretNick.TestAutomation/Tests 
dotnet test -c Angular_Headless --filter "TestCategory=api"
dotnet test -c React --filter "TestCategory=ui"
```
4. To stop and restart Docker
```
docker-compose stop
docker-compose start
```
if you have several, you can start or stop a specific one
```
docker-compose -p myproject stop
docker-compose -p myproject start
```