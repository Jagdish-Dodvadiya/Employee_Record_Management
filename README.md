# 🧑‍💼 Employee Management System (ASP.NET Core MVC)

A modern **Employee Record Management System** built using **ASP.NET Core MVC**, designed to manage employee and department data efficiently with a clean architecture and scalable structure.

---

## 🚀 Features

* 👨‍💻 Employee Management (Create, Read, Update, Delete)
* 🏢 Department Management
* 🔍 Structured data handling using Repository Pattern
* 🗄️ SQL Server database integration
* ⚙️ Dependency Injection for loose coupling
* 🌐 MVC architecture for clean separation of concerns

---

## 🛠️ Tech Stack

| Technology            | Description                  |
| --------------------- | ---------------------------- |
| ASP.NET Core MVC      | Web framework                |
| Entity Framework Core | ORM for database operations  |
| SQL Server (LocalDB)  | Database                     |
| C#                    | Backend programming language |
| Razor Views           | Frontend UI rendering        |

---

## 📁 Project Structure

```
EmployeeManagementSystem/
│
├── Controllers/           # MVC Controllers
├── Models/                # Entity Models
├── Data/                  # DbContext
├── Repositories/          # Repository Layer
├── Views/                 # Razor Views (UI)
├── wwwroot/               # Static files (CSS, JS, Images)
│
├── Program.cs             # Application configuration
├── appsettings.json       # App configuration
└── appsettings.Development.json
```

---

## ⚙️ Configuration

### 🔗 Database Connection

The application uses SQL Server LocalDB. Update connection string if needed:

```json
"ConnectionStrings": {
  "DefaultConnection": "Server=(localdb)\\mssqllocaldb;Database=EmployeeManagementSystemDb;Trusted_Connection=True;"
}
```

📌 Source: 

---

## 🔧 Application Setup

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/your-username/EmployeeManagementSystem.git
cd EmployeeManagementSystem
```

### 2️⃣ Open in Visual Studio

* Open `.sln` file
* Ensure .NET SDK is installed

### 3️⃣ Run Migrations (if applicable)

```bash
Add-Migration InitialCreate
Update-Database
```

### 4️⃣ Run the Project

```bash
dotnet run
```

---

## 🧠 Architecture Overview

The project follows a **clean layered architecture**:

### 🔹 MVC Pattern

* **Model** → Data structure
* **View** → UI
* **Controller** → Business logic handling

### 🔹 Repository Pattern

* Abstraction over data access
* Improves maintainability and testability

Registered in `Program.cs`:

```csharp
builder.Services.AddScoped<IEmployeeRepository, EmployeeRepository>();
builder.Services.AddScoped<IDepartmentRepository, DepartmentRepository>();
```

📌 Source: 

---

## ⚙️ Middleware & Configuration

Key configurations from `Program.cs`:

* MVC setup
* SQL Server DbContext
* Routing configuration
* HTTPS redirection
* Static file mapping

```csharp
app.MapControllerRoute(
    name: "default",
    pattern: "{controller=Home}/{action=Index}/{id?}");
```

📌 Source: 

---

## 📊 Logging

Basic logging configuration:

```json
"LogLevel": {
  "Default": "Information",
  "Microsoft.AspNetCore": "Warning"
}
```

📌 Source: 

---

## 📌 Future Enhancements

* 🔐 Authentication & Authorization (Identity)
* 📊 Dashboard & Analytics
* 📁 File Upload (Employee Documents)
* 🔎 Search & Filtering
* 🌍 REST API integration
* 📱 Responsive UI improvements

---

## 🤝 Contributing

Contributions are welcome! Feel free to fork the repo and submit a pull request.

---

## 📧 Contact

For any queries or suggestions:

* 📩 Email: [jagdishdodvadiya545@gmail.com](mailto:your-email@example.com)
* 💼 LinkedIn: https://linkedin.com/in/jagdish-dodvadiya
* 💻 GitHub: https://github.com/Jagdish-Dodvadiya

---

## ⭐ Acknowledgements

Built with ❤️ using ASP.NET Core MVC to demonstrate real-world CRUD operations and scalable architecture for beginner-to-intermediate developers.

---
