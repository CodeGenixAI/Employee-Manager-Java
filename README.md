# Employee Management System

A comprehensive desktop application developed in Java Swing to efficiently manage employee records. The system provides a user-friendly interface for administrators to handle essential employee information, from hiring to departure. It is backed by a MySQL database for reliable and persistent data storage.

## Table of Contents

- [Features](#features)
- [How to Get Started](#how-to-get-started)
  - [Prerequisites](#prerequisites)
  - [1. Database Setup](#1-database-setup)
  - [2. Project Configuration](#2-project-configuration)
  - [3. Running the Application](#3-running-the-application)
- [Project Structure](#project-structure)

## Features

This system is designed with a modular approach, where each feature is handled by a dedicated component.

#### splash Screen (`Front_page.java`)
*   **Purpose**: To provide an initial welcoming screen when the application starts.
*   **Functionality**: Displays a splash image or animation for a few seconds before automatically redirecting the user to the login screen. It creates a professional first impression.

#### User Authentication (`Login.java`)
*   **Purpose**: To secure the system and ensure only authorized users can access the data.
*   **Functionality**: Presents a login form where the user must enter a username and password. These credentials are then validated against the `login` table in the database. Access is granted only upon successful validation.

#### Central Dashboard (`Home.java`)
*   **Purpose**: To serve as the main navigation hub after a successful login.
*   **Functionality**: The home screen provides clear, clickable buttons to access all the primary functions of the application:
    *   Add Employee
    *   View Employees
    *   Update Employee
    *   Remove Employee & Generate Payslips

#### Add a New Employee (`AddEmployee.java`)
*   **Purpose**: To create new records for new hires.
*   **Functionality**: Opens a form with fields to enter employee details such as Name, Father's Name, Date of Birth, Salary, Address, Phone, Email, Education, and Designation. Upon submission, the data is saved as a new record in the `employee` table.

#### View and Manage Employees (`ViewEmployee.java`)
*   **Purpose**: To display a complete list of all employees and allow for easy searching and navigation to other functions.
*   **Functionality**: Fetches and displays all employee records from the database in a clear, scrollable table format. It includes a search bar to quickly find specific employees by their ID. From this screen, users can select an employee and choose to either update or remove them.

#### Update Employee Details (`UpdateEmployee.java`)
*   **Purpose**: To modify the information of existing employees.
*   **Functionality**: When an employee is selected from the "View Employees" screen, this module opens a form pre-filled with their current data. The user can edit any field (e.g., salary, address, phone number) and save the changes back to the database.

#### Remove an Employee (`RemoveEmployee.java`)
*   **Purpose**: To delete records of employees who have left the company.
*   **Functionality**: After an employee is selected from the "View Employees" list, this function can be triggered. It permanently deletes the employee's record from the database.

#### Generate Payslips (`PayslipPrinter.java`)
*   **Purpose**: To generate and print a payslip for an employee.
*   **Functionality**: This utility can generate a formatted document (like a PDF) containing salary and deduction details for a specific employee, which can then be printed. *(Note: Functionality may depend on external libraries for PDF generation.)*

#### Database Connectivity (`Connect.java`)
*   **Purpose**: To manage the connection between the Java application and the MySQL database.
*   **Functionality**: A centralized class that establishes and manages the JDBC connection. This is where you will need to configure your database username and password.

## How to Get Started

### Prerequisites

*   Java Development Kit (JDK 8 or higher)
*   MySQL Server
*   A Java IDE (e.g., NetBeans, IntelliJ IDEA, Eclipse)

### 1. Database Setup

This project will not work without a correctly configured database.

1.  **Create the Database**: In your MySQL instance, create a new database.
    ```sql
    CREATE DATABASE employee_management;
    ```
2.  **Create the Tables**: The project includes a SQL script with the required table schemas.
    *   Find the `EMPLOYEE.sql` file. **You must place this file inside a folder named `sql` in the project's root directory.**
    *   Execute this script within the `employee_management` database to create the `employee` and `login` tables.

### 2. Project Configuration

1.  **Open the Project**: Load the project folder into your IDE.
2.  **Configure Database Credentials**: Open the `src/employee_management/Connect.java` file. Update the username and password in the `DriverManager.getConnection()` method to match your local MySQL credentials.
    ```java
    // In Connect.java
    Connection c = DriverManager.getConnection("jdbc:mysql:///employee_management", "YOUR_USERNAME", "YOUR_PASSWORD");
    ```

### 3. Running the Application

*   **Build the project** in your IDE to compile the Java source files.
*   The main entry point for the application is **`Front_page.java`**. Run this file to start the system.

## Project Structure

```
Employee_Management_System/
├── src/
│   ├── employee_management/
│   │   ├── AddEmployee.java
│   │   ├── Connect.java
│   │   ├── Front_page.java
│   │   ├── Home.java
│   │   └── (etc...)
│   └── icons/
│       └── (icon files)
│
├── sql/
│   └── EMPLOYEE.sql   <-- Place your SQL file here
│
└── README.md
```
