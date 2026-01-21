# BridgeLMS API

**BridgeLMS** is a lightweight, high-performance Learning Management System (LMS) API designed to connect learners and tutors seamlessly. Built with **FastAPI**, this RESTful service provides a robust backend for managing courses, attendance, learning materials, and real-time announcements.

---

## Features

* **Authentication & Identity**: Secure user registration, login, and profile management using OAuth2 protocols.
* **Course Management**: Comprehensive CRUD operations for courses, including enrollment workflows and tutor assignments.
* **Resource Handling**: Secure endpoints for uploading and accessing course-specific learning materials.
* **Attendance Tracking**: Automated check-in systems for learners with verification capabilities for tutors.
* **Scheduling**: Integrated calendar and event management to track deadlines and course sessions.
* **Communication**: Real-time course updates and notifications via a dedicated announcements system.

---

## Tech Stack

* **Framework**: FastAPI (Python)
* **Documentation**: OpenAPI 3.1.0 (Swagger UI)
* **Security**: Bearer Token (JWT) Authentication
* **Data Validation**: Pydantic schemas for robust request/response handling

---

## API Documentation

The API includes built-in interactive documentation accessible via Swagger UI.

### Key Endpoint Groups

| Category | Description |
| --- | --- |
| **Authentication** | Handles `/users/register`, `/users/login`, and `/users/profile`. |
| **Courses** | Manages course creation, enrollment, and tutor-specific lookups. |
| **Learning Resources** | Handles the uploading and retrieval of course materials. |
| **Attendance** | Manages learner check-ins and attendance history. |
| **Announcements** | Provides a channel for course-wide updates. |

---

## Security

Most endpoints (marked with a lock icon in the documentation) require an **Authorization** header.

* **Format**: `Authorization: Bearer <your_access_token>`
* **Roles**: The system supports specific user roles defined in the `UserRole` schema to restrict access to sensitive operations like course creation or attendance verification.

---

## Data Schemas

The API uses structured objects for all data transfers to ensure consistency:

* **RegisterUserRequest**: Validates email, password, and initial profile data.
* **Body_create_course**: Defines the required structure for new educational offerings.
* **HTTPValidationError**: Standardized error responses for failed data validation.

