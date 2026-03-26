🎓 Course Recovery System (CRS)

A Java desktop application for managing student academic recovery workflows — built for universities to identify at-risk students, generate structured recovery plans, and automate communications.


📌 Overview
The Course Recovery System (CRS) is a role-based desktop application developed to streamline the academic recovery process within a university environment. The system enables administrators to monitor student performance, assess eligibility for recovery programmes, assign personalised action plans, and notify students — all from a single unified interface.
Developed as a group project by a team of 4 at Asia Pacific University of Technology & Innovation (APU).

✨ Features
🔐 Authentication & Access Control

Secure login with hashed password storage (MD5 + SHA-256)
Role-based access control: Admin, Member, and Student roles
"Remember Me" functionality with persistent session support
Full login activity logging with timestamps for audit trails

📊 Student Eligibility Assessment

Automatically identifies at-risk students based on CGPA thresholds and failed course count
Displays comprehensive student academic profiles across multiple courses and semesters
Supports filtering and querying by student ID, major, and year

📋 Recovery Plan Management

Generates personalised recovery plans per student per failed course
Supports 3 recovery action types: Retake Exam, Resubmit Assignment, Repeat Course
Tracks plan status (Pending / Completed) with notes and history

📧 Email & Notification System

Sends recovery plan notifications directly to students via JavaMail API
Internal messaging system between users (Admin → Student)
Broadcast notification manager — target announcements by student year and major
Full email log with read/unread status tracking

📄 Report Generation

Exports student recovery reports as formatted PDF documents using iTextPDF
Structured layouts with course details, marks, recovery actions, and statuses

🗃️ Data Management

CSV-based data persistence across 7 data entities: students, courses, results, recovery plans, notifications, emails, and performance metrics
Supports full CRUD operations on all core data


🛠️ Tech Stack
LayerTechnologyLanguageJava (JDK 8+)UI FrameworkJava Swing (GUI)PDF GenerationiTextPDF 5.5.13.3EmailJavaMail API 1.6.2HTTP ClientOkHttp 3.14.9JSON ParsingGson 2.11.0Data StorageCSV flat filesIDEIntelliJ IDEA

🏗️ Project Structure
Course-Recovery-System-CRS/
├── src/
│   └── com/chocodivision/app/
│       ├── Main.java                        # Entry point
│       ├── BaseFrame.java                   # Shared UI base class
│       ├── LoginFrame.java                  # Authentication screen
│       ├── MainDashboardFrame.java          # Main navigation hub
│       ├── EligibilityFrame.java            # Student eligibility checker
│       ├── EmailFrame.java                  # Email & messaging module
│       ├── LoginLogFrame.java               # Audit log viewer
│       └── NotificationManagementFrame.java # Broadcast notifications
├── data/
│   ├── student_information.csv
│   ├── student_course_results.csv
│   ├── student_performance.csv
│   ├── course_assessment_information.csv
│   ├── recovery_plans.csv
│   ├── notifications.csv
│   ├── emails.csv
│   └── login_log.txt
├── lib/
│   ├── itextpdf-5.5.13.3.jar
│   ├── javax.mail-api-1.6.2.jar
│   ├── gson-2.11.0.jar
│   └── okhttp-3.14.9.jar
└── README.md

🚀 Getting Started
Prerequisites

Java JDK 8 or higher
IntelliJ IDEA (recommended) or any Java IDE

Installation

Clone the repository:

bashgit clone https://github.com/BYTHEWAY03/Course-Recovery-System-CRS.git

Open the project in IntelliJ IDEA
Add all .jar files from the /lib folder to the project classpath:

itextpdf-5.5.13.3.jar
javax.mail-api-1.6.2.jar
gson-2.11.0.jar
okhttp-3.14.9.jar


Run Main.java to launch the application

Default Login Credentials
RoleUsernamePasswordAdminadminadmin123Students001(see users.txt)

👥 Team
Built by a team of 4 Software Engineering students at Asia Pacific University (APU), Kuala Lumpur, Malaysia.

📃 License
This project was developed for academic purposes at Asia Pacific University of Technology & Innovation (APU).
