# 🎟️ EventSphere – Smart Event Management System

EventSphere is a **Smart Event Management System** built with **Python and Django**. It provides a complete digital workflow for event organizers and attendees, including event management, ticket booking, QR-code ticketing, attendance verification, automated certificates, weather information, notifications, and role-based access.

The project is designed to make event management **paperless, faster, secure, and easier to manage**.

---

## 📌 Project Overview

Traditional event management often involves:

- Manual paper registration
- Long queues during event check-in
- Difficult ticket verification
- Manual attendance management
- Delayed certificate distribution
- Limited event information for attendees

EventSphere solves these problems through a centralized web application.

### Main Solution

- 📱 Digital event registration
- 🎫 Instant QR-code ticket generation
- 📷 QR-based event check-in
- 🌦️ Real-time weather information
- 📄 Automated PDF certificates
- 🔐 Role-based authentication
- 📧 Email notifications
- 📊 Event and attendance management

---

# ✨ Key Features

## 👥 1. Role-Based Access

EventSphere supports different user roles.

### 👨‍💼 Admin

Admin can:

- Manage users
- Manage organizers
- Approve/reject events
- Monitor events
- Manage categories
- View system information
- Verify certificates
- Monitor reports

### 🎤 Organizer

Organizers can:

- Register and login
- Manage profile
- Create events
- Edit events
- Delete events
- Upload event banners
- Upload gallery images
- Set event capacity
- Create ticket types
- Set ticket prices
- View registrations
- Scan QR tickets
- Mark attendance
- View revenue
- View analytics
- Download attendee lists
- Send announcements
- Generate certificates

### 👤 Attendee / User

Users can:

- Register and login
- Manage profile
- Browse events
- Search events
- Filter events
- View event details
- Check weather
- Book tickets
- Download tickets
- View QR tickets
- Cancel bookings
- Save favorite events
- View booking history
- Download certificates
- Review events
- Receive notifications

---

# 🎫 2. Event Management

Every event can contain:

- Event title
- Description
- Category
- Organizer
- Venue
- Address
- City
- Google Maps link
- Event date
- Event time
- Registration deadline
- Capacity
- Available seats
- Ticket types
- Ticket price
- Banner image
- Gallery images
- Event status
- Approval status

Organizers can manage their events through the organizer dashboard.

---

# 🔎 3. Search, Filter & Sort

Users can search events by:

- Event name
- Organizer
- Category
- Location

### Filters

- Date
- City
- Category
- Price
- Free/Paid
- Upcoming
- Completed

### Sorting

- Latest
- Popular
- Highest Rated
- Price
- Date

---

# 🎟️ 4. Ticket Booking System

Users can book tickets for available events.

The booking workflow includes:

```text
Browse Event
     ↓
Select Ticket
     ↓
Select Quantity
     ↓
Confirm Booking
     ↓
Generate Ticket
     ↓
Generate QR Code
     ↓
Download Ticket
```

The system supports:

- Ticket quantity
- Booking confirmation
- Booking history
- Booking status
- QR ticket
- PDF ticket
- Ticket cancellation
- Refund status

---

# 📱 5. QR Code Ticket System

Every successful booking generates a unique QR code.

The QR code can contain:

- Booking ID
- User ID
- Event ID
- Ticket Type
- Verification Token
- Timestamp

### Organizer QR Workflow

```text
User Books Ticket
       ↓
Unique QR Generated
       ↓
Organizer Scans QR
       ↓
Ticket Verification
       ↓
Duplicate Entry Check
       ↓
Attendance Marked
```

The organizer can:

- Scan QR codes
- Verify tickets
- Prevent duplicate entry
- Mark attendance
- View scan history

Tickets can be downloaded as PDF files.

---

# 📋 6. Attendance Management

Attendance can be recorded through:

- QR Code scanning
- Manual entry

### Attendance Status

```text
Present
Absent
```

The system records:

- Check-in time
- Attendance status
- Attendance reports
- Attendance analytics

