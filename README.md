# FastAPI Patient Management API

A production-style REST API built with FastAPI for managing patient records. This project demonstrates CRUD operations, request validation, computed fields, query handling, and JSON-based data persistence.

---

## Features

* Create, update, delete, and view patient records
* Automatic BMI calculation using computed fields
* Health verdict generation based on BMI
* Input validation with Pydantic
* Sorting patients by height, weight, or BMI
* Query and path parameter handling
* JSON file used as lightweight storage
* Structured error handling with HTTP exceptions
* Interactive API documentation with Swagger UI

---

## Tech Stack

* Python
* FastAPI
* Pydantic v2
* Uvicorn
* UV Package Manager
* JSON

---

## Project Structure

```text id="8mjlwm"
.
├── main.py
├── patients.json
├── pyproject.toml
├── README.md
└── .gitignore
```

---

## Setup Using UV

### Install UV

```bash id="2u2s6o"
pip install uv
```

### Create Virtual Environment

```bash id="y0y5kp"
uv venv
```

### Activate Virtual Environment

#### Windows

```bash id="ajth5w"
.venv\Scripts\activate
```

#### Linux / macOS

```bash id="pym2d2"
source .venv/bin/activate
```

### Install Dependencies

```bash id="kslxfc"
uv add "fastapi[standard]"
```

---

## Run the Development Server

```bash id="7w9m76"
uv run fastapi dev main.py
```

Server URL:

```text id="j1g6jd"
http://127.0.0.1:8000
```

Swagger Documentation:

```text id="o8hl3l"
http://127.0.0.1:8000/docs
```

---

## API Endpoints

| Method | Endpoint                | Description           |
| ------ | ----------------------- | --------------------- |
| GET    | `/`                     | API Home              |
| GET    | `/about`                | About API             |
| GET    | `/view`                 | View all patients     |
| GET    | `/patient/{patient_id}` | View specific patient |
| GET    | `/sort`                 | Sort patients         |
| POST   | `/create`               | Create patient        |
| PUT    | `/edit/{patient_id}`    | Update patient        |
| DELETE | `/delete/{patient_id}`  | Delete patient        |

---

## Example Patient Data

```json id="22f8z7"
{
  "id": "P001",
  "name": "John Doe",
  "city": "Karachi",
  "age": 24,
  "gender": "male",
  "height": 1.75,
  "weight": 72
}
```

---

## Concepts Practiced

* FastAPI fundamentals
* REST API development
* CRUD operations
* Request validation
* Query and path parameters
* JSON file handling
* HTTP exception handling
* Backend project structure

Zubair
