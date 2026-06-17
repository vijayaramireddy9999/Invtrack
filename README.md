# 🚀 InvTrack - Inventory Management System

![Java](https://img.shields.io/badge/Java-17-orange)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-4.1-green)
![React](https://img.shields.io/badge/React-Frontend-blue)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-Database-blue)
![Docker](https://img.shields.io/badge/Docker-Containerization-blue)
![JWT](https://img.shields.io/badge/JWT-Security-red)

## 📖 Overview

InvTrack is a Full-Stack Inventory Management System built using **Java 17, Spring Boot, Spring Security, JWT Authentication, PostgreSQL, React.js, Docker, and Swagger OpenAPI**.

The system enables organizations to manage products, suppliers, categories, inventory transactions, stock movement tracking, low-stock monitoring, and dashboard analytics through a secure and scalable architecture.

---

# ✨ Features

## 🔐 Authentication & Authorization

* JWT Authentication
* Spring Security Integration
* Protected REST APIs
* Token-Based Authorization

## 📦 Product Management

* Create Product
* Update Product
* Delete Product
* Search Products
* Pagination Support
* Category Mapping
* Supplier Mapping

## 📂 Category Management

* Create Category
* Update Category
* Delete Category
* View Categories

## 🏢 Supplier Management

* Create Supplier
* Update Supplier
* Delete Supplier
* Supplier Management Dashboard

## 📊 Dashboard Analytics

* Total Products
* Total Categories
* Total Suppliers
* Total Stock
* Low Stock Monitoring
* Products by Category Chart
* Supplier Distribution Chart
* Recent Inventory Transactions

## 📈 Inventory Operations

* Stock In
* Stock Out
* Inventory Transaction Tracking
* Transaction History
* Inventory Audit Trail

## 📖 API Documentation

* Swagger OpenAPI Integration

---

# 🏗️ System Architecture

```text
┌──────────────────────────────┐
│       React Frontend         │
│                              │
│ Dashboard                    │
│ Products                     │
│ Categories                   │
│ Suppliers                    │
│ Inventory                    │
└──────────────┬───────────────┘
               │
               ▼
┌──────────────────────────────┐
│      Spring Boot APIs        │
└──────────────┬───────────────┘
               │
               ▼
┌──────────────────────────────┐
│     Spring Security + JWT    │
└──────────────┬───────────────┘
               │
               ▼
┌──────────────────────────────┐
│       Service Layer          │
│  Business Logic Processing   │
└──────────────┬───────────────┘
               │
               ▼
┌──────────────────────────────┐
│     Repository Layer         │
│ Spring Data JPA / Hibernate  │
└──────────────┬───────────────┘
               │
               ▼
┌──────────────────────────────┐
│      PostgreSQL Database     │
└──────────────────────────────┘
```

---

# 🔐 Authentication Flow

```text
User Login
    │
    ▼
POST /api/auth/login
    │
    ▼
Validate Credentials
    │
    ▼
Generate JWT Token
    │
    ▼
Store Token
    │
    ▼
Protected API Access
    │
    ▼
JWT Validation Filter
    │
    ▼
Authorized Request
```

---

# 📦 Product Workflow

```text
React Form
    │
    ▼
Product Controller
    │
    ▼
Product Service
    │
    ▼
Product Repository
    │
    ▼
PostgreSQL Database
```

---

# 📈 Inventory Workflow

## Stock In

```text
Select Product
      │
      ▼
Enter Quantity
      │
      ▼
Stock In API
      │
      ▼
Quantity Updated
      │
      ▼
Transaction Created
```

## Stock Out

```text
Select Product
      │
      ▼
Validate Available Stock
      │
      ▼
Reduce Quantity
      │
      ▼
Save Transaction
```

---

# 📊 Dashboard Workflow

```text
Database
   │
   ▼
Aggregate Queries
   │
   ▼
Dashboard Service
   │
   ▼
Dashboard APIs
   │
   ▼
React Dashboard
   │
   ▼
Charts & KPI Cards
```

---

# 🗄️ Database Design

## Product

| Field       | Type    |
| ----------- | ------- |
| id          | Long    |
| name        | String  |
| sku         | String  |
| quantity    | Integer |
| price       | Double  |
| category_id | Long    |
| supplier_id | Long    |

## Category

| Field       | Type   |
| ----------- | ------ |
| id          | Long   |
| name        | String |
| description | String |

## Supplier

| Field | Type   |
| ----- | ------ |
| id    | Long   |
| name  | String |
| email | String |
| phone | String |

## Inventory Transaction

| Field            | Type                 |
| ---------------- | -------------------- |
| id               | Long                 |
| product_id       | Long                 |
| quantity         | Integer              |
| type             | STOCK_IN / STOCK_OUT |
| transaction_date | Timestamp            |

---

# 📊 Sample Dataset

* 500+ Products
* 15 Categories
* 50 Suppliers
* Inventory Transaction Records
* Analytics Dashboard Data

---

# 🛠️ Tech Stack

### Backend

* Java 17
* Spring Boot
* Spring Security
* JWT
* Spring Data JPA
* Hibernate
* Maven

### Frontend

* React.js
* Axios
* Bootstrap
* Recharts

### Database

* PostgreSQL

### DevOps

* Docker

### Documentation

* Swagger OpenAPI

---

# 📷 Application Screenshots

## Login Page

```md
![Login](screenshots/login.png)
```

## Dashboard

```md
![Dashboard](screenshots/dashboard.png)
```

## Products

```md
![Products](screenshots/products.png)
```

## Categories

```md
![Categories](screenshots/categories.png)
```

## Suppliers

```md
![Suppliers](screenshots/suppliers.png)
```

## Inventory

```md
![Inventory](screenshots/inventory.png)
```

---

# 🚀 Installation

## Clone Repository

```bash
git clone https://github.com/YOUR_GITHUB_USERNAME/invtrack.git
```

```bash
cd invtrack
```

---

## Backend Setup

```bash
mvn clean install
```

Update:

```properties
src/main/resources/application.properties
```

```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/invtrack_db
spring.datasource.username=postgres
spring.datasource.password=YOUR_PASSWORD
```

Run:

```bash
mvn spring-boot:run
```

---

## Frontend Setup

```bash
npm install
```

```bash
npm run dev
```

---

# 🐳 Docker

Build Docker Image

```bash
docker build -t invtrack .
```

Run Container

```bash
docker run -p 8080:8080 invtrack
```

---

# 📖 Swagger API Documentation

After application startup:

```text
http://localhost:8080/swagger-ui/index.html
```

---

# 🎯 Key Learning Outcomes

* REST API Development
* JWT Authentication
* Spring Security
* PostgreSQL Integration
* ORM using Hibernate
* React Integration
* Inventory Management Workflows
* Dashboard Analytics
* Docker Containerization
* API Documentation

---

# 🔮 Future Enhancements

* AWS EC2 Deployment
* AWS RDS Integration
* Role Based Access Control (RBAC)
* Email Notifications
* PDF Reports
* Excel Export
* CI/CD Pipeline using GitHub Actions
* Microservices Architecture

---

# 👨‍💻 Author

**Vijay Ram**

Java Full Stack Developer

**Skills:** Java • Spring Boot • Spring Security • JWT • PostgreSQL • Hibernate • React.js • Docker • REST APIs • Swagger • Maven

---

⭐ If you found this project useful, consider giving it a star.
