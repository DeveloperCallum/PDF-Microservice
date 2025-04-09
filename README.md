# Docker Compose Environment Setup & Usage

## Prerequisites
Before you begin, ensure you have the following installed:
- [Docker](https://docs.docker.com/get-docker/)
- [Docker Compose](https://docs.docker.com/compose/install/)
- [IntelliJ IDEA](https://www.jetbrains.com/idea/download/)
- [Maven](https://maven.apache.org/install.html)

## Setup

### 1. Clone the Repository
```bash
git clone https://github.com/DeveloperCallum/PDF-Microservice
cd <your-project-directory>
```

### 2. Build the Image Service
Before building the Docker containers, run the following Maven command to prepare the image service:
```bash
cd <image-service-directory>
mvn clean compile package
```

### 3. Create IntelliJ Configurations
Set up IntelliJ configurations as needed for smooth development and debugging.

### 4. Start the Docker Environment
Use Docker Compose to build and start the containers:
```bash
docker-compose up --build
```

### 5. Verify Running Containers
Check if all services are running:
```bash
docker ps
```

### 6. Stop the Environment
To stop the containers without removing them:
```bash
docker-compose down
```
If you want to remove all containers and networks:
```bash
docker-compose down --volumes
```

## Notes
- Ensure that the image service is successfully built with Maven before starting Docker Compose.
- Modify `docker-compose.yml` as needed to match your environment.
- Logs can be checked using `docker-compose logs -f <service-name>`.

---

This `README.md` is structured for clarity and ease of use. Let me know if you'd like to refine any sections! 🚀
