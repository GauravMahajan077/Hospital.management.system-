
# 🏥 Hospital Management System – Java Swing + MySQL

## 📌 Overview

A Java-based standalone desktop application built using **Swing** for the GUI and **MySQL** for backend data storage.
The system offers a streamlined interface for managing patients, doctors, staff, rooms, ambulances, and appointments — all in one place.
With **real-time CRUD operations** and **structured data management**, it enhances hospital efficiency, saves time, and improves record accuracy.

## ✨ Features

* **Patient Management** – Add, view, update, and delete patient records.
* **Doctor Management** – Maintain doctor details with specialization info.
* **Staff Management** – Track and manage hospital staff roles.
* **Room & Bed Allocation** – Advanced room booking and patient allocation system.
* **Ambulance Tracking** – Maintain a log of ambulance availability and assignments.
* **Appointment Scheduler** – Book and manage appointments seamlessly.
* **Database Integration** – Persistent data storage using MySQL.

## 🛠️ Tech Stack

* **Language:** Java (JDK 8+)
* **GUI Framework:** Swing (Java Foundation Classes)
* **Database:** MySQL 8.x
* **Build Tool:** Manual compilation in VSCode / any Java IDE
* **Connector:** MySQL Connector/J (JDBC driver)

## 📂 Project Structure

```
HospitalManagementSystem/
│
├── src/
│   ├── MainWindow.java           # Main Swing GUI
│   ├── DatabaseConnection.java   # MySQL JDBC connection handler
│   ├── Patient.java              # Patient model
│   ├── Doctor.java               # Doctor model
│   ├── ... (other modules)
│
├── lib/
│   └── mysql-connector-j-<version>.jar
│
└── README.md
```

---

## ⚙️ Setup Instructions

### 1️⃣ Install Requirements

* **Java JDK 8 or later** – [Download here](https://www.oracle.com/java/technologies/javase-downloads.html)
* **MySQL Community Server** – [Download here](https://dev.mysql.com/downloads/mysql/)
* **MySQL Workbench** (optional but recommended)

### 2️⃣ Create MySQL Database & Tables

Run the following SQL in MySQL Workbench:

```sql
CREATE DATABASE HospitalDB;

USE HospitalDB;

CREATE TABLE Patients (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(50),
    age INT,
    illness VARCHAR(100)
);

CREATE TABLE Doctors (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(50),
    specialization VARCHAR(100)
);
```

### 3️⃣ Add MySQL Connector/J to Project

* Download from [MySQL Connector/J](https://dev.mysql.com/downloads/connector/j/)
* Place the `.jar` in the `lib/` folder.
* Add it to your classpath in VSCode / IDE.

### 4️⃣ Configure Database Credentials

Update **`DatabaseConnection.java`**:

```java
private static final String URL = "jdbc:mysql://localhost:3306/HospitalDB";
private static final String USER = "root";       // Your MySQL username
private static final String PASSWORD = "pass";   // Your MySQL password
```

### 5️⃣ Run the Application

```bash
javac -cp ".;lib/mysql-connector-j-8.0.xx.jar" src/*.java
java -cp ".;lib/mysql-connector-j-8.0.xx.jar;src" MainWindow
```

## 🚀 Future Enhancements

* Role-based login (Admin/Doctor/Staff)
* Patient medical history & prescriptions
* Advanced search & filtering
* Reports & data export in PDF/Excel

## 📜 License

This project is licensed under the MIT License – feel free to modify and use it for learning or development.
