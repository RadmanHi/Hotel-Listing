# 🏨 Hotel Listing API - ASP.NET Core

[![ASP.NET Core](https://img.shields.io/badge/ASP.NET%20Core-10.0-purple)](https://dotnet.microsoft.com/)
[![Entity Framework Core](https://img.shields.io/badge/EF%20Core-8.0-blue)](https://docs.microsoft.com/en-us/ef/core/)
[![JWT](https://img.shields.io/badge/JWT-Authentication-orange)](https://jwt.io/)
[![Swagger](https://img.shields.io/badge/Swagger-OpenAPI-brightgreen)](https://swagger.io/)
[![Azure](https://img.shields.io/badge/Azure-Deployed-blue)](https://azure.microsoft.com/)
[![License](https://img.shields.io/badge/License-MIT-yellow)](LICENSE)

## 📌 Overview

A production-ready RESTful Hotel Listing API built with ASP.NET Core, featuring secure authentication, scalable architecture, comprehensive logging, and cloud deployment capabilities.

## ✨ Technical Features

### 🏗️ Core Architecture
- **RESTful API Design** - HTTP methods, status codes, and resource naming conventions
- **Repository Pattern** - Abstraction layer for data access separation
- **DTO & AutoMapper** - Object-object mapping with profile-based configurations
- **Dependency Injection** - Built-in DI container with scoped, transient, and singleton lifetimes

### 🗄️ Database & Data Access
- **Entity Framework Core 8** - Code-first approach with migrations
- **SQL Server / PostgreSQL** - Multi-database support
- **Repository Pattern Implementation** - Generic and specific repositories
- **Unit of Work** - Transaction management across multiple repositories

### 🔐 Security & Authentication
- **ASP.NET Core Identity** - User management with roles and claims
- **JWT Authentication** - Stateless token-based authentication
- **Refresh Tokens** - Sliding expiration and token rotation strategy
- **Role-based Authorization** - Admin, HotelManager, and Customer roles
- **Password Hashing** - BCrypt/SHA-256 encryption
- **CORS Policies** - Configurable cross-origin resource sharing

### 📊 Logging & Monitoring
- **Serilog** - Structured logging with sinks for Console, File, and Azure Application Insights
- **Health Checks** - Custom health indicators for DB, API dependencies, and memory
- **Request Logging Middleware** - Automatic logging of all HTTP requests/responses
- **Performance Monitoring** - Endpoint response time tracking

### ⚡ Performance & Scalability
- **Response Caching** - In-memory and distributed caching (Redis ready)
- **Output Caching** - Cache API responses based on query parameters
- **Request Throttling** - Rate limiting with fixed/window/sliding strategies
- **API Versioning** - URL path and query string versioning support
- **Pagination** - Efficient data retrieval with page-based navigation
- **Asynchronous Programming** - Non-blocking operations throughout

### 📚 Documentation & Testing
- **Swagger/OpenAPI** - Live interactive API documentation
- **Swagger UI Customization** - JWT Bearer token integration
- **XML Comments** - Automatic endpoint descriptions
- **Postman Collection** - Ready-to-use test suite
- **Integration Testing** - xUnit tests with in-memory database

### ☁️ Deployment & DevOps
- **Azure App Service** - Production deployment ready
- **Azure SQL Database** - Managed cloud database
- **GitHub Actions** - CI/CD pipeline configured
- **Environment Configuration** - appsettings.json with environment overrides
- **Docker Support** - Containerized deployment option

### 🛠️ Development Tools
- **GitHub** - Source control with semantic commits
- **.NET CLI** - Full command-line support
- **Entity Framework Tools** - Migrations and database updates
- **dotnet-env** - Environment variable management

## 🚀 Quick Start

### Prerequisites
- [.NET 10.0 SDK](https://dotnet.microsoft.com/download)
- [SQL Server](https://www.microsoft.com/en-us/sql-server/) or [PostgreSQL](https://www.postgresql.org/)
- [Git](https://git-scm.com/)

### Installation

```bash
# Clone the repository
git clone https://github.com/yourusername/hotel-listing-api.git
cd hotel-listing-api

# Restore dependencies
dotnet restore

# Update database connection string in appsettings.json
# Then run migrations
dotnet ef database update

# Seed initial data (admin user, roles, hotels)
dotnet run --seed

# Run the application
dotnet run
