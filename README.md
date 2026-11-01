# Expense Tracker with Graphs

A full-stack expense management mini-project built with **React + Vite**, **Node.js + Express**, **MySQL**, **JWT authentication**, and **Chart.js**.

Users can register and log in, manage expenses and categories, filter and search transactions, view monthly and category-wise charts, and track a budget.

## Project structure
- `frontend/` — React + Vite interface, charts, pages, components, and API services
- `backend/` — Express REST API, authentication, expense/category/dashboard routes, validation, and tests
- `database/schema.sql` — MySQL database and table definitions
- `docs/` — project overview, API reference, and screenshot notes
- `postman/` — API request collection

## Requirements
- Node.js 18 or newer
- MySQL 8.x
- npm

## Setup

### 1. Create the database
Run from the project root in PowerShell:
```powershell
mysql -u root -p -e "source database/schema.sql"
```

### 2. Configure and start the backend
```powershell
cd backend
Copy-Item .env.example .env
```
Edit `backend/.env` with your MySQL credentials and a long random `JWT_SECRET`, then run:
```powershell
npm install
npm run dev
```
The API defaults to `http://localhost:5000`. Health check: `http://localhost:5000/api/health`.

### 3. Start the frontend
In a separate terminal:
```powershell
cd frontend
npm install
npm run dev
```
Open `http://localhost:5173`.

### 4. Tests
With the backend running:
```powershell
cd backend
npm run test:api
```

## Environment safety
Create local `.env` files from the provided `.env.example` templates. Do not commit real database passwords or JWT secrets. Dependencies (`node_modules`) are not included in Git.

## Team
- Kalpesh Parkhe — Roll No. 36
- Aniket Patil — Roll No. 37
- Bhupendra Patil — Roll No. 38

See `docs/API.md` and `docs/PROJECT_OVERVIEW.md` for more information.
