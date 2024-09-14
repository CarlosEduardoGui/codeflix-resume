# Codeflix Project

The Codeflix project is a full-stack platform for managing and viewing movie content. It follows a microservices architecture, allowing for scalable and maintainable development. This project is composed of five main repositories that work together to provide a complete solution, covering front-end, back-end, core domain logic, and video encoding services.

---

## 1. [Codeflix](https://github.com/CarlosEduardoGui/codeflix)
The **Codeflix** repository provides the overall architecture and microservices framework for the project. It integrates multiple services, including back-end APIs, messaging systems, and authentication, to create a robust movie management system.

### Features:
- **Microservices Architecture**: Orchestrates various services like catalog, messaging, and user authentication.
- **Dockerized**: Uses Docker for containerizing each service, ensuring easy deployment.
- **Event-Driven**: Incorporates **RabbitMQ** and **Kafka** for asynchronous messaging between services.
- **Authentication**: Uses **Keycloak** for managing authentication and authorization.
- **Scalable**: Built to scale horizontally with the help of microservices, messaging queues, and containerization.

---

## 2. [Codeflix Client](https://github.com/CarlosEduardoGui/codeflix-client)
The **Codeflix Client** is the front-end of the platform, developed using **ReactJS**. It serves as the user interface, allowing users to interact with the movie catalog, search content, and manage movies.

### Features:
- **User Interface**: A responsive front-end for browsing, searching, and managing movie content.
- **Admin Dashboard**: Allows administrators to manage movies, categories, and genres.
- **API Integration**: Connects to the Codeflix API to fetch and manage data.
- **Responsive Design**: Optimized for both desktop and mobile users.

---

## 3. [FC.Codeflix.Catalog](https://github.com/CarlosEduardoGui/FC.Codeflix.Catalog)
The **FC.Codeflix.Catalog** repository focuses on the core business logic of managing the movie catalog. It is responsible for the domain-specific functionalities like managing categories, genres, cast members, and movies.

### Features:
- **Domain-Driven Design (DDD)**: Implements clear separation of concerns following DDD principles.
- **Clean Architecture**: Ensures scalability and maintainability by using clean code architecture.
- **Test-Driven Development (TDD)**: Unit tests are used to guarantee the proper functioning of the system.
- **Entity Framework Core**: Supports SQL databases for data persistence.

---

## 4. [FC.Codeflix.Catalog.Api](https://github.com/CarlosEduardoGui/FC.Codeflix.Catalog.Api)
The **FC.Codeflix.Catalog.Api** repository contains the back-end API that serves the movie catalog. It provides endpoints for managing and accessing content like movies, categories, and genres.

### Features:
- **.NET Core**: Developed using .NET Core for performance and scalability.
- **GraphQL API**: Provides a GraphQL interface to enable efficient querying of data.
- **Elasticsearch Integration**: Fast search functionality powered by Elasticsearch.
- **Microservices**: Designed to work as part of the larger Codeflix microservices architecture.

---

## 5. [Microsservice Encoder Video](https://github.com/CarlosEduardoGui/microsservice-encoder-video)
The **Microsservice Encoder Video** repository is responsible for the video encoding service of the Codeflix platform. It handles video processing tasks such as encoding and preparing videos for streaming or playback.

### Features:
- **Video Encoding**: Converts uploaded videos into multiple formats and resolutions to support different streaming devices and bandwidth conditions.
- **Event-Driven**: Listens for events (such as new video uploads) and triggers the encoding process using a message queue (RabbitMQ or Kafka).
- **Dockerized**: Uses Docker for containerized execution, ensuring consistency across environments.
- **FFmpeg Integration**: Leverages **FFmpeg** for encoding videos into the required formats efficiently.

---

## Technologies Used Across the Platform:
- **Docker**: All services are containerized for easy deployment and scaling.
- **RabbitMQ/Kafka**: Used for messaging between microservices in an event-driven architecture.
- **Keycloak**: Manages user authentication and authorization.
- **CI/CD**: Continuous integration and deployment pipelines ensure automated testing and deployment.
- **FFmpeg**: Integrated into the video encoding service for efficient video processing.

---

### How to Get Started:
1. **Clone the Repositories**:
   ```bash
   git clone https://github.com/CarlosEduardoGui/codeflix
   git clone https://github.com/CarlosEduardoGui/codeflix-client
   git clone https://github.com/CarlosEduardoGui/FC.Codeflix.Catalog
   git clone https://github.com/CarlosEduardoGui/FC.Codeflix.Catalog.Api
   git clone https://github.com/CarlosEduardoGui/microsservice-encoder-video
  

2. Run the Docker Containers: Each repository comes with a ```docker-compose.yml``` file. Use Docker Compose to start up the services:
   ```bash
   docker-compose up
   ```
3. **Access the Client**: Once the services are running, you can access the **Codeflix Client** via your browser to interact with the movie catalog.

---

### System Design
![PlantUML's solution](https://github.com/CarlosEduardoGui/FC.Codeflix.Catalog/assets/43711772/d8979056-d3f8-487b-acd7-27ebe8aee140)
---

### License:
This project is licensed under the MIT License.

---

### Contributors:
 - Carlos Eduardo Guimarães
