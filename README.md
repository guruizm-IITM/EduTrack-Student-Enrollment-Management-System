# EduTrack - Student Enrollment Management System 📚

EduTrack is a lightweight **Flask + SQLAlchemy web application** for managing student records, course enrollments, and academic details.  
It provides a simple and intuitive interface for adding, updating, deleting, and viewing student information along with their enrolled courses.

---

## 🚀 Features
- Add new students with unique roll numbers  
- Enroll students in multiple courses  
- Update student details and course enrollments  
- Delete student records (along with linked enrollments)  
- View student details and their enrolled courses  
- SQLite3 database backend (lightweight and portable)

---

## 🧱 Tech Stack
| Component | Technology |
|------------|-------------|
| **Backend** | Flask (Python) |
| **Database** | SQLite3 (SQLAlchemy ORM) |
| **Frontend** | HTML + Jinja2 Templates |
| **Framework** | Flask Web Framework |

---

## ⚙️ Installation & Setup

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/your-username/edutrack.git
cd edutrack
```

### 2️⃣ Create Virtual Environment
```bash
python -m venv venv
source venv/bin/activate   # On macOS/Linux
venv\Scripts\activate    # On Windows
```

### 3️⃣ Install Dependencies
```bash
pip install flask flask_sqlalchemy
```

### 4️⃣ Run the Application
```bash
python app.py
```
Visit the app in your browser: **http://127.0.0.1:5000/**

---

## 🗃️ Database Schema

### **Student**
| Column | Type | Description |
|--------|------|-------------|
| student_id | Integer | Primary key |
| roll_number | String | Unique student roll number |
| first_name | String | First name |
| last_name | String | Last name |

### **Course**
| Column | Type | Description |
|--------|------|-------------|
| course_id | Integer | Primary key |
| course_code | String | Unique course code |
| course_name | String | Name of the course |
| course_description | String | Optional description |

### **Enrollments**
| Column | Type | Description |
|--------|------|-------------|
| enrollment_id | Integer | Primary key |
| estudent_id | Integer | Foreign key → Student |
| ecourse_id | Integer | Foreign key → Course |

---

## 🧩 Folder Structure

```
edutrack/
│
├── app.py                  # Main Flask application
├── database.sqlite3        # SQLite database file
├── templates/              # HTML templates
│   ├── home.html
│   ├── add_student.html
│   ├── update.html
│   ├── view.html
│   └── exists.html
└── README.md
```

---

## 💡 Future Improvements
- Add search and filter functionality for students  
- Implement authentication for admin access  
- Add pagination and AJAX-based updates  
- Integrate REST API endpoints for student and course data

---

## 🧑‍💻 Author
**Abhishek Guru**  
BS in Data Science and Applications - IIT Madras

---

## 📜 License
This project is licensed under the MIT License — feel free to use and modify it!
