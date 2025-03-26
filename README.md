# Fullstack App - README

This project consists of a **FastAPI backend** and a **React (Vite) frontend**. Follow the steps below to set up and run the application.


---

## Backend Setup (FastAPI)

### 1. Navigate to the backend directory:
```sh
cd backend
```

### 2. Create and activate a virtual environment:
#### macOS/Linux:
```sh
python3 -m venv venv
source venv/bin/activate
```
#### Windows:
```sh
python -m venv venv
venv\Scripts\activate
```

### 3. Install dependencies:
```sh
pip install -r requirements.txt
```

### 4. Run the backend server:
```sh
uvicorn main:app --host 0.0.0.0 --port 8000 --reload
```

### 5. Access the API:
- Open `http://localhost:8000/docs` for interactive API docs.
- Open `http://localhost:8000/` for the base endpoint.

---

## Frontend Setup (React + Vite)

### 1. Navigate to the frontend directory:
```sh
cd frontend
```

### 2. Install dependencies:
```sh
npm install
```

### 3. Start the development server:
```sh
npm run dev
```

### 4. Open the application:
- The frontend runs on `http://localhost:5173/` by default.

---

## Connecting Frontend & Backend
Modify the **frontend fetch URL** inside `frontend/src/App.js` (or equivalent file):
```js
fetch("http://localhost:8000/")
```
Ensure both backend and frontend are running before testing the app.

---

## Running with Docker (Optional)
If you prefer using **Docker**, follow these steps:

### 1. Build and start the services:
```sh
docker-compose up --build
```

### 2. Stop the services:
```sh
docker-compose down
```

---

## Troubleshooting
- **Backend not responding?** Check if `uvicorn` is running on `8000`.
- **Frontend errors?** Ensure the correct API URL is used.
- **CORS issues?** Adjust FastAPI CORS settings if needed.

---

Happy Coding! 🚀