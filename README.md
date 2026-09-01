<div align="center">

# 🏥 Radium Diagnostic & Consultation Center
### Hospital Management System (HMS)

A role-based, web platform that replaces phone-and-paper hospital operations with a single online system for patients, doctors, receptionists, lab technicians, and administrators.

*American International University-Bangladesh (AIUB) · Department of Computer Science · Software Engineering, Summer 25-26*

![Status](https://img.shields.io/badge/status-prototype-blue)
![Roles](https://img.shields.io/badge/roles-5-informational)
![Process%20Model](https://img.shields.io/badge/process%20model-Evolutionary%20Prototyping-orange)
![Made with](https://img.shields.io/badge/design-Figma-ff69b4)

</div>

---

## 📖 Overview

**Radium Diagnostic & Consultation Center**, located in Daudkandi, Cumilla, currently runs its appointment booking, patient records, diagnostic reporting, and billing manually over the phone and on paper. As patient volume grows, this creates busy phone lines, double-bookings, misplaced reports, and no consolidated view of hospital operations.

This project designs and prototypes a **web-based Hospital Management System** that brings patient registration, appointment scheduling, doctor and department management, electronic medical records, diagnostic report handling, billing, and administrative reporting into one coherent, role-based platform.

## ✨ Core Features

| Module | What it does |
|---|---|
| 🧑‍⚕️ **Patient Management** | Registration, secure login, profile management, medical & appointment history |
| 📅 **Appointment & Diagnostic Management** | Real-time doctor availability, online booking/rescheduling/cancellation, diagnostic report upload & access |
| 🏢 **Hospital Administration** | Doctor & department management, user accounts, billing & payments, centralized reporting |

## 👥 Roles & Access

The system is built around **five actors**, each with a dedicated portal and permission set:

- **Patient** — books appointments, views medical history, diagnostic reports, and pays bills
- **Doctor** — manages schedule, reviews patient records and diagnostic reports, tracks daily consultations
- **Receptionist** — registers walk-ins, manages appointments, checks doctor availability, generates invoices
- **Laboratory Technician** — uploads and manages diagnostic reports (pathology, X-ray, ECG, ultrasound)
- **Administrator** — oversees doctors, departments, user accounts, billing, and system-wide reports

## ⚙️ Process Model

The **Evolutionary Prototyping Model** was chosen for this project: an initial working prototype was built from indirect research (Radium's public info, existing HMS platforms, informal doctor/patient feedback) rather than a formal sign-off from the client, then evaluated and refined through iterative stakeholder feedback until it matures into the final system.

```
Requirements Gathering → Quick Design → Build/Refine Prototype → Stakeholder Evaluation → Final System
                                              ▲                          │
                                              └───────── Refine ─────────┘
```

## 🖼️ UI/UX Design (Figma Prototypes)

All screens below are Figma prototypes designed per role. Full-resolution files are in [`/screenshots`](./screenshots).

<details open>
<summary><b>🧑‍⚕️ Patient Portal</b></summary>

| Login | Registration | Dashboard |
|---|---|---|
| ![Login](screenshots/01-patient/01-login.png) | ![Registration](screenshots/01-patient/02-registration.png) | ![Dashboard](screenshots/01-patient/03-dashboard.png) |

| Book Appointment | My Appointments | Medical History |
|---|---|---|
| ![Book Appointment](screenshots/01-patient/04-book-appointment.png) | ![My Appointments](screenshots/01-patient/05-my-appointments-cancel.png) | ![Medical History](screenshots/01-patient/06-medical-history.png) |

| Diagnostic Report | Billing & Payments | Profile |
|---|---|---|
| ![Diagnostic Report](screenshots/01-patient/07-diagnostic-report.png) | ![Billing](screenshots/01-patient/08-billing-payments.png) | ![Profile](screenshots/01-patient/09-profile.png) |

</details>

<details>
<summary><b>👨‍⚕️ Doctor Portal</b></summary>

| Login | Dashboard | My Schedule |
|---|---|---|
| ![Login](screenshots/02-doctor/01-login.png) | ![Dashboard](screenshots/02-doctor/02-dashboard.png) | ![My Schedule](screenshots/02-doctor/03-my-schedule.png) |

| Appointments | Patient Records | Diagnostic Reports |
|---|---|---|
| ![Appointments](screenshots/02-doctor/04-appointments.png) | ![Patient Records](screenshots/02-doctor/05-patient-records.png) | ![Diagnostic Reports](screenshots/02-doctor/06-diagnostic-reports.png) |

| Profile |
|---|
| ![Profile](screenshots/02-doctor/07-profile.png) |

</details>

<details>
<summary><b>🖥️ Receptionist Portal</b></summary>

| Login | Care Desk Dashboard | Appointment Management |
|---|---|---|
| ![Login](screenshots/03-receptionist/01-login.png) | ![Dashboard](screenshots/03-receptionist/02-dashboard.png) | ![Appointment Management](screenshots/03-receptionist/03-appointment-management.png) |

| Billing & Invoice | Register Patient | Doctor Schedule |
|---|---|---|
| ![Billing](screenshots/03-receptionist/04-billing-invoice.png) | ![Register Patient](screenshots/03-receptionist/05-register-patient.png) | ![Doctor Schedule](screenshots/03-receptionist/06-doctor-schedule.png) |

| Profile |
|---|
| ![Profile](screenshots/03-receptionist/07-profile.png) |

</details>

<details>
<summary><b>🧪 Laboratory Technician Portal</b></summary>

| Login | Dashboard | Patient Reports |
|---|---|---|
| ![Login](screenshots/04-lab-technician/01-login.png) | ![Dashboard](screenshots/04-lab-technician/02-dashboard.png) | ![Patient Reports](screenshots/04-lab-technician/03-patient-reports.png) |

| Upload Report | Profile |
|---|---|
| ![Upload Report](screenshots/04-lab-technician/04-upload-report.png) | ![Profile](screenshots/04-lab-technician/05-profile.png) |

</details>

<details>
<summary><b>🛡️ Administrator Portal</b></summary>

| Login | Dashboard | Manage Doctors |
|---|---|---|
| ![Login](screenshots/05-admin/01-login.png) | ![Dashboard](screenshots/05-admin/02-dashboard.png) | ![Manage Doctors](screenshots/05-admin/03-manage-doctors.png) |

| Manage Departments | User Accounts | Billing & Payments |
|---|---|---|
| ![Manage Departments](screenshots/05-admin/04-manage-departments.png) | ![User Accounts](screenshots/05-admin/05-user-accounts.png) | ![Billing](screenshots/05-admin/06-billing-payments.png) |

| Reports | Settings |
|---|---|
| ![Reports](screenshots/05-admin/07-reports.png) | ![Settings](screenshots/05-admin/08-settings.png) |

</details>

## 🗂️ Repository Structure

```
.
├── README.md
├── docs/
│   └── SE_-_Project_Report_Group_C.pdf     # Full SRS / project report
└── screenshots/
    ├── 01-patient/
    ├── 02-doctor/
    ├── 03-receptionist/
    ├── 04-lab-technician/
    └── 05-admin/
```

## 🧩 Use Case Summary

- **Shared use cases:** `Login` (all 5 actors) · `View Diagnostic Report` (Patient + Doctor) · `Manage Billing & Payment` (Receptionist + Administrator)
- **Patient:** Register, Login, Manage Profile, Search Doctor, Book/Cancel Appointment, View Appointment Status, View Medical History, View Diagnostic Report
- **Doctor:** Login, View Schedule, View Patient Record, Update Consultation
- **Receptionist:** Login, Register Patient, Update Patient Information, Manage Appointment, Check Doctor Availability
- **Laboratory Technician:** Login, Upload Diagnostic Report, Update Diagnostic Report
- **Administrator:** Login, Manage Users, Manage Doctors, Manage Departments, Manage Billing, Generate Reports, View Dashboard

## 📋 Non-Functional Highlights

- 🔒 **Security** — role-based access control, protected patient data
- ⚡ **Performance** — near-instant response for search/booking under normal load
- 📈 **Scalability** — supports growing patients, doctors, and diagnostic volume
- 🕒 **Availability** — accessible for online booking outside office hours
- 🎯 **Usability** — simple, low-training interface for patients and staff
- 💾 **Data Backup** — regular automated backups of records and reports

## 👨‍👩‍👧 Team — Group C, Section DD

| Name | Student ID | Module Owned |
|---|---|---|
| Samia Afruz Asha | 24-57314-2 | Patient Module |
| Munish Sarker | 24-57375-2 | Doctor & Admin Module |
| Rinko Rani Vadra | 24-58043-2 | Reception & Laboratory Module |

## 📎 Project Board

Task tracking and progress were managed on Trello: **[Radium Diagnostic Center (Group C)](https://trello.com/b/UB4WUSAL)**

## 📄 Full Documentation

The complete Software Requirements Specification — including background & problem analysis, process model justification, Gantt chart, user stories, requirements traceability matrix, and use case diagram — is available in [`docs/SE_-_Project_Report_Group_C.pdf`](./docs/SE_-_Project_Report_Group_C.pdf).

---

<div align="center">

Built as a Software Engineering course project at AIUB · Summer 2025-2026

</div>
