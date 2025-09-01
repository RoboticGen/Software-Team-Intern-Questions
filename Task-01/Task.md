# Full Stack - Interview Task

# 🚨 Software Implementation Task — NFC-Based Security Logger System

## 👤 Role

You are a **Software Engineer** tasked with building a working prototype of a digital security logging system used in public locations (ATMs, banks, buildings, etc.). The goal is to replace the current manual book-signing method with a fully automated NFC-based system.

---

## 📘 Project Summary

Security officers scan **NFC tags** that are fixed at designated locations during their patrol. These scans automatically log the **officer ID**, **location ID**, and **timestamp** into the system. Admin users monitor patrol progress via a secure dashboard.

You are required to build

- ✅ A **backend** (with all logic & database)
- ✅ A **frontend** (admin dashboard)
- ✅ A **mobile app simulator** (Python CLI script to simulate NFC Scanning behavior [ Sketch Provided ])

> Use of AI tools (e.g., ChatGPT, GitHub Copilot) is highly encouraged.
> 
> 
> Be transparent about how they were used by documenting it in your report.
> 

---

## 🧭 System Flow Overview

### 🔄 Main Process

1. Security officer logs into the system via the **mobile app simulator**.
2. Officer **starts a patrol**, which creates a new session.
3. Officer **scans multiple NFC tags** at predefined locations.
4. Officer **ends the patrol**.
5. Admin can
    - View all logs and patrols.
    - Filter logs by officer, location, patrol, or date.
    - View a **map** of scanned locations in patrol order.
    - View Analytics
    - **Export reports** per officer, patrol, or location.

---

## 🛠️ Tech Stack

| Layer | Tech ( Preferred ) |
| --- | --- |
| Backend | FastAPI (Python) |
| Frontend | Next.js + Shadcn UI |
| NFC Simulation | Python script (Sketch will be provided) |
| Database | SQLite  |

---

## 🎯 Core Requirements

### 🔹 Backend

- Authentication and Authorization ( Admin can view data, Officers can only scan )
- Relevant API Endpoints for the dashboard with CRUD operations
- API endpoint to **log a scan event**

### 🔹 Admin Dashboard

- Displays list of logs with filters (by officer, date, location, patrol)
- Analytics view
- Map of scanned places in order for a selected petrol
- Exportable reports by patrol, location, or officer
- ***Sample pages to Implement***
    - *Login page (admin)*
    - *Logs Table (filter by date, officer, location)*
    - *Map View of locations in Patrol with order*
    - *Analytics View (basic stats)*
    - *Reports Page (export to CSV or PDF per  officer, patrol, location)*

---

## 📦 Expected Deliverables

### 🔹 Source Code

- Full working code for
    - Backend
    - Frontend (Admin Dashboard)
    - Python mobile app simulator script

### 🔹 Markdown Documentation

- `README.md` and separate docs explaining
    - How to set up and run each component (backend, frontend, script)
    - Explanation of your architecture and components
    - AI tool usage documentation *(What prompts/tools did you use?)*

### 🔹 Final Report (in PDF or Markdown)

- Include
    - Total time spent (use a time tracker)
    - Problems you encountered and how you solved them
    - Things you learned
    - Extra features or improvements you added

---

## ✅ Evaluation Criteria

| Component | Criteria |
| --- | --- |
| Backend Functionality | Fully working API with CRUD and role-based auth |
| Frontend Functionality | Clean, elegant UI with working filters, map, analytics |
| Patrol Simulator | Officer script simulates realistic flow |
| Reports & Exports | Works correctly, filtered and downloadable |
| Code Quality | Clean, modular, documented |
| Documentation | Clear setup, system explanation, and AI usage summary |
| Extra Features | Depending on the features |
| Best Practices | Secure auth, code structure, reusability |

> Bonus Points: for extra features, creativity, and well-documented AI-assisted development.
> 

---

## 🧪 Dummy Data

The following files are included in `/Dummy-Data/` to help you start

| `Users.csv` | `Locations.csv` |
| --- | --- |
| Admin + 3 Officers | 6 predefined locations with NFC tags & coordinates |

---

## 🔗 Set up Project

Use the following GitHub Classroom link to access the starter repository:

👉 [https://classroom.github.com/a/DuSG6Wi0](https://classroom.github.com/a/DuSG6Wi0)

- Clone the repository
- Complete your implementation in the given structure
- Push your final code before the deadline

---

## 📅 Deadlines

| Type | Date |
| --- | --- |
| Soft Deadline | 2025-05-04 |
| Hard Deadline | 2025-05-06 |

> After the hard deadline, submissions may not be graded.
> 

---

## 📬 Contact

For questions or issues:

📧 [**dev@roboticgen.co**](mailto:dev@roboticgen.co)

---

## References

### UI

https://github.com/birobirobiro/awesome-shadcn-ui

https://ui.shadcn.com/

### Backend

https://fastapi.tiangolo.com/

### Frontend

https://nextjs.org/

https://sqlite.org/

---

## Hints

You may need to implement following core features to fulfill the requirement 

### Backend

- JWT-based **authentication and authorization**
    - Role : `admin` and `officer`
- Core CRUD APIs
    - Officers/Admin
    - Locations
    - Patrol Sessions
    - Scan Logs
- Core APIs:
    - `POST /auth/login`
    - `POST /patrol/start`
    - `POST /patrol/scan`
    - `POST /patrol/end`
    - `GET /logs`, `GET /analytics`, `GET /report`, `GET /map-data`

### 📲 Mobile App Simulator (Python Script)

Simulates a security officer

- Login
- Start patrol
- Scan NFC cards
- End patrol

---