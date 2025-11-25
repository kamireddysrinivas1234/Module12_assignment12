# FastAPI User & Calculation Service

This project implements:

- **User registration and login**
- **Auth-protected calculation CRUD endpoints**
- A simple **web calculator UI** at the root (`/`) that:
  - Logs in to the API
  - Calls the `/calculations/` endpoint behind the scenes

It also includes:

- SQLAlchemy models and Pydantic schemas  
- A small **factory pattern** for calculation logic  
- **pytest** integration tests with coverage  
- **GitHub Actions CI/CD** (tests + optional Docker Hub push)

A demo user is **seeded automatically** on startup:

- `username`: `demo`  
- `password`: `Test123!`  

---

## 1. Prerequisites

- Python 3.12 (3.11+ is fine if you tweak the workflow)
- Git
- (Optional) Docker
- (Optional) GitHub repo + Docker Hub account for CI/CD

---

## 2. Local Setup & Running the App

From the project root:

```bash
python -m venv .venv
# Windows:
.venv\Scripts\activate
# macOS/Linux:
# source .venv/bin/activate

pip install --upgrade pip
pip install -r requirements.txt
Run the FastAPI app:

bash
Copy code
python -m uvicorn app.main:app --reload
The server will start at:

API & calculator UI: http://127.0.0.1:8000/

OpenAPI docs: http://127.0.0.1:8000/docs

ReDoc: http://127.0.0.1:8000/redoc

On first startup a SQLite database (app.db) is created and a demo user demo/Test123! is seeded.