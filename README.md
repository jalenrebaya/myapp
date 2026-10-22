# My Docker App

## Project Description

My Docker App is a containerized web application built using React, a .NET Web API, and PostgreSQL. Docker Compose is used to run and manage the application services together.

## Technologies Used

- **Frontend:** React and Vite
- **Backend:** .NET 10 Web API
- **Database:** PostgreSQL 16
- **Web Server:** Nginx
- **Containerization:** Docker and Docker Compose
- **Version Control:** Git and GitHub

## Project Structure

```text
myapp/
├── api/
│   ├── Dockerfile
│   ├── Program.cs
│   └── api.csproj
├── web/
│   ├── Dockerfile
│   ├── src/
│   └── package.json
├── docker-compose.yml
└── README.md
```

## Prerequisites

Before running the project, install:

- [Docker Desktop](https://www.docker.com/products/docker-desktop/)
- Git (optional, for cloning the repository)

## How to Run the Application

1. Clone the repository:

   ```bash
   git clone https://github.com/jalenrebaya/myapp.git
   ```

2. Open the project folder:

   ```bash
   cd myapp
   ```

3. Build and start the containers:

   ```bash
   docker compose up --build -d
   ```

4. Check the running containers:

   ```bash
   docker compose ps
   ```

## Application URLs

| Service | URL |
|---|---|
| Frontend | http://localhost:3000 |
| Backend API | http://localhost:5000/api/message |
| PostgreSQL | Available internally to the Docker network |

## Docker Services

The project uses three services:

- **Web:** Serves the React frontend using Nginx.
- **API:** Handles API requests using ASP.NET Core.
- **Database:** Runs PostgreSQL for database services.

Docker Compose manages the services, their configuration, and the database volume.

## Stop the Application

To stop the running containers, execute:

```bash
docker compose down
```

To stop the containers and remove the database volume, use:

```bash
docker compose down -v
```

**Warning:** The second command deletes the persistent database volume and its stored data.

## Author

**Jallyn Ribaya**

GitHub: [@jalenrebaya](https://github.com/jalenrebaya)
