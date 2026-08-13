# 💼 NexusHire – Job Portal Website

NexusHire is a modern **front-end Job Portal Website** designed to connect **job seekers and employers/recruiters** through a simple, responsive, single-page web application.

The project is built using **HTML5, CSS3, Bootstrap, and JavaScript** with **browser localStorage** for client-side data persistence. It does not require a server, backend, or database. fileciteturn5file0L48-L62

---

## 📌 Project Overview

Finding suitable jobs can be difficult for students and freshers, while employers need an easy way to publish job opportunities and attract suitable candidates.

**NexusHire** provides a centralized front-end platform where:

- Job seekers can discover jobs.
- Users can search and filter job listings.
- Users can view complete job details.
- Registered users can apply with one click.
- Users can track their applications.
- Users can create and update their profile.
- Employers/recruiters can post job openings.
- Job information is stored and managed on the client side.

The project focuses on **pure front-end engineering** using a Single-Page Application (SPA) approach. fileciteturn5file0L48-L62

---

# ✨ Features

## 🔍 1. Advanced Job Search & Filtering

NexusHire provides a multi-filter job search engine.

### Available Filters

- Category
- Job type
- Work mode
- Experience level
- Schedule
- Salary range

### Job Categories

- Frontend
- Backend
- Government
- Healthcare
- Finance
- Management
- Agriculture
- Education

### Job Types

- Fixed
- Hourly
- Contract

### Work Modes

- Remote
- Hybrid
- Onsite

### Experience Levels

- Junior
- Mid
- Senior

### Schedule

- Full-Time
- Part-Time

### Salary

The salary range can be filtered from approximately:

```text
₹15,000 → ₹1,20,000 per month
```

The project supports sorting by relevance, salary, and newest jobs. fileciteturn5file2L342-L362

---

# 👤 2. Job Seeker Module

Job seekers can:

- Register an account
- Login
- Create a profile
- Upload a profile photo
- Search jobs
- Filter jobs
- Sort jobs
- View job details
- Apply for jobs
- Track applications
- View application status
- Logout

The platform is designed particularly for students, freshers, and other job seekers. fileciteturn5file0L94-L109

---

# 🏢 3. Employer / Recruiter Module

Employers/recruiters can work with job listings containing:

- Job title
- Description
- Salary
- Required skills
- Experience level
- Work mode
- Job schedule
- Job type

The project also supports collecting and viewing applications associated with job listings. fileciteturn5file0L103-L109

---

# 🔐 4. Authentication System

NexusHire contains Login and Signup flows using modal interfaces.

### Login Validation

The system checks:

- Email format
- Password requirements
- Stored credentials

Invalid credentials produce an inline error without a page reload.

### Signup Validation

The system validates:

- Name
- Email
- Email uniqueness
- Password
- Confirm password

The password must contain:

- Uppercase letter
- Lowercase letter
- Number
- Special character
- Minimum 8 characters

The password strength indicator displays:

```text
Weak → Medium → Strong
```

User information is stored in browser `localStorage`. fileciteturn5file0L116-L133

> **Security note:** Because this is a front-end-only academic project, credentials stored in browser localStorage should not be considered production-grade authentication.

---

# 📝 5. One-Click Job Application

Logged-in users can apply directly from a job listing.

Application workflow:

```text
Login
  ↓
Browse Jobs
  ↓
Open Job Details
  ↓
Click Apply
  ↓
Application Saved
  ↓
Status Updated
  ↓
View in My Applications
```

Once an application is submitted, the UI changes to indicate that the job has already been applied for. Application data is stored in localStorage. fileciteturn5file0L69-L87

---

# 📋 6. My Applications Tracker

Users can view jobs they have applied for.

Application information includes:

- Company name
- Job role
- Salary
- Application status

The application tracker provides a centralized view of submitted applications. fileciteturn5file0L80-L87

---

# 📊 7. Personal Dashboard

The user dashboard provides:

- Personalized welcome message
- Profile completion percentage
- Application count
- Quick links
- Profile information
- Application activity

The dashboard includes an animated profile completion bar. fileciteturn5file3L411-L426

---

# 👤 8. Dynamic Profile

Users can manage their profile information.

### Profile Features

- Name
- Email
- Profile photo
- Dynamic avatar
- Initials fallback
- Profile completion

Users can upload an image using:

```javascript
<input type="file">
```

The browser `FileReader` API is used to preview the image as Base64 data. fileciteturn5file3L417-L426

---

# 💾 9. localStorage Data Persistence

Since NexusHire has no backend or database, browser localStorage is used for data persistence.

The project stores information such as:

```text
User
 ├── name
 ├── email
 ├── password
 └── photo

Applications
 └── APPLIED_JOBS
```

The session can be detected when the application loads, and logout clears the active session without removing the stored user data. fileciteturn5file3L422-L426

---

# 🧠 10. Dynamic Job Rendering

Jobs are represented as JavaScript objects inside the application's job list.

Filtering works by:

```text
User changes filter
       ↓
filterJobs()
       ↓
renderJobGrid()
       ↓
Array.filter()
       ↓
Matching jobs displayed
```

