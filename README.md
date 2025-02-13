# 📚 FastAPI Book Management API

## 📝 Overview
This project is a **RESTful API** built with **FastAPI** for managing a book collection. It provides full **CRUD (Create, Read, Update, Delete) operations**, ensuring robust input validation, error handling, and automatic API documentation.

## 🚀 Features
- 📖 **Book Management**: Perform CRUD operations
- 🛠 **Input Validation**: Ensures data integrity using Pydantic models
- 🔍 **Genre Classification**: Uses enums for genre validation
- 🌍 **CORS Support**: Secure cross-origin requests enabled
- 📑 **Auto-Generated API Docs**: Available via FastAPI's built-in UI
- ✅ **Test Coverage**: Unit tests for API endpoints

## 🏗 Project Structure
```
fastapi-book-project/
├── api/
│   ├── db/
│   │   ├── __init__.py
│   │   └── schemas.py      # Data models and in-memory database
│   ├── routes/
│   │   ├── __init__.py
│   │   └── books.py        # Book route handlers
│   └── router.py           # API router configuration
├── core/
│   ├── __init__.py
│   └── config.py           # Application settings
├── tests/
│   ├── __init__.py
│   └── test_books.py       # API endpoint tests
├── main.py                 # Application entry point
├── requirements.txt        # Dependencies
└── README.md               # Project documentation
```

## 🛠 Technologies Used
- **Python 3.12**
- **FastAPI** (for the API framework)
- **Pydantic** (for data validation)
- **pytest** (for testing)
- **Uvicorn** (ASGI server)

## 📥 Installation
1. **Clone the repository**:
   ```bash
   git clone https://github.com/hng12-devbotops/fastapi-book-project.git
   cd fastapi-book-project
   ```
2. **Create and activate a virtual environment**:
   ```bash
   python -m venv venv
   source venv/bin/activate  # Windows: venv\Scripts\activate
   ```
3. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

## ▶ Running the Application
Start the FastAPI server:
```bash
uvicorn main:app --reload
```

### 🌐 Access API Documentation
- **Swagger UI**: [http://localhost:8000/docs](http://localhost:8000/docs)
- **ReDoc**: [http://localhost:8000/redoc](http://localhost:8000/redoc)

## 🔗 API Endpoints

### 📘 Books
| Method | Endpoint                  | Description           |
|--------|---------------------------|-----------------------|
| GET    | `/api/v1/books/`          | Get all books        |
| GET    | `/api/v1/books/{book_id}` | Get a specific book  |
| POST   | `/api/v1/books/`          | Add a new book       |
| PUT    | `/api/v1/books/{book_id}` | Update book details  |
| DELETE | `/api/v1/books/{book_id}` | Remove a book        |

### 🩺 Health Check
| Method | Endpoint         | Description          |
|--------|-----------------|----------------------|
| GET    | `/healthcheck`  | Check API status    |

## 📑 Book Schema
```json
{
  "id": 1,
  "title": "Book Title",
  "author": "Author Name",
  "publication_year": 2024,
  "genre": "Fantasy"
}
```

### 🎭 Available Genres
- `Science Fiction`
- `Fantasy`
- `Horror`
- `Mystery`
- `Romance`
- `Thriller`

## ✅ Running Tests
To run unit tests:
```bash
pytest
```

## ⚠️ Error Handling
The API properly handles errors, including:
- **Non-existent books** (404 Not Found)
- **Invalid book IDs** (400 Bad Request)
- **Incorrect genre types** (422 Unprocessable Entity)
- **Malformed requests** (422 Validation Error)

## 🤝 Contributing
1. **Fork the repository**
2. **Create a new feature branch**:
   ```bash
   git checkout -b feature/new-feature
   ```
3. **Commit your changes**:
   ```bash
   git commit -m "Add new feature"
   ```
4. **Push to your branch**:
   ```bash
   git push origin feature/new-feature
   ```
5. **Open a Pull Request**

## 📜 License
This project is licensed under the **MIT License**. See the [LICENSE](LICENSE) file for details.

## 📧 Support
For issues and inquiries, please open an issue on the **GitHub repository**.

