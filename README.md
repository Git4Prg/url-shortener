# URL Shortener Service

A robust URL shortening service built with Spring Boot that allows users to create shortened URLs and track their usage analytics.

## Features

- **URL Shortening**: Convert long URLs into short, manageable links
- **User Authentication**: Secure JWT-based authentication system
- **Analytics Dashboard**: Track click counts and usage patterns
- **User Management**: Register and manage user accounts
- **API Security**: Protected endpoints with role-based access control

## Tech Stack

- **Backend**: Spring Boot 3.5.4
- **Security**: Spring Security with JWT
- **Database**: MySQL
- **Build Tool**: Maven
- **Java Version**: 21

## Prerequisites

- JDK 21
- MySQL Server
- Maven

## Configuration

Configure the following properties in `application.properties`:


spring.datasource.url=jdbc:mysql://localhost:3306/url_shortener_db
spring.datasource.username=your_username
spring.datasource.password=your_password
jwt.secret=your_jwt_secret
jwt.expiration=178200000
frontend.url=http://localhost:5173


API Endpoints
Authentication
POST /api/auth/public/register - Register new user
POST /api/auth/public/login - Login user
URL Operations
POST /api/urls/shorten - Create short URL
GET /api/urls/myurls - Get user's URLs
GET /api/urls/analytics/{shortUrl} - Get URL analytics
GET /api/urls/totalClicks - Get total clicks statistics
GET /{shortUrl} - Redirect to original URL
Running the Application
Clone the repository
Configure database settings in application.properties
Run with Maven:
./mvnw spring-boot:run

Build
To build the project:

./mvnw clean install
