# 🏫 College Automation System 🎓

A **Java-based College Automation System** built using **NetBeans IDE** and **MySQL**, designed to automate and manage college operations efficiently.
This project is part of the **BCA Final Year Project** and includes **ER diagrams**, **database scripts**, and a **detailed project report**.

---

## 📌 Project Overview

The **College Automation System** provides a secure and user-friendly platform where:

* 🧑‍💼 **Admins** can manage students, teachers, subjects, fees, and leave requests.
* 🧑‍🎓 **Students** can register, view subjects, submit leave, and check marks & fees.
* 👨‍🏫 **Teachers** can manage leave, enter marks, and interact with student data.

The project uses **Java Swing** for GUI and **MySQL** for backend data storage, ensuring reliability and fast performance.

---

## ✨ Features

### 🧑‍💼 Admin Panel

* Add / Update / Delete Students & Teachers
* Manage Subjects, Marks, and Fees
* Approve / Track Leave Requests
* View Reports for Students and Teachers

### 🧑‍🎓 Student Module

* Register & Login
* View Subjects & Marks
* Apply for Leave
* Check Fee Details

### 👨‍🏫 Teacher Module

* Manage Leave Requests
* Enter Student Marks
* View Assigned Subjects

### 🧠 Database Integration

* 🔐 Secure MySQL Database
* 📝 Real-time Data Management
* 📊 ER Diagrams + Full Project Documentation

---

## 🛠️ Tech Stack

| Component        | Technology            |
| ---------------- | --------------------- |
| 💻 Frontend      | Java Swing (NetBeans) |
| 🗄️ Backend      | MySQL                 |
| 🧠 IDE           | NetBeans              |
| 📝 Language      | Java (JDK 8+)         |
| 🔐 DB Connection | JDBC                  |

---

## 📂 Project Structure

```
College-Automation-System/
├─ nbproject/
├─ src/
│  └─ collegeautomation/ # Java source files (Admin, Student & Teacher Modules)
├─ dist/
├─ database/
│  └─ collegemanagementsystem.sql
├─ report/
│  ├─ Project-Report.pdf
│  └─ ER-Diagram.pdf
├─ screenshots/
├─ README.md
└─ .gitignore
```

---

## 📊 ER Diagram

📌 **[View ER Diagram (PDF)](./report/ER-Diagram.pdf)**

---

## 📘 Project Report

📄 **[Download Full Project Report (PDF)](./report/Project-Report.pdf)**

The report includes:

* Problem Definition
* Objective
* Existing & Proposed System
* System Design (DFD, ERD, Schema)
* Implementation Details
* Output Screenshots
* Conclusion

---

## 🧰 Database

### **Database Name:** `collegemanagementsystem`

#### **Tables and Sample Data:**

```sql
-- Login Table
create table login (
    username varchar(25),
    password varchar(25)
);
insert into login values('admin', '12345');

-- Student Table
create table student (
    name varchar(40),
    fname varchar(40),
    rollno varchar(20),
    dob varchar(40),
    address varchar(100),
    phone varchar(20),
    email varchar(40),
    class_x varchar(20),
    class_xii varchar(20),
    aadhar varchar(20),
    course varchar(40),
    branch varchar(40)
);

-- Teacher Table
create table teacher (
    name varchar(40),
    fname varchar(40),
    empId varchar(20),
    dob varchar(40),
    address varchar(100),
    phone varchar(20),
    email varchar(40),
    class_x varchar(20),
    class_xii varchar(20),
    aadhar varchar(20),
    education varchar(40),
    department varchar(40)
);

-- Student Leave Table
create table studentleave (
    rollno varchar(20),
    date varchar(50),
    duration varchar(20)
);

-- Teacher Leave Table
create table teacherleave (
    empId varchar(20),
    date varchar(50),
    duration varchar(20)
);

-- Subject Table
create table subject (
    rollno varchar(20),
    semester varchar(20),
    subject1 varchar(50),
    subject2 varchar(50),
    subject3 varchar(50),
    subject4 varchar(50),
    subject5 varchar(50)
);

-- Marks Table
create table marks (
    rollno varchar(20),
    semester varchar(20),
    marks1 varchar(50),
    marks2 varchar(50),
    marks3 varchar(50),
    marks4 varchar(50),
    marks5 varchar(50)
);

-- Fee Table
create table fee (
    course varchar(20),
    semester1 varchar(20),
    semester2 varchar(20),
    semester3 varchar(20),
    semester4 varchar(20),
    semester5 varchar(20),
    semester6 varchar(20),
    semester7 varchar(20),
    semester8 varchar(20)
);

insert into fee values("BTech", "48000", "43000", "43000", "43000", "43000", "43000", "43000", "43000");
insert into fee values("Bsc", "40000", "35000", "35000", "35000", "35000", "35000", "", "");
insert into fee values("BCA", "35000", "34000", "34000", "34000", "34000", "34000", "", "");
insert into fee values("MTech", "65000", "60000", "60000", "60000", "", "", "", "");
insert into fee values("MSc", "47500", "45000", "45000", "45000", "", "", "", "");
insert into fee values("MCA", "43000", "42000", "42000", "49000", "", "", "", "");
insert into fee values("Bcom", "22000", "20000", "20000", "20000", "20000", "20000", "", "");
insert into fee values("Mcom", "36000", "30000", "30000", "30000", "", "", "", "");

-- College Fee Table
create table collegefee (
    rollno varchar(20),
    course varchar(20),
    branch varchar(20),
    semester varchar(20),
    total varchar(20)
);
```

💡 Admin Login:
username: admin
password: 12345

---

## 🧰 How to Run Locally

1️⃣ Clone the Repository

```bash
git clone https://github.com/rekibur-uddin/College-Automation-System.git
cd College-Automation-System
```

2️⃣ Open in NetBeans

* Open NetBeans IDE
* Go to File → Open Project
* Select the project folder

3️⃣ Import Database

* Open phpMyAdmin or MySQL Workbench
* Create schema `collegemanagementsystem`
* Import `database/collegemanagementsystem.sql`

4️⃣ Update DB Credentials

* In source code, set JDBC URL, username, password as per local MySQL

5️⃣ Run Project

* Click ▶️ Run Project in NetBeans

---

## ✍️ Author

👤 Rekibur Uddin
📧 [Visit My Portfolio](https://rekiburuddin.blogspot.com)

---

## ⭐ Support

If you like this project, consider giving it a ⭐ on [GitHub](https://github.com/rekibur-uddin/College-Automation-System) 🙌.
