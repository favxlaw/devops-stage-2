# Dockerized Full Stack Web Application Deployment

This project demonstrates the deployment of a full-stack web application using Docker containers. The application consists of a React frontend, a FastAPI backend, and a PostgreSQL database. NGNIX is used as a reverse proxy to manage the routing of the frontend and backend services.

## Prerequisites

- Docker
- Docker Compose


## Getting Started

### 1. Fork and Clone the Repository

Fork this repository to your own GitHub account, then clone it to your local machine.

### 2. Write Dockerfiles
Write Dockerfiles to containerize both the React frontend and FastAPI backend. Ensure each service can be built and run locally in their respective containers.

### 3. Configure Nginx Proxy Manager
Configure Nginx to:

Serve the frontend and backend on the same host machine port (80).
Serve the frontend on the root (/).
Proxy /api on the backend to /api on the main domain.
Proxy /docs on the backend to /docs on the main domain.
Proxy /redoc on the backend to /redoc on the main domain.

### 4. Database Configuration
Configure the application to use a PostgreSQL database. Ensure the database is properly set up and connected.

Database Service in docker-compose.yml

### 5. Adminer Setup
Configure Adminer to run on port 8080. Ensure Adminer is accessible via the subdomain db.your-domain.com and is properly connected to the PostgreSQL database.

### 6. Proxy Manager Setup
Configure the proxy manager to run on port 8090. Ensure the proxy manager is accessible via the subdomain proxy.your-domain.com.

### 7. Cloud Deployment
Deploy your Dockerized application to a cloud provider (e.g., AWS EC2). Set up a domain for your application. If you don't have a domain, get a free subdomain from Afraid DNS. Configure HTTP to redirect to HTTPS and www to redirect to non-www.

### 8. Docker Compose Configuration
Create a docker-compose.yml file to define and run multi-container Docker applications.

```sh
git clone https://github.com/your-username/your-repo.git
cd your-repo


