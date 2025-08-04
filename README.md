

---

# 🛒 Spring Boot E-Commerce Platform  
*Full-Stack Online Store with React, Spring Boot 3, JWT, and Stripe Integration*  

[![Spring Boot](https://img.shields.io/badge/Spring_Boot-3.2.0-6DB33F?logo=spring&logoColor=white)](https://spring.io/projects/spring-boot)
[![React](https://img.shields.io/badge/React-18.2.0-61DAFB?logo=react&logoColor=black)](https://reactjs.org/)
[![MySQL](https://img.shields.io/badge/MySQL-8.0-4479A1?logo=mysql&logoColor=white)](https://www.mysql.com/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

> **A production-ready e-commerce platform** built during the [Udemy: Spring Boot E-Commerce Ultimate](https://www.udemy.com/course/spring-boot-e-commerce-ultimate/) course. Features JWT authentication, real-time cart management, Stripe payments, role-based access control, and RESTful API design.  

![E-Commerce Dashboard Preview](https://via.placeholder.com/800x400?text=Live+Demo+Screenshots+Here)  


---

## ✨ Key Features  
- **🔐 Secure Authentication**  
  JWT-based login/signup with Spring Security, password encryption (BCrypt), and role-based access (USER/ADMIN).
- **🛒 Real-Time Shopping Experience**  
  Cart persistence, wishlist, product filtering, search, and inventory management.
- **💳 Payment Integration**  
  Stripe API for secure credit card processing (test mode enabled).
- **📊 Admin Dashboard**  
  Manage products, orders, users, and analytics (React frontend).
- **📦 Order Management**  
  Order history, status tracking, and email notifications (via Spring Mail).
- **📱 Responsive UI**  
  Modern React frontend with Redux for state management (mobile/desktop compatible).
- **🔍 RESTful API**  
  Well-documented endpoints following HATEOAS principles (Swagger UI included).

---

## 🛠 Tech Stack  
| **Category**       | **Technologies**                                                                 |
|---------------------|--------------------------------------------------------------------------------|
| **Backend**         | Java 17, Spring Boot 3.2, Spring Data JPA, Spring Security, Spring Mail, Lombok |
| **Frontend**        | React 18, Redux Toolkit, Axios, Bootstrap 5, React Router                        |
| **Database**        | MySQL 8.0 (with Docker Compose setup)                                           |
| **API Documentation**| Swagger UI (`/swagger-ui.html`)                                                 |
| **Payment**         | Stripe Test Mode Integration                                                   |
| **DevOps**          | Maven, Git, GitHub Actions (CI/CD ready), Docker                                |

---

## 🚀 Getting Started  
### Prerequisites
- Java 17+
- Node.js 18+
- MySQL 8.0
- Stripe Test Keys ([Get test keys](https://dashboard.stripe.com/test/apikeys))

### Setup Instructions
1. **Clone the repository**  
   ```bash
   git clone https://github.com/alhassandiallo/E-Commerce.git
   cd E-Commerce
   ```

2. **Configure Environment Variables**  
   Create `.env` file in `backend/` with:
   ```env
   SPRING_DATASOURCE_URL=jdbc:mysql://localhost:3306/ecommerce_db
   SPRING_DATASOURCE_USERNAME=root
   SPRING_DATASOURCE_PASSWORD=your_password
   STRIPE_SECRET_KEY=sk_test_xxx
   STRIPE_PUBLISHABLE_KEY=pk_test_xxx
   JWT_SECRET=your_strong_secret
   ```

3. **Run the Backend**  
   ```bash
   cd backend
   ./mvnw spring-boot:run  # Linux/Mac
   # OR
   mvnw.cmd spring-boot:run  # Windows
   ```

4. **Run the Frontend**  
   ```bash
   cd ../frontend
   npm install
   npm start
   ```

5. **Access the Application**  
   - Frontend: `http://localhost:3000`  
   - Backend API: `http://localhost:8080/api`  
   - Swagger Docs: `http://localhost:8080/swagger-ui.html`  

> 💡 **Troubleshooting Tip**: If you get port conflicts, change `server.port` in `backend/src/main/resources/application.properties`.

---

## 🌐 Project Structure  
```markdown
E-Commerce/
├── backend/                # Spring Boot Application
│   ├── src/main/java/com/ecommerce/
│   │   ├── config/         # Security, Swagger, CORS
│   │   ├── controller/     # REST APIs (User, Product, Order)
│   │   ├── service/        # Business logic (Stripe, Email)
│   │   ├── repository/     # JPA Repositories
│   │   └── model/          # Entities (User, Product, Order)
│   └── resources/
│       ├── application.properties  # Configs
│       └── data.sql                # Initial DB setup
│
├── frontend/               # React App
│   ├── public/
│   └── src/
│       ├── components/     # Reusable UI (ProductCard, Navbar)
│       ├── pages/          # Views (Home, Cart, Checkout)
│       ├── store/          # Redux state (cart, auth)
│       └── services/       # API calls (axios)
│
├── docker-compose.yml      # MySQL container setup
└── README.md
```

---

## 📸 Screenshots  

| **User View**          | **Admin Dashboard**     |
|------------------------|-------------------------|
| ![User View](https://via.placeholder.com/400x250?text=Product+Page) | ![Admin](https://via.placeholder.com/400x250?text=Order+Management) |

---

## 🧠 Why This Project Stands Out  
- **Real-World Focus**: Implements idempotency keys for payments, inventory locks, and email notifications.  
- **Security First**: CSRF protection, rate limiting, and JWT token expiration.  
- **Scalable Design**: Stateless architecture, database indexing, and connection pooling.  
- **Course Enhancements**: Added [mention YOUR improvements, e.g., "caching with Redis", "Dockerized deployment"].  

> ✨ **Pro Tip**: This project mirrors architectures used at companies like Shopify and Amazon. Understanding these patterns makes you interview-ready!

---

## 📜 License  
Distributed under the MIT License. See `LICENSE` for details.

---

## 🤝 Contributing  
While this is a course project, feel free to:  
1. Report bugs via [Issues](https://github.com/alhassandiallo/E-Commerce/issues)  
2. Suggest improvements (fork → PR)  
3. **Star the repo** to support future updates! ⭐  

---



