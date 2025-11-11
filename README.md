# 🚗 Car Workshop — Appointment Booking System

A **Next.js + Express.js** full-stack web application for managing car service appointments.
Users can **book appointments by date, time, and preferred mechanic**, with real-time availability tracking.
The system guarantees a **reliable, A-class service** experience by preventing double-booking and restricting bookings to **authenticated users only**.

<img width="1343" height="635" alt="image" src="https://github.com/user-attachments/assets/1fff4120-3c1e-41e4-aee0-ae8f8e8b4e88" />


---

## 🧭 Overview

**Car Workshop** modernizes how workshops handle customer appointments.
The platform enables customers to:

* Choose a **service date and time** via a calendar picker
* Select a **mechanic** based on live availability
* Manage bookings securely through a personal account

The backend ensures only verified, available mechanics appear for booking — and users **must log in or sign up before placing an appointment**, ensuring reliability and accountability.

---

## ✨ Features

### 🗓️ Smart Appointment Booking

* Calendar-based date & time selection
* Displays only available slots
* Prevents overlapping or duplicate appointments

### 🔐 User Authentication

* **Secure login & registration** system using JWT
* Users must be authenticated before booking an appointment
* Unauthorized users cannot access appointment functions

<img width="1355" height="632" alt="image" src="https://github.com/user-attachments/assets/b13e3cfb-a39e-4909-8406-4b18ebc427d3" />

<img width="1356" height="632" alt="image" src="https://github.com/user-attachments/assets/c8214c96-8221-491e-ab91-65aa93450be9" />


### 🧑‍🔧 Mechanic Availability

* Real-time mechanic schedules
* Mechanic profile includes name, specialization, and availability
* Users can select their **preferred mechanic**

### ⚙️ Admin Dashboard (optional)

* Add, edit, or remove mechanics
* Define working hours and off days
* Monitor appointments with live database integration

### 🧱 Database Integration

* Uses **MongoDB Atlas** for data persistence
* Three main collections:

  * `users` — stores credentials and roles
  * `mechanics` — manages mechanic data and schedules
  * `appointments` — tracks bookings

<img width="1358" height="632" alt="image" src="https://github.com/user-attachments/assets/e20c45af-10a6-446d-b872-fc0376f2f35f" />


---

## 🧩 Tech Stack

| Layer                 | Technology                    |
| --------------------- | ----------------------------- |
| **Frontend**          | Next.js (React), Tailwind CSS |
| **Backend**           | Express.js, Node.js           |
| **Database**          | MongoDB Atlas                 |
| **Authentication**    | JSON Web Token (JWT)          |
| **API Communication** | RESTful API (Axios / Fetch)   |

---

## 🚀 Getting Started

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/utshobbose/Car-Workshop.git
cd Car-Workshop
```

### 2️⃣ Install Dependencies

#### Backend

```bash
cd backend
npm install
```

#### Frontend

```bash
cd frontend
npm install
```

### 3️⃣ Configure Environment Variables

Create a `.env` file in the **backend** directory:

```env
PORT=5000
DATABASE_URL=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
```

---

## ⚙️ Run the Project

### Start the Backend

```bash
cd backend
npm run dev
```

### Start the Frontend

```bash
cd frontend
npm run dev
```

Then open:

* Frontend → `http://localhost:3000`
* Backend → `http://localhost:5000`

---

## 🧠 Workflow

1. User visits the homepage and clicks **“Book Now.”**
2. If not logged in, they are redirected to the **Login / Sign Up** page.
3. Once authenticated, they select a **date** and **time**.
4. The backend checks mechanic availability.
5. User chooses a **mechanic** and confirms the booking.
6. Appointment is saved in the MongoDB database.

This workflow ensures a **secure, authenticated, and conflict-free booking** experience.

---

## 🧮 Example API Routes

| Method   | Endpoint                               | Description                             |
| -------- | -------------------------------------- | --------------------------------------- |
| `POST`   | `/api/auth/signup`                     | Register new user                       |
| `POST`   | `/api/auth/login`                      | Authenticate user                       |
| `GET`    | `/api/mechanics`                       | Fetch all mechanics                     |
| `GET`    | `/api/mechanics/available?date=&time=` | Get available mechanics                 |
| `POST`   | `/api/appointments`                    | Create appointment (authenticated only) |
| `GET`    | `/api/appointments`                    | Fetch user’s appointments               |
| `DELETE` | `/api/appointments/:id`                | Cancel appointment                      |

---

## 🌟 Future Enhancements

* Email / SMS booking confirmations
* Mechanic reviews and ratings
* Online payment integration
* Admin analytics dashboard
* Booking reminders and notifications

---




