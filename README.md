# djangoTaskManagerJWT

A fully functional Task Management REST API built using Django REST Framework and JWT Authentication.
Users can register, log in, and manage their personal tasks securely using JSON Web Tokens. This project helped me understand JWT authentication and building real-world REST APIs using Django.

---

## Features
### Authentication (JWT)
- User Registration
- User Login (returns refresh & access tokens)
- Uses SimpleJWT for secure authentication
- Access token required for all task operations

### Task Management (CRUD)
- Create new tasks
- View all tasks
- View single task
- Update task (title, description, completion status)
- Delete task

---

## Tech Stack
- Python 3
- Django
- Django REST Framework
- SimpleJWT (JWT Authentication)
- SQLite Database
- Postman (API Testing)

## Project Structure
```
djangoTaskAPI/
│
├── tasks/              # tasks App (CRUD)
├── users/              # User Auth App (Register/Login)
├── task_api/           # Django Project Settings
│
├── screenshots/        # API testing screenshots
├── postman/            # Postman collection JSON
│
├── manage.py
├── requirements.txt
└── README.md
```

## API Endpoints

### Authentication
| Method | Endpoint          | Description            |
| ------ | ----------------- | ---------------------- |
| POST   | `/auth/register/` | Create new user        |
| POST   | `/auth/login/`    | Login & get JWT tokens |
| POST   | `/auth/refresh/`  | Refresh access token   |

### Task Endpoints (Require Bearer Token)
#### Header required:
#### Authorization: Bearer <access_token>
| Method | Endpoint       | Description      |
| ------ | -------------- | ---------------- |
| GET    | `/tasks/`      | List all tasks   |
| POST   | `/tasks/`      | Create a task    |
| GET    | `/tasks/<id>/` | Get task details |
| PUT    | `/tasks/<id>/` | Update task      |
| DELETE | `/tasks/<id>/` | Delete task      |

## Screenshots
All API testing screenshots are included in screenshots folder

## Postman Collection
Import the collection from postman/Task_API.postman_collection .
It Contains all API endpoints for quick testing.
