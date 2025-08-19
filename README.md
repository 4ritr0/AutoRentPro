# 🚗 PrimeMotors Car Rental Dealership Management System 🚗

Welcome to **PrimeMotors** – a modern, feature-rich Car Rental Database Management System built for seamless car rental management, customer experience, and robust admin control.

---

## 📋 Table of Contents

- [Features](#features)
- [Tech Stack](#tech-stack)
- [Database Design](#database-design)
- [Setup & Usage](#setup--usage)

---

## ✨ Features

- **User Authentication** 🔐: Secure login system for customers and admins.
- **Car Browsing & Filtering** 🚙: Browse available cars with advanced filters (brand, color, type, seats, price, etc.).
- **Car Details Page** 📄: View detailed information, images, and brand logos for each car.
- **Booking Management** 📝: Book cars, manage bookings, and view booking history.
- **Admin Dashboard** 🛠️: Add, update, or remove cars, manage brands, and view analytics.
- **Availability Tracking** ✅❌: Real-time car availability status and automatic updates.
- **Service Handling** 🧰: Track and manage car service records, including last and next service dates, and service costs, ensuring every vehicle is well-maintained and up-to-date.
- **Database Triggers & Procedures** ⚡: Automatic vehicle count updates, price/status changes, and more.
- **Responsive UI** 💻: Modern, visually appealing interface with custom CSS and SVG brand logos.
- **Logout & Session Management** 🔄: Secure session handling and easy logout.
- **Clever Image Management** 🖼️: Car images are organized and named as `<Color><Car>.jpeg` (e.g., `RedNexon.jpeg`, `BlueSafari.jpeg`), making it easy to dynamically display the correct image for each car based on its attributes.

---

## 🛠️ Tech Stack

| Layer         | Technology                                  |
| ------------- | ------------------------------------------- |
| Frontend      | [Streamlit](https://streamlit.io/) (Python) |
| Backend       | Python 3.x                                  |
| Database      | MySQL                                       |
| ORM/Connector | mysql-connector-python                      |
| Styling       | Custom CSS, SVG, JPEG                       |

---

## 🗄️ Database Design

The system uses a **relational MySQL database** with the following key tables:

- `Customer`, `Dealership`, `Car_Brand`, `Car_Model`, `Insurance`, `Service`, `Delivery`, `Payment`, `Booking`, `Connection`

**Key Features:**

- Foreign key relationships for data integrity
- Triggers for automatic vehicle count updates
- Stored procedures for price/status management
- Service table for tracking maintenance history, costs, and scheduling next service for each car
- Sample data for brands, models, services, and maintenance records
- Images named as `<Color><Car>.jpeg` for easy and dynamic image retrieval

See [`test.sql`](test.sql) for full schema and sample data.

---

## 🚀 Setup & Usage

1. **Clone the repository:**
   ```sh
   git clone https://github.com/4ritr0/PrimeMotors.git
   cd AutoRentPro
   ```
2. **Install dependencies:**
   ```sh
   pip install streamlit mysql-connector-python
   ```
3. **Set up the MySQL database:**
   - Create a database and import `test.sql` to set up tables and sample data.
   - Set environment variables for DB credentials:
     - `dbmsPWD` (your MySQL password)
     - `dname` (your database name)
4. **Run the app:**
   ```sh
   streamlit run homepage.py
   ```