Certificates are generated after attendance is confirmed.

---

# 🏆 7. Automated Certificate System

After event completion and attendance confirmation, the system can generate a PDF certificate automatically.

### Certificate Contains

- Participant name
- Event name
- Organizer name
- Event date
- Certificate ID
- QR verification
- Organization logo
- Digital signature
- Issue date

### Certificate Features

- Download certificate PDF
- Certificate verification
- Admin verification
- Organizer download
- User dashboard download

---

# 🌦️ 8. Real-Time Weather

EventSphere can display weather information on event pages.

The weather functionality uses:

- Python Requests
- OpenWeatherMap API

Users can check weather conditions before attending an event.

---

# 🔔 9. Notification System

The system supports:

- In-app notifications
- Email notifications

### User Notifications

Examples:

- Registration successful
- Welcome email
- Email verification
- Booking successful
- Ticket generated
- Payment successful
- Event approved
- Event cancelled
- Event rescheduled
- Venue changed
- 7-day reminder
- 1-day reminder
- 1-hour reminder
- Event started
- Event completed
- Certificate ready
- Organizer announcement

### Organizer Notifications

- Event approved
- Event rejected
- New registration
- Event full
- Reviews received
- Revenue update
- Certificate generated

### Admin Notifications

- New organizer registration
- New event pending
- Reports submitted
- Payment issues
- System alerts

### Notification Center

Users can:

- View notifications
- Check unread count
- Mark notifications as read
- Delete notifications
- View notification history

---

# ⭐ 10. Reviews & Ratings

Users can:

- Rate an event from 1–5
- Write reviews
- Edit reviews
- Delete reviews

Organizers can:

- Reply to reviews

The system displays:

- Average rating
- Total reviews

---

# ❤️ 11. Favorites

Users can save events for later.

Features:

- Add event to favorites
- Remove event from favorites
- View favorite events

---

# 📊 12. Dashboards

## Admin Dashboard

The admin dashboard can display:

- Total users
- Total organizers
- Total events
- Revenue
- Tickets sold
- Certificates
- Attendance rate
- Reviews

### Admin Charts

- Monthly revenue
- Event categories
- Ticket sales
- Attendance
- User growth

---

## Organizer Dashboard

Organizer dashboard can display:

- Total events
- Revenue
- Registrations
- Tickets sold
- Attendance
- Certificates
- Reviews

### Organizer Charts

- Event performance
- Revenue
- Attendance
- Registrations

---

## User Dashboard

User dashboard can display:

- Upcoming events
- Bookings
- Certificates
- Favorites
- Notifications

---

# 📄 13. Reports

The system can generate reports such as:

- Attendance Report
- Revenue Report
- Booking Report
- User Report
- Event Report

Reports can be exported as:

- CSV
- PDF

---

# 💳 14. Payment Module

The project can be designed to support payment integration.

Possible payment providers:

- Razorpay
- Stripe
- PayPal

For academic/demo usage, mock payments can be used while maintaining a realistic booking workflow.

---

# 🔐 15. Authentication & Security

The authentication module supports:

- User registration
- Login
- JWT authentication
- Role-based authorization
- Password encryption
- Secure login
- Forgot password
- Password reset
- Email verification
- Protected routes

Different dashboards and permissions are provided according to the user's role.

---

# 🏗️ System Architecture

EventSphere follows a **Django MVT architecture** with REST API services.

```text
                    ┌─────────────────────┐
                    │      Frontend       │
                    │ HTML/CSS/JS/Bootstrap│
                    └──────────┬──────────┘
                               │
                               ↓
                    ┌─────────────────────┐
                    │   Django Backend    │
                    │   Views / APIs      │
                    └──────────┬──────────┘
                               │
              ┌────────────────┼────────────────┐
              ↓                ↓                ↓
       ┌────────────┐   ┌────────────┐   ┌────────────┐
       │  Accounts  │   │   Events   │   │  Bookings  │
       └────────────┘   └────────────┘   └────────────┘
              │                │                │
              └────────────────┼────────────────┘
                               ↓
                    ┌─────────────────────┐
                    │   Django ORM / DB   │
                    │      SQLite3        │
                    └─────────────────────┘
                               │
          ┌────────────────────┼────────────────────┐
          ↓                    ↓                    ↓
     QR Generator         PDF Generator        Weather API
      qrcode              ReportLab          OpenWeatherMap
```

