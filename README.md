# 🚀 FastAPI CRUD API  
This project is a FastAPI-based REST API that allows you to perform CRUD (Create, Read, Update, Delete) operations on a `User` model using SQLAlchemy. It includes endpoints to create, retrieve, update, and delete user data.  

---

## ✅ Features  
✔️ **CRUD Operations**  
- Create, retrieve, update, and delete users through RESTful endpoints.  

✔️ **Database Integration**  
- Uses **SQLAlchemy** for ORM-based interaction with the database.  

✔️ **Swagger and Redoc Documentation**  
- Automatically generated API documentation available at `/docs` and `/redoc`.  

✔️ **Fast Execution**  
- Built with FastAPI for high performance and low latency.  

---

## 🏗️ Project Structure  
```plaintext
├── __init__.py
├── .env   
├── main.py  
├── models.py  
├── database.py  
├── schemas.py
├── requirements.txt
├── README.md      
└── crud.py  
```
---

## 🛠️ Tech Stack
##### Backend: FastAPI
##### ORM: SQLAlchemy
##### Database: PostgreSQL / SQLite (configurable)
##### Documentation: Swagger, Redoc
##### Environment Management: Python venv

## 🛠️ Setup Instructions

### 1. **Clone the repository**:
```bash
git clone https://github.com/Shilpa3107/RealWorldApiToFastApi.git
cd RealWorldApiToFastApi
```
### 2. Create and activate a virtual environment:

##### Create virtual environment
```bash
python -m venv venv
```

##### Activate virtual environment
## For Windows:
``` bash
.\venv\Scripts\activate
```
### 3. Install dependencies:
```bash
pip install -r requirements.txt
```
### 4. Set up the database
Create a .env file and add the following:
```bash
DATABASE_URL=postgresql://user:password@localhost/dbname
```
### 5. Run the API:
```bash
uvicorn main:app --host 127.0.0.1 --port 8000 --reload
```
## 🌐 API Endpoints
| Method | Endpoint      | Description               |
|--------|--------------|---------------------------|
| GET    | `/`          | Check if the API is running |
| POST   | `/users`     | Create a new user           |
| GET    | `/users`     | Get a list of all users     |
| PUT    | `/users/{id}` | Update an existing user     |
| DELETE | `/users/{id}` | Delete a user               |

## 📝 Example Request and Response
| Action             | Request Example | Response Example |
|--------------------|----------------|------------------|
| **Create a new user** | ``` curl -X POST "http://127.0.0.1:8000/users" -H "Content-Type: application/json" -d '{  "name": "John Doe",<br>  "email": "john@example.com"}'``` | ```{  "id": 1,  "name": "John Doe",  "email": "john@example.com"}``` |
| **Get all users**   | ``` curl -X GET "http://127.0.0.1:8000/users"``` | ```[  {    "id": 1,<br>    "name": "John Doe",<br>    "email": "john@example.com"  }]``` |
| **Update a user**   | ``` curl -X PUT "http://127.0.0.1:8000/users/1" -H "Content-Type: application/json" -d '{  "name": "Jane Doe",  "email": "jane@example.com"}'``` | ```{  "id": 1,  "name": "Jane Doe",  "email": "jane@example.com"}``` |
| **Delete a user**   | ``` curl -X DELETE "http://127.0.0.1:8000/users/1"``` | ```{  "id": 1,  "name": "Jane Doe",  "email": "jane@example.com"}``` |

## 📄 Swagger and Redoc
Swagger UI: http://127.0.0.1:8000/docs
ReDoc: http://127.0.0.1:8000/redoc

## 🌟 Future Improvements
✅ Add authentication and authorization.
✅ Add pagination for large data sets.
✅ Implement better error handling and logging.

## 🤝 Contributing
Feel free to fork the repository, create a new branch, and submit a pull request!
