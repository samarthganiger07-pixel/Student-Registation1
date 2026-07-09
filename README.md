# Task Ledger REST API

A simple full-stack **Task Ledger** application built with **React** (frontend) and **Express.js** (backend). It demonstrates CRUD (Create, Read, Update, Delete) operations using a REST API. Data is stored in memory, so it resets whenever the server restarts.

---

# Features

- Create new tasks
- View all tasks
- Mark tasks as complete/incomplete
- Delete tasks
- Clean terminal-style UI
- REST API using Express
- CORS enabled
- JSON request/response handling

---

# Tech Stack

## Frontend

- React
- Vite
- CSS
- Fetch API

## Backend

- Node.js
- Express.js
- CORS

---

# Project Structure

```
project/
│
├── backend/
│   ├── index.js
│   └── package.json
│
├── frontend/
│   ├── src/
│   │   ├── App.jsx
│   │   ├── App.css
│   │   └── main.jsx
│   └── package.json
│
└── README.md
```

---

# Installation

## 1. Clone the project

```bash
git clone https://github.com/yourusername/task-ledger.git
```

```bash
cd task-ledger
```

---

# Backend Setup

Navigate to backend folder.

```bash
cd backend
```

Install dependencies.

```bash
npm install
```

Start the Express server.

```bash
node index.js
```

Server starts on

```
http://localhost:3000
```

---

# Frontend Setup

Open another terminal.

```bash
cd frontend
```

Install dependencies.

```bash
npm install
```

Run React.

```bash
npm run dev
```

Frontend runs on

```
http://localhost:5173
```

---

# REST API Endpoints

## GET All Tasks

```
GET /tasks
```

Response

```json
[
  {
    "id": 1,
    "title": "Learn Express",
    "done": false
  }
]
```

---

## GET Single Task

```
GET /tasks/:id
```

Example

```
GET /tasks/1
```

---

## Create Task

```
POST /tasks
```

Request Body

```json
{
  "title": "Learn React"
}
```

Response

```json
{
  "id": 3,
  "title": "Learn React",
  "done": false
}
```

---

## Update Task

```
PUT /tasks/:id
```

Request Body

```json
{
  "title": "Learn React Hooks",
  "done": true
}
```

---

## Delete Task

```
DELETE /tasks/:id
```

Response

```json
{
  "message": "Task deleted"
}
```

---

# API Response Codes

| Code | Description |
|------|-------------|
|200|Success|
|201|Created|
|400|Bad Request|
|404|Not Found|

---

# Frontend Functionality

The React application provides:

- Load tasks from API
- Add task
- Toggle task status
- Delete task
- Live task counter
- Error handling
- Loading state

---

# Example Workflow

1. Start Express server.
2. Start React application.
3. Open browser.
4. Add a task.
5. Mark it completed.
6. Delete it.
7. Refresh page.
8. Data remains until the server is restarted.

---

# Sample Initial Data

```json
[
  {
    "id": 1,
    "title": "Learn Express",
    "done": false
  },
  {
    "id": 2,
    "title": "Build a REST API",
    "done": false
  }
]
```

---

# Dependencies

Backend

```text
express
cors
```

Frontend

```text
react
vite
```

---

# Notes

- This project uses an in-memory array instead of a database.
- Restarting the Express server resets all tasks.
- Designed as a beginner-friendly REST API example.
- Easily extendable to SQLite, MongoDB, or MySQL.

---

# Future Improvements

- SQLite or MongoDB database
- Authentication
- User accounts
- Search tasks
- Edit task title
- Due dates
- Categories
- Pagination
- Dark mode
- Docker support

---

# License

This project is available for educational purposes and can be modified or extended for learning full-stack web development.

---

# Author

**Samarth Ganiger**

Built using **React + Express.js** to demonstrate CRUD operations with a simple REST API.
