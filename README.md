# 📝 Task Manager App

A full-stack Task Management application built with **ReactJS**, **PHP (Laravel)**, and **MySQL**, designed for efficient task tracking and organization. This project was developed as part of a Software Engineering Assessment and demonstrates best practices in frontend architecture, backend API design, and deployment workflows.

---

## 🌐 Live URLs

- 🔗 **Frontend**: [http://13.233.71.79](http://13.233.71.79)
- 🔗 **Backend API**: [http://43.204.236.19:8080](http://43.204.236.19:8080)

---

## 🎯 Objective

Develop a Task Manager App that allows users to:

- Register and log in securely
- Create, update, delete, and manage tasks
- Filter and search for tasks
- Drag & drop tasks across different statuses (To Do, In Progress, Done)
- Edit tasks inline
- Deploy application with a production-ready setup

---

## 👣 User Flow

1. **Register**:  
   Users create an account by providing valid registration credentials (name, email, password).

2. **Login**:  
   After successful registration, the user is redirected to the login page. Upon entering valid credentials, a token is received and stored securely.

3. **Dashboard (Task Board)**:  
   Authenticated users are taken to the **Taskboard** page, where they can:
   - View all tasks in a **grid layout** grouped by task status.
   - Add new tasks using a form with proper validation.
   - **Inline edit** task name, description, or status by clicking on the respective fields.
   - Use **drag and drop** to move tasks between **To Do**, **In Progress**, and **Done** columns.
   - Dragging is enabled by holding the **drag icon** at the bottom-right corner of the task card.
   - Tasks are updated optimistically for better UX, even before the API responds.

---

## 🛠️ Tech Stack

### Frontend

- [ReactJS](https://reactjs.org/) with [Vite](https://vitejs.dev/)
- [Redux](https://redux.js.org/) for state management
- [Redux-Saga](https://redux-saga.js.org/) for side effects handling
- [Tailwind CSS](https://tailwindcss.com/) for styling
- [@dnd-kit](https://docs.dndkit.com/) for drag-and-drop
- [React Router](https://reactrouter.com/) for routing
- Optimistic UI updates, Debounced search, Lazy loading

### Backend

- [PHP Laravel](https://laravel.com/) MVC Framework
- [MySQL](https://www.mysql.com/) database
- [Laravel Sanctum](https://laravel.com/docs/10.x/sanctum) for token-based authentication
- RESTful API with search, filter, and CRUD functionality
- Dockerized setup for containerized deployment
- Unit tests for API endpoints

---

## 📦 Features

### ✅ Task Management

- Create, update, delete tasks
- Inline editing of task name, description, status
- Drag and drop tasks between statuses (To Do, In Progress, Done)
- Filtering by status, sorting by due date
- Debounced task search bar
- Optimistic UI updates (UI updates immediately on actions)

### 👤 Auth Flow

- User registration and login (secured with Laravel Sanctum)
- Authentication token stored securely
- Protected Taskboard route for authenticated users only

### 🧩 UI/UX

- Fully responsive and clean layout
- Smooth animations on drag & drop
- Accessible forms with validation
- Reusable and modular components

### 🧠 State & Performance

- Redux & Redux-Saga for predictable and scalable state management
- Debounced search to reduce unnecessary API calls
- API caching and lazy-loading of components for performance optimization

---

## 🧪 Testing

- Laravel feature tests for API endpoints
- Tests include validation, task creation, update, deletion, and filtering

---

## 🐳 Docker Support

- Backend containerized using Docker
- Docker Compose configured for Laravel backend and MySQL
- Easy to deploy and run in isolated environments

---

## ☁️ Deployment

- Frontend deployed on **AWS EC2** (Vite build served via Nginx)
- Backend deployed on **AWS EC2**
- MySQL hosted on **AWS RDS**
- Laravel environment variables secured
- Production-ready setup with separate environments

---

## 🗃️ API Endpoints

| Method | Endpoint               | Description             |
| ------ | ---------------------- | ----------------------- |
| POST   | /api/register          | Register new user       |
| POST   | /api/login             | Login and receive token |
| GET    | /api/tasks             | Fetch all tasks         |
| GET    | /api/tasks?search=term | Search tasks            |
| GET    | /api/tasks?status=done | Filter by status        |
| POST   | /api/tasks             | Create new task         |
| PUT    | /api/tasks/{id}        | Update task             |
| DELETE | /api/tasks/{id}        | Delete task             |
