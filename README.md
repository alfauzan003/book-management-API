# Book Management System in Golang and MySQL

This is a simple book management system implemented in Golang with a MySQL database. It allows you to perform basic CRUD (Create, Read, Update, Delete) operations on books. This project is created for learning purposes.

## Prerequisites

Before running this application, make sure you have the following prerequisites installed:

- Go (Golang): [Download Go](https://golang.org/dl/)
- MySQL: [Install MySQL](https://dev.mysql.com/downloads/installer/)

## Getting Started

1. Clone this repository to your local machine:
   ```
   git clone https://github.com/alfauzan003/book-management-API.git
   ```

2. Configure MySQL database on your machine
    - Create a MySQL database named 'BookManagement'.
    - Update the database connection settings in the pkg/config/app.go if needed.

3. Build and run the application:
    ```
    go run cmd/main/main.go
    ```

## API Endpoints
- `POST /book` : Create a new book
    - Request Body (JSON) Example:
        ```
        {
            "Name" : "Matahari",
            "Author": "Tere Liye",
            "Publication": "GPU"
        }
- `GET /book` : Get all book
- `GET /book/{bookId}` : Get a book by ID
- `PUT /book/{bookId}` : Update book
    - Request Body (JSON) Example:
        ```
        {
            "Name" : "Komet Minor",
            "Author": "Tere Liye",
            "Publication": "GPU"
        }
- `DELETE /book/{bookId}` : Delete book

## Project Structure
- `cmd/main/main.go` : The main entry point of the application.
- `pkg/config/app.go` : Database configuration and connection code.
- `pkg/controllers/book-controller.go` : Contains the controller functions for handling book-related operations.
- `pkg/models/book.go` : Defines the book model and database operations.
- `pkg/routes/bookstore-routes.go` : Registers the API routes using the Gorilla Mux router.
- `pkg/utils/utils.go` : Utility functions for parsing HTTP request bodies.