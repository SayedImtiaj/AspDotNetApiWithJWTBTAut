AspJWTBTAut
AspJWTBTAut is an ASP.NET Core web application that demonstrates JWT-based authentication and a comprehensive order management system. It supports user registration, login, and the management of orders including CRUD operations and file uploads.

Features
User Authentication: Secure JWT-based authentication system.
Order Management: Full CRUD operations for managing orders with detailed order information.
File Upload: Upload images associated with orders.
Order Details: Manage complex order structures with associated details.
API Endpoints: Example endpoints for registering, logging in users, and managing orders.
Technologies Used
ASP.NET Core: Framework for building modern web applications.
Entity Framework Core: ORM for database interactions.
JWT: For secure authentication.
SQLite: Database used for development.
Getting Started
Prerequisites
.NET Core SDK (3.1 or later)
SQLite (for development)
Visual Studio Code or Visual Studio for development
Setup
Clone the Repository

sh
Copy code
git clone https://github.com/yourusername/AspJWTBTAut.git
cd AspJWTBTAut
Install Dependencies

Restore the project dependencies by running:

sh
Copy code
dotnet restore
Configure the Database

The project uses SQLite by default. Ensure that the database is set up by running the migrations:

sh
Copy code
dotnet ef database update
Run the Application

Start the application with:

sh
Copy code
dotnet run
The application will be accessible at http://localhost:5000 (or the port specified in launchSettings.json).

API Endpoints
Authentication
Register

POST /api/authmanagement/register
Request body: UserRegistrationDto
Response: User registration details or errors
Login

POST /api/authmanagement/login
Request body: UserLoginDto
Response: JWT token for authentication
Orders
Get Orders

GET /api/order
Response: List of orders with details
Get Order by ID

GET /api/order/{orderId}
Response: Order details by ID
Create Order

POST /api/order
Request: Form data including CustomerName, OrderDate, IsComplete, ImageFile, and OrderDetail
Response: Created order with details
Update Order

PUT /api/order/{id}
Request: Form data including CustomerName, OrderDate, IsComplete, ImageFile, and OrderDetail
Response: Updated order with details
Delete Order

DELETE /api/order/{orderId}
Response: List of remaining orders
Project Structure
Controllers: API controllers for handling requests.
Models: Data models and DTOs used throughout the application.
DAL (Data Access Layer): Database context and entity configurations.
Configuration: JWT and application configuration settings.
Contributing
Contributions are welcome! To contribute:

Fork the repository
Create a new branch (git checkout -b feature-branch)
Make your changes
Commit your changes (git commit -am 'Add new feature')
Push to the branch (git push origin feature-branch)
Create a new Pull Request
License
This project is licensed under the MIT License. See the LICENSE file for details.

Contact
For questions or support, please contact your-email@example.com.
