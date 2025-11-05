# Fullstack Docker Application

This is a full-stack application containerized with Docker, featuring a React frontend, Node.js/Express backend, and PostgreSQL database.

## Project Structure

```
fullstack-docker-app/
├── frontend/
│   ├── src/
│   ├── public/
│   ├── Dockerfile
│   └── package.json
├── backend/
│   ├── app.js
│   ├── package.json
│   └── Dockerfile
├── db-data/
├── docker-compose.yml
├── .env
└── README.md
```

## Prerequisites

- Docker
- Docker Compose

## Getting Started

1. Clone the repository:
```bash
git clone https://github.com/phantom-userrr/fulll-stack-docker-app.git
cd fulll-stack-docker-app
```

2. Start the application:
```bash
docker-compose up --build
```

3. Access the application:
- Frontend: http://localhost:3000
- Backend API: http://localhost:5001
- Database: localhost:5432

## Features

- React frontend with real-time backend connectivity
- Node.js/Express backend API
- PostgreSQL database with persistent storage
- Docker containerization for consistent development and deployment
- Environment variable configuration
- Volume persistence for database data

## Container Information

- Frontend Container: React application (port 3000)
- Backend Container: Node.js/Express API (port 5001)
- Database Container: PostgreSQL (port 5432)

## Data Persistence

The application uses Docker volumes for database persistence. The database data is stored in the `db-data` volume, ensuring data survives container restarts.

## Development

To run the application in development mode:

```bash
# Start all services
docker-compose up

# Stop all services
docker-compose stop

# Restart all services
docker-compose start

# Rebuild and start
docker-compose up --build
```

## Debugging

To view container logs:
```bash
docker logs fullstack-docker-app-frontend-1
docker logs fullstack-docker-app-backend-1
docker logs fullstack-docker-app-db-1
```

To access container shell:
```bash
# Frontend
docker exec -it fullstack-docker-app-frontend-1 sh

# Backend
docker exec -it fullstack-docker-app-backend-1 sh

# Database
docker exec -it fullstack-docker-app-db-1 bash
```