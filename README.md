# Infinity-Drones-Pilot-Portal
The portal aims to streamline day-to-day flight management and track pilot performance efficiently. We utilized NodeJS as the backend technology and I designed a scalable AWS infrastructure to ensure smooth user experiences and sustainable operations. http://infinitydronespilotportal.eu-north-1.elasticbeanstalk.com/login 


# **PilotPortal** 🛩️

*A full-stack web application designed to manage drone pilot training, flight operations, crash reporting, and automated notifications for both pilots and administrators.*

PilotPortal streamlines pilot activity tracking, enhances safety, and automates reporting and reminders for efficient management.

---

## **🚀 Key Features**

* **User Authentication**

  * Secure signup/login with JWT and bcrypt for password hashing.

* **Profile Management**

  * Pilots can create and update their profiles, including uploading images.

* **Flight & Simulation Logging**

  * Log real and simulated flight hours for dashboards and reports.

* **Crash Reporting**

  * Report crashes, specify damaged parts, and calculate repair costs.

* **Dashboard & Analytics**

  * Interactive charts (Chart.js) for flight stats, crash history, battery usage, and more.

* **Flight Scheduling**

  * Schedule, edit, or delete upcoming flights.

* **Automated Call Reminders**

  * Twilio integration to call pilots before scheduled flights.

* **PDF Report Generation**

  * Generate detailed pilot activity reports using EJS + Puppeteer.

* **Automated Emailing**

  * Email pilots and admins every 15 days with summaries via Nodemailer.

---

## **🛠️ Technical Architecture**

* **Backend:** Node.js with Express.js (routing + business logic)
* **Frontend:** EJS templates, Bootstrap, Chart.js
* **Database:**

  * **PostgreSQL** for structured data (users, flights, schedules, crashes, costs)
  * **MongoDB** (via Mongoose) for storing pilot images & flexible data
* **File Storage:** AWS S3 (optional) for scalable image storage
* **Authentication:** JWT tokens (HTTP-only cookies), bcrypt for password security
* **Scheduling:** node-cron for automated tasks (calls, mailing)
* **External APIs:**

  * **Twilio** – automated phone calls
  * **Open-Meteo** – weather-based flight suggestions

---

## **📦 How the System Works (User Flow)**

1. **Signup/Login** – Pilots register, login, and receive JWT tokens.
2. **Profile Management** – Pilots update profiles & upload images (MongoDB/S3).
3. **Flight Logging** – Log real & simulated flights (PostgreSQL).
4. **Crash Reporting** – Submit crash details & calculate repair costs.
5. **Dashboard** – View charts summarizing flights, crashes, costs.
6. **Flight Scheduling & Reminders** – Schedule flights & get automated calls via Twilio.
7. **PDF Reports & Mailing** – Every 15 days, PDF reports sent to pilots & admins via Nodemailer.

---

## **🔒 Security Practices**

* Password hashing with **bcrypt**.
* Stateless authentication via **JWT** in HTTP-only cookies.
* Store sensitive data (DB credentials, API keys) in environment variables.
* Parameterized SQL queries to prevent injection.
* Role-based access control for admin features.

---

## **📌 Installation & Setup**

```bash
# Clone the repository
git clone https://github.com/yourusername/pilotportal.git

# Navigate to project folder
cd pilotportal

# Install dependencies
npm install

# Setup environment variables
cp .env.example .env
# Fill in DB credentials, JWT secret, API keys

# Start development server
npm run dev
```

---

## **🖼️ Tech Stack**

* **Frontend:** EJS, Bootstrap, Chart.js
* **Backend:** Node.js, Express.js
* **Database:** PostgreSQL, MongoDB
* **Storage:** AWS S3
* **Scheduler:** node-cron
* **APIs:** Twilio, Open-Meteo

---

## **📄 License**

This project is licensed under the MIT License – see the LICENSE file for details.

---


Do you want me to do that?

