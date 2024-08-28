# TMS Project - Docker Setup

This repository contains the Docker Compose configuration for running the microservices that make up the **TMS Project**. It orchestrates all the necessary services, including Kafka, Zookeeper, MySQL databases, and the microservices themselves.

## Project Repositories

The project consists of several separate repositories:

1. **[TMS Main Service](https://github.com/TaskManagerSystem/TMS-main-service)**: The main service for task and project management.
2. **[TMS Attachment Service](https://github.com/TaskManagerSystem/TMS-attachment-service)**: The service for managing attachments and integration with Dropbox.
3. **[TMS Notification Service](https://github.com/TaskManagerSystem/TMS-notification-service)**: The service for sending notifications via email and Telegram.
4. **[TMS Common DTO](https://github.com/TaskManagerSystem/TMS-common-dto)**: A shared DTO library used across all microservices.

## Usage

### 1. Clone the Repositories

Clone all the necessary repositories to your local machine:

```bash
git clone https://github.com/TaskManagerSystem/TMS-docker-compose.git
git clone https://github.com/TaskManagerSystem/TMS-main-service.git
git clone https://github.com/TaskManagerSystem/TMS-attachment-service.git
git clone https://github.com/TaskManagerSystem/TMS-notification-service.git
git clone https://github.com/TaskManagerSystem/TMS-common-dto.git
```

### 2. Configure Environment Variables

Before starting the containers, create a '.env' file based on the '.env.example' file and fill it with the appropriate values:

```bash
cp .env.example .env
```

Fill in the '.env' file with the required values.

### 3. Start the Containers

To start all services, use the following command:

```bash
docker-compose up -d
```

This will launch all the microservices, Kafka, Zookeeper, and MySQL databases.

### 4. Stop the Containers

To stop all running services:

```bash
docker-compose down
```