---

# 🧩 Django Application Modules

The project is organized into separate Django applications.

| App | Responsibility |
|---|---|
| `accounts` | Authentication, profiles, roles and user decorators |
| `events` | Event listings, banners, search, filters and event management |
| `bookings` | Reservations, QR generation and booking workflow |
| `certificates` | PDF certificate generation and verification |
| `api` | REST API endpoints, serializers and custom permissions |

This modular structure makes the application easier to maintain and extend.

---

# 🛠️ Technology Stack

## Backend

- Python 3.10+
- Django
- Django ORM
- Django REST Framework

## Frontend

- HTML5
- CSS3
- JavaScript
- Bootstrap 5

## Database

- SQLite3
- Django ORM

## PDF Generation

- ReportLab

## QR Code

- Python `qrcode` library

## Weather

- Requests
- OpenWeatherMap API

## Authentication

- JWT
- Role-Based Authorization

---

# 📂 Project Structure

```text
EventSphere/
│
├── manage.py
│
├── project/
│   ├── settings.py
│   ├── urls.py
│   ├── wsgi.py
│   └── asgi.py
│
├── accounts/
│   ├── models.py
│   ├── views.py
│   ├── urls.py
│   ├── forms.py
│   └── templates/
│
├── events/
│   ├── models.py
│   ├── views.py
│   ├── urls.py
│   ├── forms.py
│   └── templates/
│
├── bookings/
│   ├── models.py
│   ├── views.py
│   ├── urls.py
│   └── templates/
│
├── certificates/
│   ├── models.py
│   ├── views.py
│   ├── utils.py
│   └── templates/
│
├── api/
│   ├── serializers.py
│   ├── views.py
│   ├── urls.py
│   └── permissions.py
│
├── static/
├── media/
├── templates/
├── db.sqlite3
├── requirements.txt
└── README.md
```

> The exact folder names may vary depending on the project version.

---

# ⚙️ Installation & Setup

## 1. Clone the Repository

```bash
git clone https://github.com/your-username/eventsphere.git
cd eventsphere
```

---

## 2. Create a Virtual Environment

### macOS / Linux

```bash
python3 -m venv venv
source venv/bin/activate
```

### Windows

```bash
python -m venv venv
venv\Scripts\activate
```

---

## 3. Install Dependencies

Create or use the project's `requirements.txt` file.

Example:

```text
Django
djangorestframework
djangorestframework-simplejwt
Pillow
qrcode
reportlab
requests
django-cors-headers
```

Install dependencies:

```bash
pip install -r requirements.txt
```

---

# 🗄️ Database Setup

Run Django migrations:

```bash
python manage.py makemigrations
python manage.py migrate
```

Create an administrator account:

```bash
python manage.py createsuperuser
```

Follow the terminal instructions to enter:

```text
Username
Email
Password
```

---

# ▶️ Run the Project

Start the Django development server:

```bash
python manage.py runserver
```

Open the application in your browser at:

```text
http://127.0.0.1:8000/
```

---

# 🔑 Admin Panel

Django provides an administration interface.

Run:

```bash
python manage.py runserver
```

Then open:

```text
http://127.0.0.1:8000/admin/
```

Login using the superuser credentials created earlier.

---

# 🔄 Complete System Workflow