The results count and active filter tags are updated dynamically without reloading the page. fileciteturn5file2L356-L362

---

# 🎨 UI/UX Design

NexusHire uses a modern professional job-portal interface.

## Color System

| Color | Usage |
|---|---|
| Navy `#0F172A` | Main backgrounds |
| Electric Blue `#2563EB` | Actions and links |
| Green | Success states |
| Amber | Warnings and salary |
| Slate | Secondary text |

## Typography

The project uses:

- **Sora** for headings
- **DM Sans** for body text

## UI Features

- Responsive job cards
- Hover effects
- Card shadows
- Toast notifications
- Modal dialogs
- Backdrop blur
- Responsive navigation
- Animated transitions

The design uses CSS Grid/Flexbox and adapts to smaller screens. fileciteturn5file3L433-L451

---

# 📱 Responsive Design

The website is designed to work across:

- Desktop
- Laptop
- Tablet
- Mobile

The CSS Grid layout collapses to a single-column layout on smaller screens, with non-essential navigation text hidden on mobile. fileciteturn5file3L445-L451

---

# 🏗️ Application Architecture

NexusHire follows a client-side SPA architecture.

```text
                 ┌──────────────────────┐
                 │      NexusHire       │
                 │     Frontend SPA     │
                 └──────────┬───────────┘
                            │
            ┌───────────────┼───────────────┐
            ↓               ↓               ↓
        HTML5             CSS3          JavaScript
            │               │               │
            │               │               ├── Authentication
            │               │               ├── Job Search
            │               │               ├── Filtering
            │               │               ├── Applications
            │               │               ├── Dashboard
            │               │               └── Profile
            │               │
            └───────────────┼───────────────┘
                            ↓
                     Browser localStorage
```

There is currently:

```text
❌ No backend
❌ No server
❌ No database
```

This is explicitly a front-end-only implementation. fileciteturn5file0L54-L60

---

# 🛠️ Technology Stack

| Technology | Purpose |
|---|---|
| HTML5 | Website structure |
| CSS3 | Styling, layout and animations |
| Bootstrap | Responsive UI components |
| JavaScript | Application logic and interactivity |
| Font Awesome | Icons |
| Google Fonts | Typography |
| Browser localStorage | Client-side data persistence |

The project presentation identifies HTML5, CSS3, JavaScript, Font Awesome, Google Fonts, and Bootstrap as the main technologies. fileciteturn5file5L721-L748

---

# 📂 Project Structure

For the uploaded project, the main website is provided as:

```text
NexusHire/
│
├── nexushire_updated_fixed.html
└── README.md
```

The HTML file contains the page structure, styling, JavaScript logic, job data, authentication logic, filtering, dashboard, profile management, and application functionality.

If you later separate the project into individual files, a recommended structure is:

```text
NexusHire/
│
├── index.html
├── css/
│   └── style.css
├── js/
│   └── script.js
├── assets/
│   ├── images/
│   └── icons/
└── README.md
```

---

# ▶️ How to Run

NexusHire is a front-end project, so no Python, Node.js, database, or backend server is required.

## Method 1 — Open Directly

Simply double-click:

```text
nexushire_updated_fixed.html
```

It will open in your browser.

---

## Method 2 — VS Code

1. Open the project folder in VS Code.
2. Open `nexushire_updated_fixed.html`.
3. Install the **Live Server** extension.
4. Right-click the HTML file.
5. Select **Open with Live Server**.

The website will open in your browser.

---

# 🔄 User Workflow

```text
                    START
                      │
                      ↓
              ┌───────────────┐
              │ Open NexusHire│
              └───────┬───────┘
                      ↓
             ┌─────────────────┐
             │ Login / Register│
             └────────┬────────┘
                      ↓
               ┌──────┴───────┐
               │              │
               ↓              ↓
          Job Seeker       Recruiter
               │              │
               ↓              ↓
          Browse Jobs      Post Jobs
               │              │
               ↓              ↓
        Search / Filter    Job Details
               │              │
               ↓              ↓
          Job Details      Applications
               │
               ↓
           Apply
               │
               ↓
       My Applications
               │
               ↓
          Track Status
```

---

# 🔎 Job Filtering Workflow

```text
Select Category
       +
Select Job Type
       +
Select Work Mode
       +
Select Experience
       +
Select Schedule
       +
Set Salary
       ↓
Apply Filters
       ↓
JavaScript Array.filter()
       ↓
Render Matching Jobs
```

Available sorting includes:

- Most Relevant
- Salary High to Low
- Salary Low to High
- Newest First

The uploaded implementation contains these filtering and sorting controls. fileciteturn5file6L773-L802

---

# 📋 Application Workflow

The application logic prevents a logged-in user from repeatedly applying to the same job.

Conceptually:

```text
User clicks Apply
       ↓
Check Login
       ↓
Check Existing Application
       ↓
Save Application
       ↓
Save to localStorage
       ↓
Show Success Toast
       ↓
Update UI
```

