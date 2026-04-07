# Node Docker App - First Docker Image

A simple Node.js application containerized with Docker.

## Description

This project demonstrates how to:
- Create a basic Node.js HTTP server
- Build a Docker image for a Node.js application
- Run a Node.js container with Docker

## Prerequisites

- [Docker Desktop](https://www.docker.com/products/docker-desktop/) installed and running
- Node.js (optional, for local development)

## Project Structure

```
node-docker-app/
├── app.js           # Main application file
├── package.json     # Node.js package configuration
├── Dockerfile       # Docker image build instructions
├── .dockerignore    # Files to exclude from Docker build
└── .gitignore       # Files to exclude from Git
```

## Quick Start

### 1. Build the Docker image

```bash
docker build -t node-docker-app .
```

### 2. Run the container

```bash
docker run -p 3000:3000 node-docker-app
```

### 3. Access the application

Open your browser and visit: [http://localhost:3000](http://localhost:3000)

You should see: **Hello, Docker!**

## Dockerfile Explanation

```dockerfile
FROM node:18-alpine     # Use lightweight Node.js Alpine image
WORKDIR /app            # Set working directory inside container
COPY package*.json ./   # Copy package files
RUN npm install         # Install dependencies
COPY . .                # Copy application code
EXPOSE 3000            # Expose port 3000
CMD ["node", "app.js"] # Start the application
```

## Screenshots Evidence

See the `screenshots/` folder for evidence of:
- Docker Desktop running
- Terminal commands execution
- Browser showing "Hello, Docker!" message

## Author

Created as part of Docker learning exercise.

## License

ISC