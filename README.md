# E-Commerce Web Application

![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=for-the-badge&logo=spring&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black)
![MySQL](https://img.shields.io/badge/MySQL-00000F?style=for-the-badge&logo=mysql&logoColor=white)

## Overview

This is a full-featured e-commerce web application built with Spring Boot and modern web technologies. The application provides a complete online shopping experience with user authentication, product catalog, shopping cart, payment processing, and order management capabilities.

This project was developed as part of the [Spring Boot E-Commerce Ultimate](https://www.udemy.com/course/spring-boot-e-commerce-ultimate/) course on Udemy, implementing best practices for enterprise-grade e-commerce applications.

## Key Features

- **User Management**
  - Registration and login with JWT authentication
  - Role-based access control (admin, customer)
  - User profile management

- **Product Catalog**
  - Product categories and subcategories
  - Product search and filtering
  - Product details with images and specifications
  - Customer reviews and ratings

- **Shopping Experience**
  - Shopping cart functionality
  - Wishlist management
  - Product recommendations

- **Order Processing**
  - Checkout workflow
  - Multiple payment options (Stripe/PayPal integration)
  - Order history and tracking
  - Invoice generation

- **Admin Dashboard**
  - Product management
  - Order management
  - User management
  - Sales analytics and reporting

## Technology Stack

### Backend
- **Framework**: Spring Boot 3.x
- **Language**: Java 17
- **Database**: MySQL
- **Security**: Spring Security with JWT
- **API Documentation**: Swagger/OpenAPI
- **Payment Integration**: Stripe/PayPal
- **Email Service**: Spring Mail

### Frontend
- **Framework**: React.js
- **State Management**: Redux
- **Styling**: Bootstrap 5 with custom CSS
- **Routing**: React Router

### DevOps
- **Build Tool**: Maven
- **API Testing**: Postman
- **Version Control**: Git
- **Containerization**: Docker (optional)

## Getting Started

### Prerequisites
- Java 17 or higher
- Maven 3.6+
- MySQL 8.0+
- Node.js 16.x+ (for frontend)
- npm 8.x+

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/alhassandiallo/E-Commerce.git
   cd E-Commerce
   ```

2. **Set up the database**
   - Create a MySQL database named `ecommerce_db`
   - Update database configuration in `backend/src/main/resources/application.properties`
     ```properties
     spring.datasource.url=jdbc:mysql://localhost:3306/ecommerce_db
     spring.datasource.username=root
     spring.datasource.password=your_password
     ```

3. **Build and run the backend**
   ```bash
   cd backend
   mvn spring-boot:run
   ```

4. **Run the frontend**
   ```bash
   cd ../frontend
   npm install
   npm start
   ```

5. **Access the application**
   - Frontend: `http://localhost:3000`
   - Backend API: `http://localhost:8080/api`
   - Swagger UI: `http://localhost:8080/swagger-ui.html`

## Project Structure

```
E-Commerce/
├── backend/                # Spring Boot application
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/com/ecommerce/
│   │   │   │   ├── config/       # Configuration classes
│   │   │   │   ├── controller/   # REST API controllers
│   │   │   │   ├── dto/          # Data transfer objects
│   │   │   │   ├── exception/    # Custom exceptions
│   │   │   │   ├── model/        # Entity classes
│   │   │   │   ├── repository/   # Spring Data repositories
│   │   │   │   ├── security/     # Security configuration
│   │   │   │   ├── service/      # Business logic services
│   │   │   │   └── EcommerceApplication.java
│   │   │   └── resources/
│   │   │       ├── application.properties
│   │   │       ├── data.sql      # Initial data
│   │   │       └── schema.sql    # Database schema
│   │   └── test/                 # Unit and integration tests
│   └── pom.xml                   # Maven configuration
│
├── frontend/               # React application
│   ├── public/
│   ├── src/
│   │   ├── components/     # Reusable UI components
│   │   ├── context/        # React context API
│   │   ├── hooks/          # Custom hooks
│   │   ├── pages/          # Application pages
│   │   ├── services/       # API service calls
│   │   ├── store/          # Redux store
│   │   ├── utils/          # Utility functions
│   │   ├── App.js
│   │   └── index.js
│   └── package.json
│
├── docs/                   # Project documentation
├── .gitignore
└── README.md
```

## API Endpoints

### Authentication
- `POST /api/auth/signup` - Register a new user
- `POST /api/auth/signin` - Login to existing account

### Products
- `GET /api/products` - Get all products
- `GET /api/products/{id}` - Get product by ID
- `GET /api/products/search?keyword={keyword}` - Search products

### Cart
- `GET /api/cart` - Get current user's cart
- `POST /api/cart` - Add item to cart
- `DELETE /api/cart/{itemId}` - Remove item from cart

### Orders
- `GET /api/orders` - Get user's order history
- `POST /api/orders` - Place a new order
- `GET /api/orders/{id}` - Get order details

[View full API documentation](http://localhost:8080/swagger-ui.html)

## Screenshots

### Homepage
![Homepage](https://via.placeholder.com/800x500?text=E-Commerce+Homepage)

### Product Listing
![Product Listing](https://via.placeholder.com/800x500?text=Product+Listing+Page)

### Product Details
![Product Details](https://via.placeholder.com/800x500?text=Product+Details+Page)

### Shopping Cart
![Shopping Cart](https://via.placeholder.com/800x500?text=Shopping+Cart)

### Admin Dashboard
![Admin Dashboard](https://via.placeholder.com/800x500?text=Admin+Dashboard)

## Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- [Spring Boot E-Commerce Ultimate Course](https://www.udemy.com/course/spring-boot-e-commerce-ultimate/) on Udemy
- Spring Framework
- React.js Community
- Bootstrap Team

---

**Note**: This application is for educational purposes only. For production deployment, additional security measures and optimizations would be required.
