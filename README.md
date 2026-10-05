# Alfido Tech - Task 1: RESTful API

A CRUD REST API built with Node.js, Express.js and MongoDB/Mongoose.

## Features

- GET all products
- GET a single product
- POST a new product
- PUT a product
- PATCH product fields
- DELETE a product
- Mongoose schema validation
- Error handling
- Basic request logging with Morgan
- Environment variables using dotenv

## Requirements

Install these before running:

- Node.js
- npm
- MongoDB (local) OR a MongoDB Atlas connection

## 1. Install dependencies

Open a terminal inside this project folder:

```bash
npm install
```

## 2. Configure environment variables

Copy `.env.example` and rename the copy to `.env`.

For local MongoDB:

```env
PORT=5000
MONGO_URI=mongodb://127.0.0.1:27017/alfido_task1
```

For MongoDB Atlas, replace `MONGO_URI` with your Atlas connection string.

Do NOT upload `.env` to GitHub.

## 3. Start MongoDB

If you are using MongoDB locally, make sure MongoDB is running.

## 4. Run the API

Development mode:

```bash
npm run dev
```

Normal mode:

```bash
npm start
```

You should see:

```text
MongoDB connected successfully
Server running at http://localhost:5000
```

## 5. Test the API

Health check:

```text
GET http://localhost:5000/api/health
```

Products:

```text
GET    http://localhost:5000/api/products
GET    http://localhost:5000/api/products/:id
POST   http://localhost:5000/api/products
PUT    http://localhost:5000/api/products/:id
PATCH  http://localhost:5000/api/products/:id
DELETE http://localhost:5000/api/products/:id
```

## Example POST body

```json
{
  "name": "Wireless Mouse",
  "description": "Ergonomic wireless mouse",
  "price": 799,
  "category": "Electronics",
  "inStock": true
}
```

## Suggested submission screenshots

Take screenshots of:

1. Project folder/code in VS Code
2. `.env.example` (not `.env`)
3. MongoDB database/collection
4. GET request in Postman
5. POST request in Postman
6. PUT/PATCH request in Postman
7. DELETE request in Postman
8. Terminal showing server + MongoDB connection

## Deliverables

- GitHub repository containing the server code
- README.md
- Postman collection
- `.env.example`

Do not upload `.env` or MongoDB credentials.