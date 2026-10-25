# React CRUD – Users (MERN)

Full-stack CRUD application for managing users (name, e-mail, age). A React front end lists users and lets you create, update and delete them; a Node.js/Express back end stores them in MongoDB through Mongoose.

## Tech stack

| Part | Technologies |
| --- | --- |
| `clint/` (front end) | React 18, Vite 5, React Router 6, axios, Bootstrap 5 |
| `server/` (back end) | Node.js (CommonJS), Express 4, Mongoose 8, cors, nodemon |
| Database | MongoDB |

`Client/CRUDS/` is an unmodified Vite + React starter template and is not used by the application.

## Folder structure

```text
React-CRUD-Front-Back/
├── Client/
│   └── CRUDS/
│       ├── public/
│       ├── src/
│       ├── index.html
│       ├── package.json
│       ├── README.md
│       └── vite.config.js
├── clint/
│   ├── public/
│   ├── src/
│   │   ├── assets/
│   │   ├── App.jsx
│   │   └── main.jsx
│   ├── index.html
│   ├── package.json
│   ├── README.md
│   └── vite.config.js
├── server/
│   ├── models/
│   ├── index.js
│   └── package.json
├── .editorconfig
├── .gitignore
└── README.md
```

## API endpoints (`server/index.js`)

| Method | Path | Description |
| --- | --- | --- |
| GET | `/` | List all users |
| GET | `/getUser/:id` | Get one user |
| POST | `/createUser` | Create a user |
| PUT | `/updateUser/:id` | Update a user |
| DELETE | `/deleteUser/:id` | Delete a user |

## Prerequisites

- Node.js 18+ and npm
- MongoDB running locally on `mongodb://127.0.0.1:27017` (database `crud`)

## Configuration

The MongoDB connection string and the port (`3001`) are set in `server/index.js`. The front end calls the API at `http://localhost:3001`.

## Running locally

```bash
# 1. Back end
cd server
npm install
npm start                 # nodemon index.js → http://localhost:3001

# 2. Front end (in a second terminal)
cd clint
npm install
npm run dev               # Vite dev server, by default http://localhost:5173
```

Build the front end for production with `npm run build` inside `clint/` (output in `clint/dist`).
