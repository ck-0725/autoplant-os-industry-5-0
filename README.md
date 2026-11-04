# AutoPlant OS 5.0 — Industry 5.0 Smart Factory Management System

**Academic mini-project | Team of four**

## Overview
AutoPlant OS 5.0 is a smart-factory management prototype with a browser-based interface, a FastAPI backend, and a PostgreSQL database. The application includes role-oriented workflows for workers, managers, and administrators.

## Technologies
- Frontend: HTML, CSS, JavaScript, Web Speech API
- Backend: Python, FastAPI, psycopg2
- Database: PostgreSQL

## Repository Structure
- `autoplant-os-light-theme.html` — main user interface
- `backend/main.py` — FastAPI API and database access
- `database/industry5db.sql` — database schema and **demo** seed data
- `backend/.env.example` — sample database configuration (no real credentials)
- `requirements.txt` — Python dependencies

## Local Setup
1. Install Python and PostgreSQL.
2. Create a PostgreSQL database for the project.
3. Import `database/industry5db.sql` into that database. **Warning:** the script drops and recreates tables; use only a disposable development database.
4. Copy `backend/.env.example` to `backend/.env` and enter your **local** database credentials. Never commit `.env`.
5. Create and activate a Python virtual environment, then run `pip install -r requirements.txt`.
6. From the `backend` directory, run `uvicorn main:app --reload`.
7. Open `http://127.0.0.1:8000/` in your browser if the backend serves the frontend, or follow your local frontend setup. Confirm that the UI can reach the API.

## Project Notes and Security
- The SQL script contains fictional sample employees and **public demo passwords**. Do not reuse these passwords in any real system.
- The current prototype checks plaintext passwords in its login query and passes login parameters in a URL. **It is not production-ready.** A deployed version should hash passwords, use request bodies over HTTPS, restrict CORS, and implement proper authentication/authorization.
- The project has not been executed or end-to-end tested during this packaging step.

## Team and Contributions
Developed as an academic mini-project by a **four-member team**. Add the four team members and their actual contributions here with their agreement before publishing.
