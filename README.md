# Retail Store Sample Application

## About the Application

The Retail Store Sample Application is a cloud-native microservices-based e-commerce demo application designed to demonstrate modern containerized application architecture.

It simulates a basic online retail store where users can:

- Browse products
- Add items to a shopping cart
- Checkout and place orders

This application is built purely for learning and demonstration purposes. It showcases how multiple independent services work together in a distributed system.

---

## Application Architecture (High-Level)

The application follows a Microservices Architecture pattern.

Each business capability is implemented as an independent service running in its own container.

### Core Services

- **UI Service**  
  The frontend web application that users interact with.

- **Catalog Service**  
  Provides product listing and product details.

- **Cart Service**  
  Manages shopping cart operations.

- **Checkout Service**  
  Coordinates the checkout workflow.

- **Orders Service**  
  Stores and retrieves order information.

---

### Architecture Diagram

![Application Architecture](architecture.png)

---

## Architecture Flow

1. User accesses the UI service.
2. UI communicates with backend services via REST APIs.
3. Cart and Catalog services handle user actions.
4. Checkout service orchestrates order placement.
5. Orders service persists order data.

All services communicate over HTTP and operate independently, enabling scalability and modular deployment.