# DEPI-Project
Graduation Project for DEPI

Project Name: ICU Reservation & Management System
Team members:
Mahmoud Mohamed Mahmoud
Mohamed tarek
Moahmed Hosam
Saad Elsokkary
Nourhan mohamed



🧩 1. Project Planning Summary
Goal:
Develop a smart, automated ICU reservation and management system to handle bed allocation, ambulance tracking, and patient flow efficiently.
Methodology:
Agile (2-week sprints)
Duration:
6 months (9 phases)
Core Tech Stack:
    • Frontend: React + Tailwind + Socket.io-client
    • Backend: Node.js + Express + PostgreSQL + Prisma
    • Infra: Docker + AWS + GitHub Actions
    • Testing: Jest, Cypress, Postman
Team Roles:
    • 1× Project Manager
    • 2–3× Full-Stack Developers
    • 1× UI/UX Designer
    • 1× QA Engineer
    • 1× DevOps Engineer (part-time)



👥 2. Stakeholder Analysis
Stakeholder	Role / Responsibility	Goals	Influence	Interest
Hospital Admin	System owner, full access, user management, reporting	Ensure ICU efficiency and staff accountability	High	High
ICU Manager	Oversees bed usage, approves reservations	Maintain optimal ICU occupancy	High	High
Receptionist	Handles patient check-in/out	Smooth admissions/discharges	Medium	High
Ambulance Staff	Receives transport updates	Quick patient transfer	Medium	Medium
Dev Team	Builds and maintains system	Deliver reliable, scalable system	High	High
QA Engineer	Ensures software quality	Minimize bugs and downtime	Medium	High
Patients / Families	Indirect users	Timely ICU allocation	Low	High

🗃 3. Database Design (Conceptual Overview)
Main Entities:
    • Users
    • id, name, email, role, password_hash
    • Roles
    • id, role_name, permissions
    • ICU_Beds
    • id, bed_number, status, last_cleaned, assigned_patient_id
    • Reservations
    • id, patient_name, priority, status, created_by, approved_by, bed_id
    • Ambulances
    • id, driver_name, status, location, assigned_reservation_id
    • Logs
    • id, user_id, action_type, timestamp, details

Relationships:
    • User (1) → Reservation (many)
    • Reservation (1) → ICU_Bed (1)
    • Reservation (1) → Ambulance (1)
    • User (1) → Logs (many)



The Design: https://www.figma.com/make/wTeXxzI3bXvJcnQ3LZ4uzw/ICU-Reservation-Dashboard-UI?fullscreen=1
