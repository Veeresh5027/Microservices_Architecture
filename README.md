
# Hotel Rating System - Microservices Architecture

[![Java](https://img.shields.io/badge/Java-17%2B-orange)](https://www.oracle.com/java/)
[![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.x-brightgreen)](https://spring.io/projects/spring-boot)
[![Spring Cloud](https://img.shields.io/badge/Spring%20Cloud-2022.x-blue)](https://spring.io/projects/spring-cloud)
[![Eureka](https://img.shields.io/badge/Service-Registry-yellow)](https://spring.io/projects/spring-cloud-netflix)

**Microservices_Architecture** is a distributed system designed for a Hotel Rating platform. It demonstrates the core patterns of microservices, including service discovery, inter-service communication, and centralized configuration management using the **Spring Cloud** ecosystem.

---

## 🏗️ System Architecture & Design Patterns

This project implements the following microservices patterns:

* **Service Discovery (Netflix Eureka):** All microservices register themselves with the `ServiceRegistry` for dynamic address resolution.
* **API Gateway:** A single entry point for all client requests, providing unified routing to underlying services.
* **Externalized Configuration:** Centralized management of application properties across environments using `ConfigServer`.
* **Inter-Service Communication:** Implemented using **Feign Client** and **RestTemplate** for synchronous communication.
* **Resilience (Optional/Future):** Structure ready for Circuit Breaker implementation (Resilience4j).

---

## 🛠️ Microservices Modules

| Service | Responsibility |
| :--- | :--- |
| **ServiceRegistry** | Eureka Server for service registration and discovery. |
| **ApiGateway** | Routes requests and handles cross-cutting concerns. |
| **ConfigServer** | Provides centralized configuration from a Git or local file system. |
| **UserService** | Manages user profiles and aggregates ratings/hotel info. |
| **HotelService** | Manages hotel information and inventory. |
| **RatingService** | Handles user ratings and feedback for specific hotels. |

---
