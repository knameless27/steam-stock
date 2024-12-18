# todo.md - Inventory Management System with Stock Forecasting and Redis Caching

## Project Description

Create a desktop application in **C#** using **.NET Framework** that allows for managing inventory in a warehouse environment. The application should include functions for managing products, categories, suppliers, and warehouses, in addition to detailed reports on the current inventory, incoming and outgoing products. Implement forecasting functionalities using simple algorithms to predict future stock needs based on historical product movement data.

### Key Features:
- **Inventory CRUD Operations**: Create, read, update, and delete products, categories, and suppliers.
- **User and Permission Management**: Implement basic authentication and role-based permissions where only certain users can add or modify information.
- **Stock Forecasting**: Implement a basic forecasting model (like moving average or simple linear regression) to predict the demand for products based on past sales.
- **Real-Time Reporting**: Design real-time reports with SQL to show critical inventory and products that may run out soon. Use Redis to cache critical queries such as low-stock products or daily/weekly sales reports to optimize performance.
- **Redis Integration for Notifications**: Implement Redis for managing a real-time notification system that alerts users of low-stock products or pending orders using a messaging channel for immediate alerts.
- **Synchronization and Persistence of Redis**: Ensure Redis data is synchronized with SQL in case of Redis restarts or failures. This can be done by setting up periodic backups or using data update patterns.
- **Git Integration**: Collaborate on the project using Git with good branching and version control practices. Document changes with clear commits and manage team reviews.

---

## Task Distribution

### Tasks for Andrés

1. **Initial Setup and Project Structure**
    - [ ] Set up the development environment (SQL Server, Redis).

2. **CRUD Implementation**
    - [ ] Develop CRUD operations for products, categories, and suppliers in **C#**.
    - [ ] Create basic interfaces for data input and display using **WinForms** or **WPF**.
    - [ ] Design the SQL database required for these operations.

3. **User and Permission Management**
    - [ ] Design and implement an authentication system with roles and permissions.
    - [ ] Develop the login module in **C#**.

4. **Redis and Synchronization**
    - [ ] Implement Redis integration for caching critical data.
    - [ ] Design logic to synchronize Redis with SQL using periodic update patterns.
    - [ ] Configure Redis persistence (AOF or RDB).

5. **Testing and CI/CD**
    - [ ] Configure Docker for the project.
    - [ ] Set up GitHub Actions for CI/CD:
        - [ ] Automated unit testing.
        - [ ] Application deployment to a cloud environment.
    - [ ] Create the Dockerfile to containerize the application.

---

### Tasks for Juan

1. **Introduction to C# and .NET**
    - [ ] Familiarize yourself with the basics of **C#** syntax and the **.NET Framework** ecosystem.
    - [ ] Review the initial project setup by Andrés to understand its structure.

2. **User Interface**
    - [ ] Create basic forms to manage products, categories, and suppliers using **WinForms** or **WPF** (guided by the initial structure).
    - [ ] Design reusable UI components like dropdowns, text boxes, and buttons.

3. **Forecasting Algorithms**
    - [ ] Research basic forecasting algorithms (moving average, simple linear regression).
    - [ ] Implement an initial version of the algorithm in **C#** (it can be very basic to start with).
    - [ ] Test the integration of the algorithm with Redis to temporarily store predictions.

4. **Notification System**
    - [ ] Implement a notification system using Redis Pub/Sub for low-stock alerts.
    - [ ] Design a simple popup window or log interface to display notifications.

5. **Testing**
    - [ ] Learn to write unit tests in C# using frameworks like **xUnit** or **NUnit**.
    - [ ] Write basic tests for the forecasting algorithms and notification system.

---

### Collaboration
1. **Reviews and Feedback**
    - Andrés reviews Juan’s contributions, helping to refine and optimize the implementation.
    - Juan assists by testing functionalities in different scenarios and validating the interface.

2. **Documentation**
    - Andrés documents the synchronization and Redis patterns.
    - Juan documents how to use the interfaces and forecasting algorithms.

---

### Progress and Learning
This division ensures Andrés leads the architecture and complex tasks while Juan tackles more manageable aspects like UI and basic algorithms. This approach ensures the project progresses while both acquire new skills.

