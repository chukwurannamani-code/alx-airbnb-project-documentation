# 🏠 ALX Airbnb Project — Backend Requirements Documentation

## Overview
This document outlines the **technical** and **functional requirements** for key backend features of the ALX Airbnb Clone system.  
It includes detailed specifications for:

1. User Authentication  
2. Property Management  
3. Booking System  

Each section covers the system’s objectives, API endpoints, request/response structures, validation rules, and performance expectations.

---

## 1️⃣ User Authentication

### **Functional Requirements**
- Users must be able to register and log in securely.  
- Passwords must be stored in a hashed format.  
- Authentication should use **JWT (JSON Web Tokens)**.  
- Only authenticated users can perform actions such as property creation or booking.  

### **API Endpoints**

| Method | Endpoint | Description |
|--------|-----------|-------------|
| `POST` | `/users/` | Create (register) a new user |
| `GET` | `/users/{user_id}/` | Retrieve specific user details |
| `PUT` | `/users/{user_id}/` | Update user profile information |
| `DELETE` | `/users/{user_id}/` | Delete a user account |
| `POST` | `/auth/login` | Authenticate user and return JWT token |

### **Input Specification**

**User Registration**
```json
{
  "full_name": "John Doe",
  "email": "john@example.com",
  "password": "SecurePass123!"
}
