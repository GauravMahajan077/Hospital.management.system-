# 📚 Learning Management System (LMS)

A **feature-rich desktop LMS** built with **PyQt6** and **SQLite**, designed to streamline academic workflows for both **students** and **administrators**.  
It unifies course management, material delivery, tasks, announcements, reminders, notes, calendar events, and progress tracking into one modern, responsive interface.

---

## 🚀 Features

### 👤 Role-Based Access Control
- **Student** — Access enrolled courses, tasks, notes, reminders, and personal progress reports.
- **Admin** — Full CRUD control over courses, announcements, events, and student performance.

### 📦 Course & Material Management
- Upload/manage PDFs (with page count tracking) and videos.
- Safe deletion with cascading cleanup of related progress data.
- Card-based course dashboard with progress indicators.

### 📄 PDF & Video Access
- **Custom PDF Viewer** with page-resume functionality.
- Video playback via system player.
- Persistent per-user progress tracking.

### 📝 Tasks, Announcements & Reminders
- Student-created tasks with deadlines.
- Admin announcements as trackable tasks with approval workflows.
- Personal reminders for deadlines and important dates.

### 🗒️ Notes & Event Calendar
- Rich-text **My Notes** with inline image support.
- Calendar with color-coded events (holidays, academic days, etc.).

### 📊 Progress Analytics & Reports
- Real-time bar/pie charts using **matplotlib**.
- Auto-generated PDF progress reports (grades, achievements, remarks, signatures) stored in DB.

### 🎨 Modern UI/UX
- **Dark/Light themes**, collapsible sidebar, adaptive layouts.
- Dialog-based editing, viewing, and confirmation actions.

### 🔒 Security & Data Integrity
- SQLite backend with **foreign key constraints**.
- PBKDF2-hashed credentials.
- Input validation and guarded destructive actions.

---

## 🛠️ Tech Stack
- **Frontend/UI**: [PyQt6](https://pypi.org/project/PyQt6/)
- **Backend**: Python 3
- **Database**: SQLite (local, FK constraints enabled)
- **Data Visualization**: matplotlib
- **PDF Reports**: reportlab

---

## 📂 Project Structure
