# Nova Task Manager

A full-stack task manager web application built with React, React Router, Node.js, Express and SQLite.

## Student Name
Ndiye Mbaiwa

## Project Description
Nova Task Manager allows users to register, login, add tasks, view tasks, search tasks, edit task details, mark tasks as complete and delete tasks. The frontend connects to the backend API, and the backend stores users and tasks in a SQLite database.

## Technologies Used

### Frontend
- React
- React Router
- CSS
- Vite

### Backend
- Node.js
- Express.js
- SQLite
- JWT authentication
- bcryptjs password hashing
- CORS
- dotenv

## Features
- User registration
- User login
- JWT protected task routes
- Add task form with validation
- View task list
- Search tasks
- View task details
- Edit task details
- Mark task as complete/incomplete
- Delete task
- Responsive design for desktop, tablet and mobile

## Folder Structure

```text
react-midterm-project
├── backend
│   ├── db.js
│   ├── server.js
│   ├── package.json
│   └── .env.example
├── src
│   ├── components
│   │   ├── Navbar.jsx
│   │   └── TaskCard.jsx
│   ├── pages
│   │   ├── Home.jsx
│   │   ├── Login.jsx
│   │   ├── Register.jsx
│   │   ├── List.jsx
│   │   ├── Details.jsx
│   │   └── AddTask.jsx
│   ├── services
│   │   └── api.js
│   ├── App.jsx
│   ├── App.css
│   └── main.jsx
├── package.json
└── README.md
```

## How to Run Locally

### 1. Run Backend

```bash
cd backend
npm install
copy .env.example .env
npm run dev
```

For Mac/Linux, use:

```bash
cp .env.example .env
```

Backend runs on:

```text
http://localhost:5000
```

### 2. Run Frontend

Open a second terminal in the main project folder:

```bash
npm install
npm run dev
```

Frontend runs on:

```text
http://localhost:5173
```

## Frontend Environment Variable

Create `.env` in the main project folder:

```env
VITE_API_URL=http://localhost:5000/api
```

When deployed on Vercel, set `VITE_API_URL` to your backend URL plus `/api`.

Example:

```env
VITE_API_URL=https://your-backend-name.onrender.com/api
```

## Backend Environment Variables

Create `backend/.env`:

```env
PORT=5000
FRONTEND_URL=http://localhost:5173
JWT_SECRET=replace-this-with-a-long-random-secret
SQLITE_PATH=./database.sqlite
```

When deployed, set `FRONTEND_URL` to your Vercel website URL.

Example:

```env
FRONTEND_URL=https://your-frontend-name.vercel.app
```

## SQLite Database

The SQLite database is created automatically when the backend starts. The database file will be created inside the `backend` folder as:

```text
database.sqlite
```

The backend creates these tables automatically:

- `users`
- `tasks`

## API Endpoints

### Auth

```text
POST /api/auth/register
POST /api/auth/login
GET  /api/auth/me
```

### Tasks

```text
GET    /api/tasks
GET    /api/tasks/:id
POST   /api/tasks
PUT    /api/tasks/:id
DELETE /api/tasks/:id
```

Task routes require login because they use JWT authentication.

## Deployment Notes

### Frontend on Vercel
1. Deploy the main project folder.
2. Set environment variable:

```env
VITE_API_URL=https://your-backend-name.onrender.com/api
```

3. Redeploy after adding the environment variable.

### Backend on Render
1. Deploy the `backend` folder as a Node.js web service.
2. Build command:

```bash
npm install
```

3. Start command:

```bash
npm start
```

4. Add environment variables:

```env
PORT=5000
FRONTEND_URL=https://your-frontend-name.vercel.app
JWT_SECRET=replace-this-with-a-long-random-secret
SQLITE_PATH=./database.sqlite
```

## Screenshots Required for Submission
Take screenshots of:
- Home page
- Register/Login page
- Task list page
- Add task form page
- Task details page

## Live URL
Add your deployed frontend URL here after deployment:

```text
Frontend: 
Backend: 
```
