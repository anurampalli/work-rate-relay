# 📘 Work Rate Relay

Work Rate Relay is a ServiceNow scoped application designed to streamline employee performance reviews by automating data entry, notification delivery, and reporting. Built using ServiceNow Studio and Git source control, this project showcases practical application development across custom tables, workflows, email notifications, and real-time analytics.

This app was developed as part of a training project to demonstrate end-to-end capabilities in ServiceNow development — including table design, email triggers, report configuration, and scoped app packaging.

---

## 🛠 Technologies Used

- ServiceNow Studio (Scoped Application)
- Git Integration with Source Control
- ServiceNow Tables & Dictionary
- Email Notifications
- Pie Chart Reporting
- HTML Fields & Choice Fields

---

## 📁 Application Modules

| Module           | Description                                                                 |
|------------------|-----------------------------------------------------------------------------|
| Employee Table   | Stores employee name (linked to sys_user), and their work done for FY24     |
| Manager Table    | Stores manager's reviews, ratings, and linked employee                      |
| Email Notifications | Auto-send to manager when employee logs entry; notify employee when rated |
| Rating Reports   | Pie chart view summarizing employee ratings                                 |

---

## 🧾 Table Structures

🧑‍💼 Employee Table
- Employee ID (auto-generated)
- Employee Name (Reference: sys_user)
- Work Done in FY24 (HTML)

👨‍💼 Manager Table
- Manager Name (Reference: sys_user)
- Employee Name (Reference: sys_user)
- Performance Review (HTML)
- Rating (Choice: Excellent, Very Good, Good, Bad)

---

## 🔔 Email Notification Logic

- When an employee creates a new record, the system:
  - Sends an email to the assigned manager
  - Includes all "Work Done in FY24" details

- When a manager updates the rating field:
  - The system sends an email to the employee
  - Includes the rating and performance review text

Emails are triggered using standard Notification Rules configured via Conditions and Template Variables.

---

## 📊 Report Generation

- Pie Chart report categorizes employee performance by rating level:
  - Excellent: 2 employees
  - Very Good: 5 employees
  - Good: N employees
  - Bad: N employees

- Accessible via Reporting → Create New → Chart → Table: Manager

---

## 🧩 Update Set Strategy

- The application changes are stored in an Update Set called:
  Work Rate Relay – Core Setup

- This allows easy export/import into other instances if needed.

---

## 💻 Setup & Import Guide

1. Clone this repository.
2. Open your PDI (Personal Developer Instance).
3. Go to Studio → Import from Source Control.
4. Connect to this GitHub repo and pull changes.
5. Activate Email Notification Plugin (if not already enabled).
6. Preview and commit each file in the Update Set to move changes.

---

## 📷 Screenshots (to be added)

- Form layout for Employee table
- Manager review interface
- Example email template
- Sample Pie Chart report

---

## 👤 About the Developer

Hi, I’m Anu — a developer passionate about business process automation and ITSM platforms. This project reflects my learning journey in ServiceNow platform development, and I hope it helps others
