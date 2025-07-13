
# 🧑‍💼 Employee Management System (Java + GUI)

A **Java-based desktop application** for managing employee records with a graphical user interface (GUI). The system provides functionality to perform core employee-related operations like adding, updating, deleting, and searching employee records. It also allows for **pay slip generation in PDF format**, powered by JasperReports, and stores data securely using **MySQL** or **SQLite** databases.

---

## 🚀 Features

The system is designed to simplify employee administration tasks. Below are the core functionalities:

* ✅ **Add New Employees**
  Add employee records with fields like:

  * Name
  * Employee ID
  * Position/Role
  * Department
  * Salary
  * Date of Hire
  * Contact Details

* ✅ **Search Employees by ID**
  Quickly search employees using their unique ID.

* ✅ **Update Employee Information**
  Edit and update existing employee details with ease.

* ✅ **Delete Employees**
  Remove employees from the system using their Employee ID.

* ✅ **View Employee List in a Table**
  Browse a table displaying all employees, with sorting and search features.

* ✅ **Generate Pay Slips (PDF)**
  Create and export individual pay slips as PDF files using **JasperReports**.

* ✅ **Cross-Platform Support**
  Runs on Windows, Linux, and macOS using Java Runtime.

---

## 🛠️ Technologies Used

| Technology     | Purpose                           |
| -------------- | --------------------------------- |
| Java (JDK 8+)  | Core programming language         |
| Swing          | GUI creation and event handling   |
| JasperReports  | PDF pay slip generation           |
| MySQL / SQLite | Backend database for data storage |
| JDBC           | Java Database Connectivity (JDBC) |

---

## 💻 Installation & Setup

Follow these steps to set up and run the project locally:

### 🔃 Clone the Repository

```bash
git clone https://github.com/yourusername/Employee-Manager-Java.git
cd Employee-Manager-Java
```

### ☕ Install Prerequisites

Make sure the following are installed on your system:

* Java JDK 8 or later
* MySQL or SQLite
* Java IDE (Eclipse, IntelliJ IDEA, or NetBeans)

### 🗄️ Set Up the Database

* **Option 1: MySQL**

  * Create a database: `employee_db`
  * Import the provided SQL schema: `schema.sql`
  * Update database credentials in `DBConnection.java`

* **Option 2: SQLite**

  * Place the `.db` file in the project directory
  * Modify JDBC connection string accordingly

### ▶️ Run the Application

1. Open the project in your preferred IDE.
2. Build and compile the `EmployeeManagementSystem.java` file.
3. Launch the main application window.

---

## 🧭 Usage Guide

### ➕ Add Employee

* Click on the **"Add Employee"** button.
* Fill in the required fields.
* Click **Save** to insert the record into the database.

### 🔍 Search Employee

* Enter the **Employee ID** in the search box.
* Click **Search** to view employee details.

### 📝 Update Employee

* Select the employee from the table.
* Edit the details in the form.
* Click **Update** to save changes.

### ❌ Delete Employee

* Select the employee from the table.
* Click the **"Delete"** button to remove the record.

### 📄 Generate Pay Slip

* Select an employee.
* Click **"Generate PDF"**.
* Save or print the generated pay slip.

---

## 📸 Screenshots

> 📷 *Add some screenshots of your GUI here to illustrate usage.*

```
[ Add Employee Form ]
[ Search & Table View ]
[ Pay Slip PDF Example ]
```

---

## 🧪 Project Structure

```
Employee-Manager-Java/
│
├── src/
│   ├── db/
│   │   └── DBConnection.java
│   ├── gui/
│   │   ├── AddEmployeeForm.java
│   │   ├── UpdateEmployeeForm.java
│   │   └── EmployeeTable.java
│   ├── reports/
│   │   └── PaySlipReport.jrxml
│   └── EmployeeManagementSystem.java
│
├── lib/
│   ├── jasperreports-x.x.x.jar
│   └── mysql-connector-java-x.x.x.jar
│
├── resources/
│   └── schema.sql
│
└── README.md
```

---

## 🙌 Contributing

Contributions are welcome! To contribute:

1. Fork the repository.
2. Create a new branch: `git checkout -b feature-name`.
3. Make your changes.
4. Submit a pull request.

Feel free to improve features, fix bugs, or suggest enhancements!

---

## 📄 License

This project is licensed under the **MIT License**.
See the [LICENSE](LICENSE) file for more information.


