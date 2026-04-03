# 🚀 URL Shortener Service

A scalable backend URL Shortener system built using **Spring Boot**, designed for high performance, secure API access, and efficient redirection using caching and optimized database design.

---

## 📌 Features

- 🔗 Generate short URLs from long URLs  
- ⚡ Fast redirection using **Redis caching (O(1) lookup)**  
- 📊 Basic click analytics tracking  
- 🔐 Secure APIs with **JWT Authentication**  
- 🚦 API protection using **Rate Limiting (Bucket4j)**  
- 🗄️ Optimized storage using **MySQL indexing**  
- 🧠 Duplicate URL detection using **SHA-256 hashing**

---

## 🛠️ Tech Stack

- Java  
- Spring Boot  
- MySQL  
- Redis  
- Spring Security  
- JWT  
- Bucket4j  
- Maven  

---

## 🏗️ Architecture

- Layered architecture: Controller → Service → Repository  
- RESTful API-based backend system  
- Redis caching layer for fast URL resolution  
- MySQL for persistent storage  
- Optional asynchronous processing for analytics updates  

---

## 🔗 API Endpoints

### Authentication
- POST `/auth/register` → Register new user  
- POST `/auth/login` → Generate JWT token  

### URL Operations
- POST `/api/shorten` → Create short URL  
- GET `/{shortUrl}` → Redirect to original URL  
- GET `/api/analytics/{shortUrl}` → Get click statistics  

---

## ⚙️ Workflow

1. User submits a long URL  
2. System generates a unique short code  
3. URL mapping is stored in MySQL  
4. Frequently accessed URLs are cached in Redis  
5. On request, system checks Redis first → fallback to DB  
6. Analytics are updated for tracking usage  

---

## 📈 Highlights

- High-performance redirection using caching  
- Secure and scalable backend design  
- Optimized database queries with indexing  
- Rate-limited APIs to prevent abuse  
- Clean and modular code structure  

---

## 🚀 Future Improvements

- Custom aliases for short URLs  
- Expiry time for URLs  
- Advanced analytics dashboard  
- Distributed caching support  

---

## 👨‍💻 Author

**Gungun Singhal**  
GitHub: [GungunSinghal03](https://github.com/GungunSinghal03)

---

## ⭐ Support

If you like this project, consider giving it a ⭐ on GitHub!