The implementation stores the application with a job ID and timestamp and persists it as `nexus_applications` in localStorage. fileciteturn5file9L908-L916

---

# 🧪 Testing Checklist

## Authentication

- [ ] Register with valid information
- [ ] Test invalid email
- [ ] Test duplicate email
- [ ] Test weak password
- [ ] Test password confirmation
- [ ] Login with valid credentials
- [ ] Login with invalid credentials
- [ ] Logout

## Job Search

- [ ] Search jobs
- [ ] Filter by category
- [ ] Filter by salary
- [ ] Filter by work mode
- [ ] Filter by experience
- [ ] Filter by schedule
- [ ] Sort jobs
- [ ] Clear filters

## Applications

- [ ] Apply while logged out
- [ ] Apply while logged in
- [ ] Apply to same job twice
- [ ] Check application status
- [ ] Check My Applications

## Profile

- [ ] Edit profile
- [ ] Upload profile image
- [ ] Check image preview
- [ ] Check initials fallback
- [ ] Check profile completion

## Responsive UI

- [ ] Desktop
- [ ] Tablet
- [ ] Mobile

---

# ⚠️ Limitations

Because NexusHire is currently a front-end-only project:

- No real server-side authentication
- No centralized database
- No real employer account management
- No real-time job synchronization
- No production payment system
- No email service
- No resume/CV processing
- localStorage data is browser-specific
- Passwords should not be stored this way in production

Therefore, this version should be considered an **academic/demo front-end project**, not a production recruitment platform.

---

# 🚀 Future Scope

The project can be upgraded with a real backend.

### Backend

Possible technologies:

```text
Node.js
Express.js
MongoDB
```

### Future Features

- Real user authentication
- Secure password hashing
- Employer dashboard
- Admin dashboard
- Real job posting
- Resume/CV upload
- Resume parsing
- Email notifications
- Application notifications
- Employer analytics
- Interview scheduling
- Job recommendation system
- AI-powered resume matching
- Cloud database
- Production deployment

The project presentation specifically identifies **Node.js + MongoDB**, resume/CV parsing, email notifications, and an employer analytics dashboard as future scope. fileciteturn5file3L458-L473

---

# 📚 Key Learning Outcomes

This project demonstrates practical knowledge of:

- HTML5 semantic structure
- CSS3
- Flexbox
- CSS Grid
- Responsive design
- Bootstrap
- JavaScript DOM manipulation
- Event-driven JavaScript
- Array methods
- Dynamic rendering
- Form validation
- Regular expressions
- localStorage
- Session management
- FileReader API
- Base64 image preview
- SPA-style navigation
- UI/UX design
- Client-side filtering

The project presentation highlights event-driven JavaScript, reusable render functions, FileReader API, and CSS custom properties as key learning outcomes. fileciteturn5file3L464-L468

---

# 🎯 Project Objectives

The main objectives of NexusHire are:

1. Create a simple job discovery platform.
2. Help students and freshers find relevant opportunities.
3. Provide powerful job filtering.
4. Provide a simple one-click application process.
5. Allow users to maintain their profiles.
6. Provide application tracking.
7. Demonstrate modern front-end development.
8. Build a responsive and user-friendly SPA.
9. Demonstrate client-side data persistence.
10. Provide a foundation for future full-stack development.

---

# 👨‍💻 Project Team

| Name | Enrollment Number | Role |
|---|---|---|
| **Patel Harshkumar Kanaiyalal** | 24002171710023 | Team Lead |
| **Shah Ansh Shashinbhai** | 25002170420012 | UI Designer |
| **Gediya Poojan Hareshbhai** | 24002170210025 | JavaScript |

The team details are listed in the project presentation. fileciteturn5file0L24-L41

---

# 🎓 Academic Project

**Project Name:** NexusHire – Job Portal Website

**Project Type:** Full Stack Development / Front-End Academic Project

**Current Implementation:** Front-End SPA

**Target Users:**

- Students
- Freshers
- Job Seekers
- Employers
- Recruiters

The current version intentionally focuses on front-end engineering without a server, backend, or database. fileciteturn5file0L48-L62

---

# ⭐ Project Highlights

```text
✅ Job Portal Website
✅ Single Page Application
✅ Job Search
✅ Advanced Multi-Filter
✅ Salary Range Filter
✅ Remote / Hybrid / Onsite
✅ Junior / Mid / Senior
✅ Full-Time / Part-Time
✅ Fixed / Hourly / Contract
✅ One-Click Applications
✅ My Applications
✅ User Dashboard
✅ Profile Management
✅ Profile Photo Upload
✅ Password Strength Checker
✅ Login & Signup
✅ Form Validation
✅ localStorage Persistence
✅ Responsive Design
✅ Bootstrap
✅ Font Awesome
✅ Google Fonts
✅ Toast Notifications
✅ Dynamic Job Rendering
```

---

# 📜 License

This project is developed for **educational and academic purposes**.

It may be modified and extended for learning, college submissions, demonstrations, and portfolio purposes.

---

## 💼 NexusHire

> **Discover. Apply. Connect. Get Hired.**
