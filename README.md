# steam-stock: Inventory Management System with Stock Forecasting and Redis Caching

This project is an inventory management system designed for warehouses, developed in **C#** with **.NET Framework** and **SQL**. The application allows for the management of products, categories, suppliers, and real-time reports, incorporating a stock forecasting module. Additionally, **Redis** is used as a caching system to optimize performance and improve the response time for critical queries.

## Features

- **Full CRUD** for Inventory and Categories: Manage products, suppliers, and categories easily.
- **User and Role Management**: Authentication system with role-based permissions.
- **Stock Forecasting**: Implements a basic forecasting model (moving average or simple linear regression) to predict inventory needs based on historical data.
- **Real-time Reporting**: Query real-time inventory and predictions. Redis is used to cache intensive queries.
- **Real-time Notifications**: Notifies users about low stock levels or high-demand products.
- **Redis Caching**: Redis reduces response time and load on the SQL database.

## Technologies Used

- **C# and .NET Framework**: Main language and framework for developing the application.
- **SQL**: Database for storing products, categories, users, and historical movement records.
- **Redis**: Used for caching frequent data and handling real-time notifications.
- **Git**: Version control for collaboration between developers.

## Installation and Setup

1. **Clone the repository**:
   ```bash
   git clone https://github.com/your-username/steam-stock.git
   cd steam-stock
