# GraphQL Example with Node.js and Apollo Server

This project is a simple implementation of a GraphQL API using Node.js, Express, and Apollo Server. The API allows basic operations such as querying and adding books to a collection.

---

## 🚀 Features

- **Query books**: Retrieve a list of all books.
- **Add a book**: Add a new book to the collection.

---

## 🛠️ Prerequisites

Before starting, ensure you have the following installed:

- [Node.js](https://nodejs.org/) (version 14 or higher)
- [npm](https://www.npmjs.com/) (comes with Node.js)

---

## 📦 Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/graphql-example.git
   cd graphql-example
   ```
2. Install dependencies:
   ```bash
   npm install
   ```

## 🔧 Usage
Start the server:

```bash
npm start
```
Open your browser and navigate to:

```bash
http://localhost:4000/graphql
```
## 📖 Example Queries
Query all books
To retrieve all books, use the following query:

```graphql
Copiar código
query {
  books {
    id
    title
    author
  }
}
```
Add a new book
To add a new book to the collection, use the following mutation:

```graphql
Copiar código
mutation {
  addBook(title: "The Great Gatsby", author: "F. Scott Fitzgerald") {
    id
    title
    author
  }
}
```
Example Response (Query)
```json
Copiar código
{
  "data": {
    "books": [
      { "id": "1", "title": "1984", "author": "George Orwell" },
      { "id": "2", "title": "Brave New World", "author": "Aldous Huxley" }
    ]
  }
}
```
Example Response (Mutation)
```json
Copiar código
{
  "data": {
    "addBook": {
      "id": "3",
      "title": "The Great Gatsby",
      "author": "F. Scott Fitzgerald"
    }
  }
}
```
## 🌟 Technologies Used
- Node.js
- Express
- Apollo Server
- GraphQL
