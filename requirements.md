# Airbnb Clone – Backend Requirements Specification

This document defines the technical and functional requirements for key backend features of the Airbnb Clone system.  
It includes API endpoints, expected inputs and outputs, validation rules, and performance criteria.

---

## 1. 🧑‍💻 User Authentication

### **Description**
Manages user registration, login, and authentication using JWT tokens.

### **Functional Requirements**
- Users can register with first name, last name, email, password, and role.
- The system must validate unique email addresses.
- Passwords must be hashed before storage.
- Users can log in and receive a JWT token for session authentication.

### **API Endpoints**
| Method | Endpoint | Description |
|--------|-----------|-------------|
| POST | `/api/auth/register` | Register a new user |
| POST | `/api/auth/login` | Authenticate user and issue token |
| GET | `/api/users/:id` | Get user profile (authenticated only) |

### **Input / Output Examples**
**POST /api/auth/register**
```json
Input:
{
  "first_name": "Sama",
  "last_name": "Mostafa",
  "email": "sama@example.com",
  "password": "MyPass@123",
  "role": "guest"
}

Output:
{
  "message": "User registered successfully",
  "user_id": "uuid"
}
