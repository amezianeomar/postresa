# POSTRESA — PFE (OFPPT DEVWFS) 2025–2026

POSTRESA is an integrated platform for **space reservations** and **institutional communication** inside a training center.

It follows a strict **4‑role architecture**:
- **Stagiaire**
- **Prof**
- **Admin**
- **Super Admin**

## Monorepo structure (strict)

```text
POSTRESA/
├── frontend/          # React (Vite) + Tailwind + Redux Toolkit
├── backend/           # Laravel (native, Composer initialized)
├── docs/              # UML + system architecture
└── report/latex/       # Academic report (LaTeX)
```

> Note: DB migrations/seeders live **natively** in `backend/database/` (Laravel standard). No external `data/` folder for migrations.

## Tech stack & hosting

### Frontend
- React (Vite)
- Tailwind CSS
- **Redux Toolkit** (mandatory)
- Hosting: **Vercel**

### Backend
- Laravel (PHP)
- Hosting: **Render**

### Databases (Hybrid)
- **MySQL (Alwaysdata)**: core relational data (users/roles/rooms/reservations)
- **MongoDB (Atlas)**: announcements/comments/likes + global activity logs

### Storage
- **Cloudinary** for image uploads (store only URLs in DB)

## Modules

### Reservation (MySQL)
- Rooms/resources catalog
- Availability calendar
- Reservation requests with workflow: pending → approved/refused
- Admin blocking for fixed schedule

### Social / Publications (MongoDB)
- Announcements feed
- Visibility targeting (school/class/specific users)
- Likes & comments

### Messaging
- Integrated messaging between stagiaires and profs

### Supervision / Logs (MongoDB)
- Activity logs per school (Admin)
- Global logs across schools (Super Admin)

## Getting started (local)

> The repo is being initialized. Commands and environment setup will be added as soon as `frontend/` and `backend/` are generated.

## Authors
- Omar Ameziane
- Soulayman Elkharraz