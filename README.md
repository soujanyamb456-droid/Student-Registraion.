# 💰 Expense Tracker

A beginner-friendly **Full Stack Expense Tracker** application built with **React, Vite, Express.js, SQLite, and better-sqlite3**. The application helps users record daily expenses, view monthly spending summaries, filter expenses by category, and manage expense records through a simple and responsive interface.

---

# 🚀 Features

## Backend

- Express.js REST API
- SQLite database using **better-sqlite3**
- Automatic database and table creation
- Create new expense
- Read all expenses
- Update existing expense
- Delete expense
- Category filtering
- Month-wise filtering
- Pagination support
- Monthly expense summary by category
- JSON-based API responses
- CORS enabled for frontend communication

---

## Frontend

- Add new expenses
- Input validation
- Monthly summary dashboard
- Category-wise spending visualization
- Filter expenses by category
- Delete expenses
- Pagination
- Responsive UI
- Loading indicators
- Error handling using try/catch

---

# 🛠 Tech Stack

### Frontend

- React
- Vite
- JavaScript (ES6)
- CSS

### Backend

- Node.js
- Express.js
- better-sqlite3
- CORS

### Database

- SQLite (`data.db`)

---

# 📂 Project Structure

```
Expense-Tracker/
│
├── backend/
│   ├── index.js
│   ├── package.json
│   └── data.db (created automatically)
│
└── frontend/
    ├── src/
    │   ├── App.jsx
    │   ├── App.css
    │   ├── main.jsx
    │   └── index.css
    └── package.json
```

---

# ⚙️ Installation

## Clone the Repository

```bash
git clone https://github.com/your-username/expense-tracker.git
cd expense-tracker
```

---

## Install Backend Dependencies

```bash
cd backend
npm install
```

---

## Start Backend Server

```bash
node index.js
```

The backend server runs on:

```
http://localhost:5000
```

---

## Install Frontend Dependencies

Open a new terminal.

```bash
cd frontend
npm install
```

---

## Start Frontend

```bash
npm run dev
```

The frontend runs on:

```
http://localhost:5173
```

---

# 🗄 Database Schema

The application automatically creates a SQLite database named:

```
data.db
```

### expenses Table

| Column | Type | Description |
|---------|------|-------------|
| id | INTEGER | Primary Key |
| title | TEXT | Expense title |
| amount | REAL | Expense amount |
| category | TEXT | Expense category |
| date | TEXT | Expense date |
| created_at | TEXT | Record creation timestamp |

---

# 📡 REST API Endpoints

## 1. Create Expense

**POST**

```
POST /expenses
```

Request Body

```json
{
  "title": "Groceries",
  "amount": 450.50,
  "category": "Food",
  "date": "2026-07-06"
}
```

---

## 2. Get Expenses

**GET**

```
GET /expenses
```

### Optional Query Parameters

| Parameter | Description |
|-----------|-------------|
| page | Page number |
| limit | Records per page |
| category | Filter by category |
| month | Filter by month (YYYY-MM) |

Example

```
GET /expenses?page=1&limit=10&category=Food&month=2026-07
```

---

## 3. Monthly Summary

**GET**

```
GET /expenses/summary
```

Example

```
GET /expenses/summary?month=2026-07
```

Returns:

- Category-wise totals
- Grand total spending

---

## 4. Update Expense

**PUT**

```
PUT /expenses/:id
```

Example

```json
{
    "amount": 700
}
```

Only the supplied fields are updated.

---

## 5. Delete Expense

**DELETE**

```
DELETE /expenses/:id
```

Deletes the selected expense.

---

# 📌 Expense Categories

- 🍔 Food
- 🚌 Transport
- 💡 Bills
- 🎬 Entertainment
- 📦 Other

---

# 💻 User Interface

The application contains three main sections:

### ➜ Add Expense

- Title
- Amount
- Category
- Date
- Validation
- Submit button

---

### ➜ Monthly Summary

- Month selector
- Category-wise spending bars
- Grand total
- Empty state handling

---

### ➜ Expense List

- Category filter
- Expense details
- Delete option
- Pagination
- Loading indicator

---

# ▶ Running the Project

### Backend

```bash
cd backend
node index.js
```

### Frontend

```bash
cd frontend
npm run dev
```

Visit:

```
http://localhost:5173
```

---

# 📚 Learning Outcomes

This project demonstrates:

- React Functional Components
- React Hooks (`useState`, `useEffect`)
- Fetch API
- RESTful API Development
- Express.js Routing
- SQLite Database Operations
- CRUD Operations
- SQL Aggregation (`SUM`, `GROUP BY`)
- Pagination
- Filtering
- Client–Server Communication
- Form Validation
- Responsive CSS Design

---

# 🔮 Future Enhancements

- Edit expenses from the UI
- Search expenses by title
- Expense charts using Chart.js
- User authentication
- Export expenses to CSV/PDF
- Dark mode
- Mobile-first improvements

---

# 👨‍💻 Author

Developed as a beginner-friendly **Full Stack Expense Tracker** project using **React, Express.js, SQLite, and better-sqlite3** for learning CRUD operations, REST APIs, and full-stack web development.
