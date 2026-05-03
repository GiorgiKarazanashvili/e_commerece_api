# E-Commerce API

RESTful API backend for a multi-tenant e-commerce platform, built with FastAPI and Tortoise ORM.

## Features

- JWT-based authentication with token refresh
- User registration with email verification
- Product CRUD with image upload
- Multi-tenant architecture (business/seller separation)
- Order management

## Tech Stack

- **Framework:** FastAPI
- **ORM:** Tortoise ORM (async, SQLite/PostgreSQL)
- **Auth:** JWT (python-jose), bcrypt password hashing
- **Email:** FastAPI-Mail for verification flows

## Project Structure

```
main.py            # App entry point, route definitions
models.py          # Tortoise ORM models (User, Product, Order)
authentication.py  # JWT creation, verification, password hashing
emails.py          # Email verification templates and sending
```

## Running

```bash
pip install fastapi tortoise-orm python-jose bcrypt fastapi-mail uvicorn
uvicorn main:app --reload
```

API docs available at `http://localhost:8000/docs` (Swagger UI).

## License

MIT
