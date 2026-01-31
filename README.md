Hospital Appointment & Treatment Management System
A backend REST API built using Django and Django REST Framework to manage hospital appointments, treatments, and prescriptions with role-based access control and JWT authentication.

This project demonstrates real-world backend concepts such as custom user roles, secure APIs, filtering, profiling, and database design visualization.

Features
Custom User model with roles:
Doctor
Patient
Admin
Appointment scheduling system
Treatment management
Prescription creation linked to completed appointments
JWT Authentication (Login & Token-based access)
Role-based permissions:
Doctors can create prescriptions
Patients can view only their own appointments
Object-level access control
Filtering support (doctor, status, appointment date)
API performance profiling using Django Silk
Database schema visualization using Graphviz (models.dot)
Tech Stack
Backend Framework: Django
API Framework: Django REST Framework (DRF)
Authentication: JWT (SimpleJWT)
Database: SQLite (development)
Profiling: Django Silk
Schema Visualization: django-extensions + Graphviz
Version Control: Git & GitHub
Project Structure
hospital-appointment-system/ ├── config/ # Project settings and URLs ├── stores/ # Main application │ ├── models.py # Database models │ ├── serializers.py # DRF serializers │ ├── views.py # API views │ ├── permissions.py # Custom permissions │ ├── urls.py # App routes │ └── admin.py # Admin registrations ├── api.http # API testing file ├── models.dot # Database schema diagram source ├── manage.py ├── requirements.txt ├── README.md └── .gitignore

Authentication Flow (JWT)
User logs in using /api/token/
Receives:
access token
refresh token
Access token is sent in headers for protected APIs: Authorization: Bearer <access_token>
📡 API Endpoints Overview
Authentication
POST /api/token/ – Get JWT tokens
POST /api/token/refresh/ – Refresh access token
Appointments
GET /api/appointments/ – List appointments
POST /api/appointments/ – Create appointment
GET /api/appointments/<id>/ – View appointment details
Treatments
GET /api/treatments/ – List treatments
Prescriptions
POST /api/prescriptions/create/ – Create prescription (Doctor only)
GET /api/prescriptions/?appointment=<id> – List prescriptions
🧪 API Testing
APIs can be tested using:
Postman
VS Code / PyCharm HTTP client via api.http
JWT tokens are required for all protected routes
📊 API Profiling (Django Silk)
Django Silk is integrated to monitor:

Request/response time
SQL queries
Performance bottlenecks
Access Silk dashboard at:

http://127.0.0.1:8000/silk/

⚠️ Silk is enabled only for development purposes.

🗂️ Database Schema Diagram
The database structure is visualized using Graphviz.

Source file: models.dot
Generated via django-extensions
This diagram shows:

All models
Fields
Relationships (ForeignKey & ManyToMany)
Setup Instructions
1️⃣ Clone the repository
git clone https://github.com//hospital-appointment-system.git cd hospital-appointment-system 2️⃣ Create virtual environment python -m venv venv source venv/bin/activate 3️⃣ Install dependencies pip install -r requirements.txt 4️⃣ Run migrations python manage.py migrate 5️⃣ Create superuser python manage.py createsuperuser 6️⃣ Start server python manage.py runserver

Learning Outcomes Designing relational databases using Django ORM Implementing JWT authentication Enforcing role-based and object-level permissions Structuring scalable Django REST APIs Profiling APIs for performance Using Git & GitHub for version control Future Improvements Pagination for large datasets Email notifications for appointments Dockerization Frontend integration (React / Flutter) Deployment to cloud (AWS / Render) 👤 Author Lakhvinder singh Backend Developer | Django | REST APIs If you find this project useful, feel free to star the repository!