---

## Features & Requirements

### 1. Inventory and Category CRUD Operations
- [ ] Create modules to manage products, allowing the creation, reading, updating, and deletion of products, categories, and suppliers.
- [ ] Implement form-based interfaces for managing data input and display.

### 2. User and Permission Management
- [ ] Implement a basic authentication system.
- [ ] Introduce role-based access where only authorized users can add or modify data.
- [ ] Design a login system and permissions table in SQL.

### 3. Stock Forecasting Module
- [ ] Implement a basic stock forecasting model (e.g., moving average or simple linear regression) to predict stock needs.
- [ ] Store forecasted results temporarily in Redis to improve performance when displaying reports.
- [ ] Create an algorithm in SQL or C# to calculate the predictions.

### 4. Real-Time Reporting
- [ ] Design real-time reports to display inventory status, critical products, and out-of-stock forecasts.
- [ ] Use advanced SQL queries and stored procedures to generate reports.
- [ ] Cache real-time reports in Redis for faster access.
- [ ] Use Redis to cache frequently accessed data such as low-stock products or daily/weekly sales.

### 5. Redis Integration for Notifications
- [ ] Use Redis for real-time notifications on low-stock levels or pending orders.
- [ ] Implement a messaging channel to send alerts to users whenever an important event occurs.
- [ ] Use Redis Pub/Sub for efficient and scalable message handling.

### 6. Synchronization and Persistence of Redis
- [ ] Ensure Redis data stays in sync with SQL.
- [ ] Set up Redis persistence options to ensure data isn’t lost in case of Redis failure (e.g., AOF or RDB snapshots).
- [ ] Implement periodic data synchronization from Redis to SQL.

### 7. Git Integration
- [ ] Set up a Git repository for version control.
- [ ] Collaborate using branches for features or bug fixes.
- [ ] Follow Git best practices: meaningful commit messages, merging with pull requests, and regular pushes.
- [ ] Review code changes via pull requests to maintain quality.

---

## Next Steps

1. **Set up the development environment**:
    - [ ] Install **Visual Studio** or **Visual Studio Code** with **C#** support.
    - [ ] Set up **SQL Server** or any SQL-compatible database for storing data.
    - [ ] Install **Redis** locally or set up a Redis server.

2. **Create initial project structure**:
    - [ ] Set up the solution in **Visual Studio**.
    - [ ] Create the main project files and structure the directories for models, views, controllers, and services.

3. **Develop the features iteratively**:
    - [ ] Implement the CRUD operations for inventory and categories.
    - [ ] Add user authentication and role management.
    - [ ] Develop the forecasting algorithm and integrate Redis caching.
    - [ ] Implement the reporting system with SQL and cache the results in Redis.
    - [ ] Set up the notification system using Redis Pub/Sub.

4. **Test each module**:
    - [ ] Write unit tests for the stock forecasting model and real-time notifications.
    - [ ] Test the Redis caching and data synchronization.

5. **Deploy**:
    - [ ] **Create Dockerfile** for the application to containerize it.
    - [ ] **Set up a CI/CD pipeline** using **GitHub Actions**:
        - [ ] Set up workflows for **build** and **test** processes.
        - [ ] Set up a workflow to **deploy to Azure** or another free cloud platform (e.g., **Render** or **Fly.io** for free deployment options).
        - [ ] Configure the deployment step to automatically deploy the app on successful builds.
    - [ ] **Dockerize** the application:
        - [ ] Create a Docker image for the application.
        - [ ] Push the image to a Docker registry (e.g., Docker Hub or GitHub Container Registry).
        - [ ] Set up the application on **Azure App Services** or **Render** for hosting with Docker support.
    - [ ] **Continuous Deployment**:
        - [ ] Ensure that the pipeline triggers deployments automatically to a staging or production environment after each commit.
    - [ ] Set up monitoring and logs on the deployment platform to track errors and performance metrics.

---

By following these steps and implementing the features outlined, this project will provide you with a full-fledged inventory management system that incorporates modern technologies and showcases a wide range of development skills.
