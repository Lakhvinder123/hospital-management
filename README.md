# 🏥 Hospital Appointment & Treatment Management System

A backend REST API built using Django and Django REST Framework to manage hospital appointments, treatments, and prescriptions with role-based access control.

This project demonstrates real-world backend concepts such as custom user roles, secure APIs, filtering, permissions, and database design.

---

## 🚀 Features

- Custom User Model with Roles:
  - Doctor
  - Patient
  - Admin
- Appointment Scheduling System
- Treatment Management
- Prescription Creation Linked to Appointments
- Role-Based Permissions
  - Doctors can create treatments/prescriptions
  - Patients can view only their own appointments
- Object-Level Access Control
- Filtering Support (doctor, patient, appointment date)
- API Testing using `api.http`
- Modular Django App Structure

---

## 🛠 Tech Stack

- Backend Framework: Django  
- API Framework: Django REST Framework (DRF)  
- Database: SQLite (Development)  
- Version Control: Git & GitHub  

---

## 📂 Project Structure
Hospital Appointment & Treatment Management System/
│
├── backend/
│ ├── settings.py
│ ├── urls.py
│ ├── asgi.py
│ └── wsgi.py
│
├── stores/
│ ├── models.py
│ ├── serializers.py
│ ├── views.py
│ ├── permissions.py
│ ├── urls.py
│ ├── admin.py
│ └── migrations/
│
├── api.http
├── manage.py
├── screenshots/
├── README.md
└── .gitignore

---

## 🔐 Authentication Flow

1. User logs in via API
2. Receives authentication credentials
3. Authenticated users can access protected endpoints based on their role

Doctors, Patients, and Admins each have different access permissions.

---

## 📡 API Endpoints Overview

### Appointments

- `GET /appointments/` – List appointments  
- `POST /appointments/` – Create appointment  
- `GET /appointments/<id>/` – Appointment details  

### Treatments

- `GET /treatments/` – List treatments  

### Prescriptions

- `POST /prescriptions/create/` – Create prescription (Doctor only)  
- `GET /prescriptions/?appointment=<id>` – List prescriptions  

---

## 🧪 API Testing

APIs can be tested using:

- VS Code / PyCharm HTTP Client (`api.http`)
- Postman

Protected routes require authentication.

---

## 📸 Project Screenshots

Screenshots demonstrating admin panel, APIs, appointments, and treatment workflows are available inside:

screenshots/

---

## ⚙️ Setup Instructions

### 1️⃣ Clone Repository

```bash
git clone https://github.com/your-username/hospital-appointment-system.git
cd hospital-appointment-system

2️⃣ Create Virtual Environment
python -m venv venv
venv\Scripts\activate

3️⃣ Install Dependencies
pip install django djangorestframework

4️⃣ Run Migrations
python manage.py makemigrations
python manage.py migrate

5️⃣ Create Superuser
python manage.py createsuperuser

6️⃣ Run Server
python manage.py runserver

Open in browser:
http://127.0.0.1:8000/

📌 Important
Do not upload the following to GitHub:
venv/
__pycache__/
.env
db.sqlite3
*.pyc

📚 Learning Outcomes

Designing relational databases using Django ORM

Building REST APIs with Django REST Framework

Implementing role-based permissions

Structuring scalable backend projects

Using Git & GitHub for version control

🚀 Future Improvements

JWT Authentication

Pagination for large datasets

Email notifications

Frontend integration (React)

Dockerization

Cloud deployment

👤 Author

Lakhvinder singh
Django | REST APIs

If you find this project useful, feel free to ⭐ the repository!






