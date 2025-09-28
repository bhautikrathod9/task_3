# Books REST API

A simple Node.js + Express REST API for managing books with CRUD operations. Books are stored in memory.

## 🚀 Getting Started

### Prerequisites
- Node.js installed on your machine
- npm (comes with Node.js)

### Installation

1. **Create project directory**
   ```bash
   mkdir books-api
   cd books-api
   ```

2. **Initialize npm and install dependencies**
   ```bash
   npm init -y
   npm install express
   ```

3. **Create server.js file**
   - Copy the provided server code into `server.js`

4. **Run the server**
   ```bash
   node server.js
   ```

The server will start on `http://localhost:3000`

## 📚 API Endpoints

| Method | Endpoint | Description | Body |
|--------|----------|-------------|------|
| GET | `/books` | Get all books | - |
| GET | `/books/:id` | Get book by ID | - |
| POST | `/books` | Create new book | `{"title": "Book Title", "author": "Author Name"}` |
| PUT | `/books/:id` | Update book by ID | `{"title": "New Title", "author": "New Author"}` |
| DELETE | `/books/:id` | Delete book by ID | - |

## 🧪 Testing the API

### Using curl

**Get all books:**
```bash
curl http://localhost:3000/books
```

**Get single book:**
```bash
curl http://localhost:3000/books/1
```

**Create new book:**
```bash
curl -X POST http://localhost:3000/books \
  -H "Content-Type: application/json" \
  -d '{"title": "Clean Code", "author": "Robert C. Martin"}'
```

**Update book:**
```bash
curl -X PUT http://localhost:3000/books/1 \
  -H "Content-Type: application/json" \
  -d '{"title": "The Hobbit: An Unexpected Journey"}'
```

**Delete book:**
```bash
curl -X DELETE http://localhost:3000/books/2
```

### Using Postman

1. **GET all books** → `GET http://localhost:3000/books`
2. **GET single book** → `GET http://localhost:3000/books/1`
3. **POST new book** → `POST http://localhost:3000/books`
   - Body (JSON): `{"title": "Clean Code", "author": "Robert C. Martin"}`
4. **PUT update book** → `PUT http://localhost:3000/books/1`
   - Body (JSON): `{"title": "The Hobbit: An Unexpected Journey"}`
5. **DELETE book** → `DELETE http://localhost:3000/books/2`

## 📋 Sample Data

The API comes with 2 sample books:
- The Hobbit by J.R.R. Tolkien (ID: 1)
- 1984 by George Orwell (ID: 2)

