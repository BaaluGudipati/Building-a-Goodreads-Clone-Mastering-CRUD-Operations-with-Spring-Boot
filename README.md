Goodreads Clone - Mastering CRUD Operations with Spring Boot
Overview
The Goodreads Clone is a Spring Boot application designed to replicate the basic functionalities of the popular book discovery platform, Goodreads. This project demonstrates how to create, read, update, and delete (CRUD) operations using REST APIs, making it an excellent learning resource for mastering Spring Boot.

Features
Create New Books: Add new books with essential attributes like id, name, and imageUrl.
Read Books: Fetch all books or retrieve details of a specific book.
Update Books: Modify existing book details.
Delete Books: Remove books from the system.
Error Handling: Proper exception handling with meaningful HTTP response codes.
Tech Stack
Language: Java
Framework: Spring Boot
Build Tool: Maven
Database: HashMap (in-memory data storage)
API Testing Tool: Postman/Browser for testing HTTP requests
Getting Started
Prerequisites
Ensure the following tools are installed on your system:

Java JDK 11 or higher
Maven
Git
An IDE (e.g., IntelliJ IDEA, Eclipse, or VS Code)
Clone the Repository
bash
Copy code
git clone https://github.com/BaaluGudipati/Building-a-Goodreads-Clone-Mastering-CRUD-Operations-with-Spring-Boot.git
cd Building-a-Goodreads-Clone-Mastering-CRUD-Operations-with-Spring-Boot
Run the Application
Navigate to the project directory:
bash
Copy code
cd goodreads
Build the project using Maven:
bash
Copy code
mvn clean install
Run the Spring Boot application:
bash
Copy code
mvn spring-boot:run
The application will start at http://localhost:8080.

Endpoints
1. Get All Books
URL: /books
Method: GET
Response:
json
Copy code
[
  {
    "id": 1,
    "name": "Book Name",
    "imageUrl": "URL"
  }
]
2. Get a Specific Book
URL: /books/{bookId}
Method: GET
Path Parameter: bookId (integer)
Response:
json
Copy code
{
  "id": 1,
  "name": "Book Name",
  "imageUrl": "URL"
}
3. Add a New Book
URL: /books
Method: POST
Body:
json
Copy code
{
  "id": 1,
  "name": "Book Name",
  "imageUrl": "URL"
}
4. Update a Book
URL: /books/{bookId}
Method: PUT
Body:
json
Copy code
{
  "name": "Updated Book Name",
  "imageUrl": "Updated URL"
}
5. Delete a Book
URL: /books/{bookId}
Method: DELETE
6. Error Handling
If a book is not found, the API returns:

Status Code: 404 Not Found
Response:
json
Copy code
{
  "message": "Book not found"
}
Project Structure
bash
Copy code
goodreads/
│
├── src/main/java/com/example/goodreads/
│   ├── model/
│   │   └── Book.java                # Book model class
│   ├── service/
│   │   └── BookService.java         # Business logic
│   ├── controller/
│   │   └── BookController.java      # Handles HTTP requests
│   └── repository/
│       └── BookRepository.java      # Interface for abstraction
│
├── src/main/resources/
│   ├── application.properties       # Spring Boot configuration
│
├── pom.xml                          # Maven dependencies
└── README.md                        # Project documentation