```text
                    START
                      │
                      ↓
             ┌────────────────┐
             │ User Registers │
             └───────┬────────┘
                     ↓
             ┌────────────────┐
             │ Email / Login  │
             └───────┬────────┘
                     ↓
              ┌──────┴──────┐
              │             │
              ↓             ↓
          ATTENDEE       ORGANIZER
              │             │
              ↓             ↓
       Browse Events    Create Event
              │             │
              ↓             ↓
       Search / Filter   Event Approval
              │             │
              ↓             ↓
        Book Ticket      Manage Event
              │
              ↓
       QR Ticket Generated
              │
              ↓
       Attend Event
              │
              ↓
         QR Check-in
              │
              ↓
       Attendance Saved
              │
              ↓
      Certificate Generated
              │
              ↓
       Download Certificate
```

---

# 📈 Project Impact

EventSphere aims to provide:

- ✅ 100% paperless event workflow
- ✅ Reduced check-in queue time
- ✅ Instant ticket verification
- ✅ Automated attendance management
- ✅ Automated certificate generation
- ✅ Centralized event management
- ✅ Better organizer analytics
- ✅ Improved attendee experience

---

# 🚀 Future Scope

The system can be enhanced with:

### 💳 Production Payment Gateway

Integrate:

- Razorpay
- Stripe
- PayPal

### 📱 Mobile Application

Develop native/mobile applications using:

- Flutter
- React Native

### 🤖 AI Recommendation Engine

Add personalized event recommendations based on:

- User interests
- Previous bookings
- Categories
- Location
- Ratings

### ☁️ Cloud Deployment

Deploy the system using:

- AWS
- Azure
- Google Cloud
- Render
- Railway

### 🔔 Advanced Notifications

Add:

- Push notifications
- SMS notifications
- WhatsApp notifications

---

# 🧪 Testing

Before deployment, test:

### Authentication

- Registration
- Login
- Logout
- Password reset
- Email verification
- Role permissions

### Events

- Create event
- Edit event
- Delete event
- Approve/reject event
- Search/filter event

### Booking

- Ticket booking
- Ticket cancellation
- QR generation
- Duplicate QR prevention

### Attendance

- QR scanning
- Manual attendance
- Attendance reports

### Certificates

- Certificate generation
- Certificate verification
- PDF download

---

# ⚠️ Security Notes

For production deployment:

- Use environment variables for secrets.
- Never commit API keys or passwords.
- Use HTTPS.
- Configure secure Django settings.
- Use strong password hashing.
- Validate uploaded files.
- Restrict file types and sizes.
- Implement proper role-based permissions.
- Secure JWT tokens.
- Use a production database.
- Configure CORS carefully.
- Enable CSRF protection.
- Keep dependencies updated.

---

# 🎓 Academic Learning Outcomes

This project demonstrates practical knowledge of:

- Python
- Django
- Django MVT architecture
- REST APIs
- Authentication
- JWT
- Role-based authorization
- Django ORM
- Database management
- HTML
- CSS
- JavaScript
- Bootstrap
- QR code generation
- PDF generation
- API integration
- Email services
- Event management
- File uploads
- Data validation

---

# 👨‍💻 Project Team

| Name | Enrollment | Branch |
|---|---|---|
| **Patel Harshkumar** | 24002171710023 | CSE_AI |
| **Chauthari Tirth** | 25002170220003 | IT |
| **Gediya Poojan** | 24002170210025 | IT |

---

# 📜 License

This project is developed for **educational and academic purposes**.

You may modify and extend the project for learning, college submissions, and portfolio purposes.

---

# ⭐ Project Highlights

```text
✅ Smart Event Management
✅ Role-Based Authentication
✅ Admin Dashboard
✅ Organizer Dashboard
✅ User Dashboard
✅ Event CRUD
✅ Search & Filters
✅ Ticket Booking
✅ QR Code Tickets
✅ QR Attendance
✅ PDF Tickets
✅ Automated Certificates
✅ Certificate Verification
✅ Weather API
✅ Email Notifications
✅ Reviews & Ratings
✅ Favorites
✅ Reports
✅ Analytics
✅ REST APIs
✅ Django ORM
```

---

## 🎟️ EventSphere

> **Plan. Book. Attend. Verify. Celebrate.**
