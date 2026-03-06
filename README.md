# CafOrSystem - Cafe Management System

This project is a modern Blazor Web App application developed to digitalize a cafe’s product, category, employee, and customer management.

## Features
- Product Management: Adding, updating, and deleting products on the menu
- Category System: Grouping products by categories and tracking relational data
- Visual Home Page: Pastry and coffee themed content welcoming the user
- Relational Database: Foreign Key relationships between tables and data management with EF Core
- Sample Data: Sample category/product/customer/employee/order data is included in the SQL script

## Technologies Used
- Framework: .NET 8 / Blazor Web App
- ORM: Entity Framework Core (Database-First)
- Database: Microsoft SQL Server

## Setup and Run

### 1) Opening the project files
Project files are included in this repo as a zip:
- Download `Caf-Orzip.zip`
- Extract the zip
- Open the `CMPE232.sln` file in the extracted folder with Visual Studio

### 2) Database Setup
1. Create a database named `CafOrSystem` on SQL Server.
2. Open the `Caforsql.sql` file located inside the project folder/ZIP in SSMS.
3. Run the script to create the tables and sample data.

### 3) Connection String Settings
Update the connection string in `SengWeb/appsettings.json` and/or `SengWeb/appsettings.Development.json` according to your computer.

Example:

"ConnectionStrings": {
  "SengWebContext": "Server=DESKTOP-PQ9II1K\\SQLEXPRESS;Database=CafOrSystem;Trusted_Connection=True;MultipleActiveResultSets=true;TrustServerCertificate=True;"
}
### Notes
- `Server=...\\SQLEXPRESS` part differs from computer to computer.
- If your SQL Server instance name is different, edit accordingly (e.g. `localhost\\SQLEXPRESS`).

### Running the Project
- Open `CMPE232.sln` in Visual Studio.
- Build > Rebuild Solution
- Start the application with F5.
- `SengWeb` must be selected as the Startup project.

### Presentation / Explanation Notes
- Data Connectivity: Database connection is provided via `ConnectionStrings -> SengWebContext`.
- SQL Script: `Caforsql.sql` contains both the schema and the sample data.
