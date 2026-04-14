# 📝 Task Manager REST API

A simple REST API for managing tasks built using **Node.js** and **Express.js**.
This project demonstrates core backend concepts like CRUD operations, RESTful design, and proper error handling.

---

## 🚀 Features

* Create a new task
* Get all tasks
* Get a task by ID
* Update a task
* Mark a task as completed
* Delete a task
* Filter tasks by status (Bonus)
* Sort tasks by creation time (Bonus)
* Proper HTTP status codes and error handling

---

## ⚙️ Tech Stack

* Node.js
* Express.js
* JavaScript (ES6)

---

## 📁 Project Structure

```
task-manager-api/
│
├── index.js
├── package.json
```

---

## ⚙️ Installation & Setup

1. Clone the repository:

```
git clone <your-repo-link>
cd task-manager-api
```

2. Install dependencies:

```
npm install
```

3. Start the server:

```
node index.js
```

Server will run on:

```
http://localhost:3000
```

---

## 📬 API Endpoints

### 1. Create Task

**POST /tasks**

Request Body:

```
{
  "title": "Study DSA",
  "description": "Practice arrays"
}
```

Response:

* 201 Created
* 400 Bad Request (if title is missing)

---

### 2. Get All Tasks

**GET /tasks**

Optional Query Parameters:

* `status=pending`
* `sort=createdAt`

Example:

```id="s8t0pr"
GET /tasks?status=pending
```

---

### 3. Get Task by ID

**GET /tasks/:id**

Response:

* 200 OK
* 404 Not Found (if task doesn't exist)

---

### 4. Update Task

**PUT /tasks/:id**

Request Body:

```
{
  "title": "Updated Task"
}
```

Response:

* 200 OK
* 400 Bad Request (if no fields provided)
* 404 Not Found

---

### 5. Mark Task as Done

**PATCH /tasks/:id/done**

Response:

* 200 OK
* 404 Not Found

---

### 6. Delete Task

**DELETE /tasks/:id**

Response:

* 200 OK
* 404 Not Found

---

## ⚠️ Error Handling

* **400 Bad Request** → Missing or invalid input
* **404 Not Found** → Task not found
* **405 Method Not Allowed** → Unsupported route

---

## 🧠 Implementation Details

* Tasks are stored in an **in-memory array** (no database used)
* Each task contains:

  * `id` (auto-incremented)
  * `title`
  * `description`
  * `status` (pending/done)
  * `createdAt`
* Implemented filtering and sorting using query parameters

---

## 🎯 Key Highlights

* Clean and simple REST API design
* Proper HTTP status codes
* Input validation and error handling
* Bonus features implemented (filtering & sorting)
* Easy to understand and run

---

## 📌 Future Improvements

* Add database (MongoDB / PostgreSQL)
* Add authentication (JWT)
* Convert to MVC structure
* Add API documentation (Swagger)

---

## 👨‍💻 Author

Shaurya Singh

---

## 📎 Note

This project was built as part of a developer assignment to demonstrate backend development skills, API design, and clean coding practices.
