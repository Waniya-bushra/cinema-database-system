# 🎬 Cinema Database System

### Built with Oracle SQL & Oracle APEX

👨‍💻 **Developer:** Waniya Bushra  
🛠️ **Tools Used:** Oracle APEX 24.2 | Oracle Database  
📂 **Project Type:** Database Management System (DBMS)

---

# 📌 Project Overview

The Cinema Database System is a fully functional database management application developed using Oracle SQL and Oracle APEX.

This system is designed to manage:

- Movies
- Theaters
- Showtimes
- Customers
- Ticket Bookings
- Payments
- Invoices

The application provides an organized and user-friendly environment for handling cinema operations efficiently.

---

# 🗄️ Database Structure

The project contains 9 main tables:

| Table Name | Purpose |
|---|---|
| USERSS | Manages users and roles |
| GENRESS | Stores movie genres |
| THEATERSS | Stores theater details |
| MOVIESS | Stores movie information |
| CUSTOMERSS | Stores customer records |
| SHOWTIMESS | Handles movie schedules |
| TICKETSS | Manages ticket bookings |
| PAYMENTSS | Stores payment details |
| INVOICESS | Generates invoices |

---

# 🔑 Main Features

✅ Movie Management  
✅ Theater & Showtime Management  
✅ Customer Registration  
✅ Ticket Booking System  
✅ Payment Tracking  
✅ Invoice Generation  
✅ Role-Based User Access  
✅ Data Integrity Constraints  
✅ Oracle APEX Web Interface  

---

# 🔒 Database Security & Constraints

- Primary Keys and Foreign Keys implemented
- Unique constraints applied where required
- CHECK constraints used for validation
- Trigger prevents invoice deletion
- Double booking prevention implemented

---

# ⚙️ Technologies Used

| Technology | Purpose |
|---|---|
| Oracle SQL | Database creation & queries |
| Oracle APEX 24.2 | Web application development |
| PL/SQL | Trigger & database logic |
| Oracle Database | Data storage |

---

# 🔥 Trigger Used

The following trigger prevents deletion of invoices to maintain financial integrity:

```sql
CREATE OR REPLACE TRIGGER prevent_invoice_delete
BEFORE DELETE ON invoicess
FOR EACH ROW
BEGIN
    RAISE_APPLICATION_ERROR(-20001, 'Invoice deletion is not allowed.');
END;
```

---

# 🚀 How to Run the Project

## Step 1 — Open Oracle APEX

Navigate to:

SQL Workshop → SQL Commands

---

## Step 2 — Run SQL Script

- Copy the complete SQL script
- Paste it into SQL Commands
- Click Run

---

## Step 3 — Insert Sample Theater Data

```sql
INSERT INTO theaterss (theater_name, capacity, category)
VALUES ('A1', 300, 'PLATINUM');
```

```sql
INSERT INTO theaterss (theater_name, capacity, category)
VALUES ('B1', 500, 'GOLD');
```

```sql
INSERT INTO theaterss (theater_name, capacity, category)
VALUES ('C1', 700, 'SILVER');
```

```sql
COMMIT;
```

---

## Step 4 — Create Oracle APEX Application

1. Open App Builder
2. Create New Application
3. Add pages for each table
4. Run the application

---

# 📊 Entity Relationship Overview

```text
GENRESS ──────────── MOVIESS
                        │
                    SHOWTIMESS ──── THEATERSS
                        │
                    TICKETSS ──── CUSTOMERSS
                        │
                    PAYMENTSS
                        │
                    INVOICESS
```

---

# 📌 Developer Notes

- Double "SS" naming convention avoids Oracle reserved keyword conflicts
- IDENTITY columns are used for auto-increment IDs
- Database normalization principles are applied
- Oracle APEX used for frontend application development

---

# 👨‍💻 Developed By

## Waniya Bushra

🎓 Database Management System Project  
📅 2026

---

⭐ If you like this project, feel free to star the repository.

*Cinema Database System — Developed by Waniya Bushra*
