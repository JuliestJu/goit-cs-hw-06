# Simple Web Application with Socket Server and MongoDB

## Overview

This project demonstrates a simple web application that interacts with a socket server and stores data in a MongoDB database. It includes:
- An HTTP server that serves web pages and handles form submissions.
- A socket server that processes data received from the HTTP server and stores it in MongoDB.
- Docker configuration to containerize the application and MongoDB for easy deployment.

## Features

1. **HTTP Server**:
   - Serves `index.html` as the home page.
   - Serves `message.html` for message submissions.
   - Handles static resources like CSS and images.
   - Returns a custom `error.html` page for 404 errors.
   - Listens on port 3000.

2. **Socket Server**:
   - Receives data from the HTTP server.
   - Processes the data and stores it in a MongoDB collection.
   - Listens on port 5001.

3. **MongoDB**:
   - Stores submitted messages with a timestamp.
   - Ensures data persistence using Docker volumes.

## Requirements

- Docker
- Docker Compose

## Setup Instructions

### 1. Clone the Repository

```sh
git clone <repository-url>
cd <repository-directory>
```

## 2. Create and Start the Containers

Use the provided `start.sh` script to build and start the Docker containers.

```sh
cd ./HW6
./start.sh
```

This script will:
- Check if Docker and Docker Compose are installed.
- Build and start the Docker containers using `docker-compose up --build`.

## 3. Access the Application

- Open your web browser and go to `http://localhost:3000` to access the home page.
- Navigate to `http://localhost:3000/message` to submit a message.

## Notes

- Ensure that Docker and Docker Compose are installed and running on your machine.
- The MongoDB data is persisted using Docker volumes, ensuring data is not lost when containers are stopped or removed.

## Troubleshooting

- If you encounter any issues, check the Docker logs for the containers using `docker logs <container-id>`.
- Ensure that all dependencies are correctly installed and that the containers are properly built and running.
```
