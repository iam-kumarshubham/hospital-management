# Hospital Management System

A Django REST API-based hospital management system that handles doctors, patients, appointments, and billing information.

## Features

- Manage doctors and their specializations
- Track patient information
- Schedule appointments
- Handle billing records
- RESTful API endpoints
- User authentication

## Tech Stack

- Python 3.11
- Django 5.2.1
- Django REST Framework
- SQLite3

## Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd hospital-management
```

2. Create a virtual environment and activate it:
```bash
python -m venv env
source env/bin/activate  # On Windows: env\Scripts\activate
```

3. Install dependencies:
```bash
pip install django djangorestframework
```

4. Apply database migrations:
```bash
python manage.py makemigrations
python manage.py migrate
```

5. Create a superuser (admin):
```bash
python manage.py createsuperuser
```

6. Run the development server:
```bash
python manage.py runserver
```

## API Endpoints

- `GET/POST /api/doctors/` - List all doctors or create a new doctor
- `GET/PUT/DELETE /api/doctors/{id}/` - Retrieve, update or delete a doctor
- `GET/POST /api/patients/` - List all patients or create a new patient
- `GET/PUT/DELETE /api/patients/{id}/` - Retrieve, update or delete a patient
- `GET/POST /api/appointments/` - List all appointments or create a new appointment
- `GET/PUT/DELETE /api/appointments/{id}/` - Retrieve, update or delete an appointment
- `GET/POST /api/billings/` - List all billing records or create a new billing record
- `GET/PUT/DELETE /api/billings/{id}/` - Retrieve, update or delete a billing record

## Models

### Doctor
- User (One-to-One relationship with Django User)
- Specialization
- Contact

### Patient
- User (One-to-One relationship with Django User)
- Age
- Contact

### Appointment
- Doctor (Foreign Key)
- Patient (Foreign Key)
- Date
- Time
- Symptoms

### Billing
- Appointment (One-to-One relationship)
- Amount
- Paid Status

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.