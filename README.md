# Task Manager App

A full-stack Task Management application built with **ReactJS**, **PHP (Laravel)**, and **MySQL**, designed for efficient task tracking and organization. The project implements best practices in frontend architecture, backend API design, and production deployment.

---

## Live URLs

- **Frontend**: [http://13.233.71.79](http://13.233.71.79)
- **Backend API**: [http://43.204.236.19:8080](http://43.204.236.19:8080)

---

## Objective

The application allows users to:

- Register and log in securely
- Create, update, delete, and manage tasks
- Filter, sort, and search tasks
- Drag and drop tasks between statuses (To Do, In Progress, Done)
- Edit tasks inline
- Experience a responsive and interactive UI with optimistic updates

---

## User Flow

1. **Registration**  
   New users sign up with their name, email, and password.

2. **Login**  
   Upon successful registration, users are directed to the login page. Valid credentials return an authentication token stored securely.

3. **Taskboard**  
   Authenticated users access the taskboard where they can:
   - View tasks in a grid grouped by status
   - Add new tasks using a validated form
   - Edit task title, description, and status inline
   - Move tasks between columns via drag and drop, enabled by an icon in the bottom-right of each card
   - Experience instant UI feedback via optimistic updates before the API responds

---

## Tech Stack

### Frontend

- **ReactJS** with **Vite**
- **Redux** for state management
- **Redux-Saga** for handling side effects
- **Tailwind CSS** for styling
- **@dnd-kit** for drag-and-drop
- **React Router** for routing
- Optimistic UI updates, lazy loading, debounced search

### Backend

- **Laravel (PHP MVC Framework)**
- **MySQL** for data storage
- **Laravel Sanctum** for token-based authentication
- RESTful API with search, filter, and CRUD
- Unit tests for API functionality
- Dockerized setup for deployment

---

## Key Features

### Task Management

- Add, edit (inline), and delete tasks
- Drag and drop between task statuses
- Search tasks with debounce
- Filter and sort tasks by status and due date
- Optimistic UI updates

### Authentication

- Secure user registration and login
- Token stored on the client securely
- Authenticated access to task features

### UI/UX and Performance

- Clean, responsive, and modular design
- Smooth animations on drag-and-drop
- Debounced API calls for better performance
- Lazy-loaded components and API response caching

---

## Testing

- Feature tests written using Laravel's built-in testing tools
- Coverage includes validation, CRUD operations, and filtering logic

---

## Docker Support

- Laravel backend and MySQL containerized using Docker
- Docker Compose file for easy setup
- Nginx configured for serving the Laravel application

---

## Deployment

- Frontend deployed to **AWS EC2** and served via **Nginx**
- Backend API deployed to **AWS EC2**
- Database hosted on **AWS RDS**
- Environment variables secured with `.env` configuration

---

## API Endpoints

| Method | Endpoint               | Description            |
| ------ | ---------------------- | ---------------------- |
| POST   | /api/register          | Register a new user    |
| POST   | /api/login             | Authenticate user      |
| GET    | /api/tasks             | Fetch all tasks        |
| GET    | /api/tasks?search=term | Search tasks           |
| GET    | /api/tasks?status=done | Filter tasks by status |
| POST   | /api/tasks             | Create a new task      |
| PUT    | /api/tasks/{id}        | Update a task          |
| DELETE | /api/tasks/{id}        | Delete a task          |
