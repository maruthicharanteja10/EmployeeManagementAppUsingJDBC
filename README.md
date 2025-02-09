# Employee Management Application using JDBC

This is a simple Java console-based Employee Management Application that demonstrates basic CRUD (Create, Read, Update, Delete) operations using JDBC with a MySQL database. The project is organized using multiple packages under `com.employeeApp`.

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Project Structure](#project-structure)
- [Requirements](#requirements)
- [Setup Instructions](#setup-instructions)
- [How to Run](#how-to-run)
- [Future Enhancements](#future-enhancements)
- [License](#license)
- [Contact](#contact)

## Overview

This application provides a basic console-based menu system to manage employee records. It allows you to:
- Add a new employee.
- Display all employees.
- Show details for a specific employee (based on ID).
- Update an employee's name.
- Delete an employee record.

The application uses a simple DAO pattern:
- **`DbConnection`**: Establishes a connection to the MySQL database.
- **`Employee`**: A Plain Old Java Object (POJO) representing an employee.
- **`EmployeeInterface`**: An interface declaring the CRUD operations.
- **`EmployeeImpl`**: The implementation of the CRUD operations.
- **`EmpTestApp`**: Contains the `main` method and the interactive menu for the user.

## Features

- **JDBC-based Database Connection:** Uses MySQL as the backend.
- **CRUD Operations:** Create, read, update, and delete employee records.
- **Console-based User Interface:** A simple menu-driven approach to interact with the application.
- **Modular Design:** Clear separation of concerns using separate classes and an interface.

## Project Structure
com.employeeApp │ ├── DbConnection.java // Manages the MySQL database connection. ├── EmpTestApp.java // Main class with the console menu. ├── Employee.java // Employee POJO. ├── EmployeeInterface.java // Interface defining CRUD methods. └── EmployeeImpl.java // Implementation of EmployeeInterface.


## Requirements

- **Java JDK 8 or higher**
- **MySQL Database**  
  The application expects a MySQL database named `employee_db` with a table `emp`.  
- **MySQL Connector/J** (JDBC driver) added to the classpath.

## Setup Instructions

1. **Database Setup:**
   - Install MySQL and create a database called `employee_db`.
   - Create a table named `emp` with the following structure (example using SQL):

     ```sql
     CREATE TABLE emp (
       eid INT PRIMARY KEY,
       ename VARCHAR(100),
       salary DOUBLE,
       age INT,
       desg VARCHAR(50)
     );
     ```

2. **Clone the Repository:**
   - Clone or download the repository from GitHub:
     ```bash
     git clone https://github.com/your-username/EmployeeManagementApp.git
     ```

3. **Configure Database Credentials (Optional):**
   - The database connection details are currently hardcoded in `DbConnection.java`:
     ```java
     String url = "jdbc:mysql://localhost:3306/employee_db";
     String user = "root";
     String psswd = "charantej@@18";
     ```
   - Modify these values as needed for your environment.

## How to Run

1. **Compile the Project:**
   - Ensure that the MySQL JDBC driver (mysql-connector-java.jar) is in your classpath.
   - From the project root, compile the source files:
     ```bash
     javac -cp .;path/to/mysql-connector-java.jar com/employeeApp/*.java
     ```
   - (On Unix/Mac, replace `;` with `:` in the classpath separator.)

2. **Run the Application:**
   - Run the main class:
     ```bash
     java -cp .;path/to/mysql-connector-java.jar com.employeeApp.EmpTestApp
     ```
   - The console menu will be displayed. Follow the on-screen instructions to add, display, update, or delete employee records.

## Future Enhancements

- **Enhanced Error Handling:** Improve exception management and user feedback.
- **Input Validation:** Add more robust validation for user inputs.
- **Configuration Externalization:** Use a properties file or environment variables for database credentials and other settings.
- **GUI Implementation:** Develop a graphical user interface (GUI) for better usability.
- **Logging:** Integrate a logging framework (e.g., Log4j or SLF4J) to replace console outputs.

## License

This project is licensed under the [MIT License](LICENSE).

## Contact

For any questions or suggestions, please contact:
- **Email:** [charantejdonthireddy@gmail.com](mailto:charantejdonthireddy@gmail.com)


