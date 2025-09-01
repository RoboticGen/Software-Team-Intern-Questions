# Software Engineer Intern Task — Obo Nexus VS Code Extension

## 👤 Role

You are a **Software Engineer Intern** building a **VS Code extension** that helps students at **RoboticGen Academy** independently complete their self-learning projects. Your tool will allow students to log in, complete assigned coding tasks, and submit their solutions directly from their code editor. Mentors will use a **dashboard** to view and review submissions.

---

## 📘 Project Summary

RoboticGen Academy manages project-based learning through structured documents. These documents (currently in **ClickUp**) can be transformed into **notebook-style tasks** consisting of markdown-based instructions and coding prompts.

You are required to build a **VS Code extension** for students and a **dashboard** for mentors, along with a backend service that connects them.

---

## 🧭 System Flow Overview

### 🔄 Main Process

1. Student logs in to the **VS Code extension** via username/password (JWT auth).
2. The extension fetches
    - Assigned projects
    - Recommended projects
3. Students
    - View projects in a notebook-like editor (instructions + code cells)
    - Complete the steps
    - **Submit** their notebook/code
4. Mentor logs into the **dashboard**
5. Mentor can
    - View all submissions (filter by student, project)
    - View individual submissions and code
    - (Bonus: Add feedback/comment)

---

## 🛠️ Tech Stack

| Layer | Tech (Preferred) |
| --- | --- |
| VS Code Extension | JavaScript or TypeScript |
| Frontend Dashboard | Next.js + Shadcn UI |
| Backend | FastAPI (Python) **or** NestJS (TypeScript) |
| Auth | Username + Password → JWT |
| DB | SQLite or Postgres |

---

## 🎯 Core Requirements

### 🔹 VS Code Extension (Student Tool)

- **Login screen** (username/password → JWT saved locally)
- Sidebar: List of
    - Assigned Projects
    - Recommended Projects
    - Project Progress
- **Notebook Viewer**
    - Each project has steps (markdown + editable code area)
    - Button to **Save locally**
    - Button to **Submit notebook**

### 🔹 Backend API

- JWT-based **Authentication**
    - `POST /auth/login` → returns JWT
    - `POST /auth/register` (optional)
- Project APIs:
    - `GET /projects/assigned`
    - `GET /projects/recommended`
    - `GET /projects/:id`
    - `POST /projects/:id/submit`
- Mentor APIs:
    - `GET /submissions` → All submissions
    - `GET /submissions/:id` → View individual submission
- Role-based access: `student`, `mentor`

### 🔹 Mentor Dashboard (Next.js + Shadcn UI)

- Mentor login (JWT)
- Table View of all student submissions
    - Filters: student, project, status
- Click to view:
    - Project title
    - Student name
    - Code/notebook submitted
- (Optional): Add comment or feedback

---

## 📦 Expected Deliverables

### 🔹 Source Code

- Fully working
    - VS Code Extension
    - Backend (FastAPI or NestJS)
    - Mentor Dashboard (Next.js + Shadcn UI)

### 🔹 Documentation

- `README.md` or `/docs/` for:
    - How to set up backend, extension, and dashboard
    - Project structure and tech decisions
    - How authentication works (JWT)
    - AI usage disclosure *(if any)*

### 🔹 Final Report

Include

- Time spent
- Issues encountered and solutions
- What you learned
- Bonus features implemented

> Use of AI tools (e.g., ChatGPT, GitHub Copilot, Cursor) is highly encouraged.
> 
> 
> Be transparent about how they were used by documenting it in your report.
> 

---

## ✅ Evaluation Criteria

| Component | Criteria |
| --- | --- |
| VS Code Extension | Smooth UX, notebook functionality, working auth |
| Mentor Dashboard | Filterable view, readable submissions |
| Backend | Secure auth, clean API design |
| Code Quality | Modular, readable, documented |
| Docs & Report | Clear setup and reasoning |
| Bonus Points | Language Model Integration, autosave, creative features |

---

## 🧪 Sample Data

You will use following two projects 

1. **Recipe Organizer -** https://doc.clickup.com/37017639/p/h/139p17-33878/d920535b81cb35d (Assigned Project)
2. **Treasure Hunt Game -** https://doc.clickup.com/37017639/p/h/139p17-34838/0d0fd4a64234e6c (Suggested Project)

Use following users

[Users](Software%20Engineer%20Intern%20Task%20%E2%80%94%20Obo%20Nexus%20VS%20Code%20%2021bbda01018c809598e7e8fe125b51f8/Users%2021bbda01018c80a7bad1c7b6ab584a94.csv)

---

## 🔗 Starter Repository

👉 [https://classroom.github.com/a/T0t5OTfz](https://classroom.github.com/a/T0t5OTfz)

- Clone the repository
- Each subfolder (`/backend`, `/mentor-dashboard`, `/obo-nexus-editor`) is scaffolded
- Complete your work and push your final version

---

## 📅 Deadlines

| Type | Date |
| --- | --- |
| Soft Deadline | 2025-07-06 |
| Hard Deadline | 2025-07-11 |

---

## 📬 Contact

For technical clarifications:

📧 [**dev@roboticgen.co**](mailto:dev@roboticgen.co)

---

## References

### VS Code Extension

- [https://code.visualstudio.com/api](https://code.visualstudio.com/api)
- [https://code.visualstudio.com/api/get-started/your-first-extension](https://code.visualstudio.com/api/get-started/your-first-extension)
- [https://code.visualstudio.com/api/extension-guides/notebook](https://code.visualstudio.com/api/extension-guides/notebook)
- [https://github.com/microsoft/vscode-extension-samples](https://github.com/microsoft/vscode-extension-samples)

### Frontend

- [https://nextjs.org/](https://nextjs.org/)
- [https://ui.shadcn.com/](https://ui.shadcn.com/)

### Backend

- [https://fastapi.tiangolo.com/](https://fastapi.tiangolo.com/)
- [https://docs.nestjs.com/](https://docs.nestjs.com/)
- [https://jwt.io/](https://jwt.io/)

## 💡 Additional Features (Suggestions)

- You can integrate copilot features and other language models directly into extension like a tutor for the task.
- Ref
    - [https://code.visualstudio.com/api/extension-guides/language-model](https://code.visualstudio.com/api/extension-guides/language-model)
    - [https://code.visualstudio.com/api/extension-guides/chat](https://code.visualstudio.com/api/extension-guides/chat)