# 🔗 URL Shortener

A **URL Shortener Web Application** that allows users to generate short
links, manage them, and track analytics. Built with **Java, Spring Boot,
Spring Security (JWT), and React**.

👉 **[Live Demo](https://codewithpritam.site)**

------------------------------------------------------------------------

## 🚀 Features

-   ✅ Shorten long URLs into simple shareable links\
-   ✅ Redirect users seamlessly to the original URL\
-   ✅ User authentication with **JWT-based security**\
-   ✅ Analytics tracking (click count, usage stats)\
-   ✅ Caching for **faster performance**\
-   ✅ Responsive frontend built with **React**

------------------------------------------------------------------------

## 🛠 Tech Stack

**Backend:** Java, Spring Boot, Spring Security, JWT, Redis (caching)\
**Frontend:** React, HTML, CSS, JavaScript\
**Database:** MySQL\
**Tools:** Postman, Git, Maven, Docker

------------------------------------------------------------------------

## 📂 Project Structure

    url-shortener/
    │── backend/        # Spring Boot application
    │   ├── controller/ # REST API controllers
    │   ├── service/    # Business logic
    │   ├── repository/ # Database access layer
    │   └── security/   # JWT Authentication
    │
    │── frontend/       # React application
    │   ├── components/ # UI Components
    │   ├── pages/      # Application pages
    │   └── utils/      # Helper functions

------------------------------------------------------------------------

## ⚙️ Setup & Installation

### 1. Clone the Repository

``` bash
git clone https://github.com/PritamBiswas06/url-shortener.git
cd url-shortener
```

### 2. Backend (Spring Boot)

``` bash
cd backend
mvn spring-boot:run
```

Runs at: `http://localhost:8080`

### 3. Frontend (React)

``` bash
cd frontend
npm install
npm start
```

Runs at: `http://localhost:3000`

------------------------------------------------------------------------

## 📌 API Endpoints

### Authentication

-   `POST /api/auth/signup` → Register new user\
-   `POST /api/auth/login` → Login & get JWT token

### URL Management

-   `POST /api/url/shorten` → Create a short URL\
-   `GET /api/url/{shortCode}` → Redirect to original URL\
-   `GET /api/url/analytics/{shortCode}` → Fetch analytics

------------------------------------------------------------------------

## 📊 Example

**Request:**

``` json
POST /api/url/shorten
{
  "originalUrl": "https://www.example.com/some/very/long/url"
}
```

**Response:**

``` json
{
  "shortUrl": "http://localhost:8080/u/xyz123",
  "originalUrl": "https://www.example.com/some/very/long/url"
}
```

------------------------------------------------------------------------

## 🔒 Security

-   JWT-based authentication\
-   Role-based access control\
-   Passwords hashed with **BCrypt**

------------------------------------------------------------------------

## 👨‍💻 Author

**Pritam Kumar Biswas**\
- 🌐 [Portfolio](https://portfolio.codewithpritam.site)\
- 💻 [GitHub](https://github.com/PritamBiswas06)\
- 💼 [LinkedIn](https://linkedin.com/in/pritambiswasnetwork)

------------------------------------------------------------------------

⚡ *A simple but powerful tool to shorten URLs and track their usage.*
