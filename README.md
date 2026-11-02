# Beauty Parlour Management System (BPMS)

A PHP and MySQL-based web application designed to simplify beauty parlour operations by managing customer registrations, service information, appointment bookings, billing, enquiries, and administrative activities through a centralized platform.

## Overview

The **Beauty Parlour Management System (BPMS)** provides two main interfaces:

- **Customer Panel:** Allows customers to register, log in, explore available beauty services, book appointments, and view their booking and invoice history.
- **Admin Panel:** Allows administrators to manage appointments, customers, services, invoices, enquiries, and business reports.

The application aims to reduce manual record-keeping and make routine parlour management activities easier to organize.

## Key Features

### Customer Module

- Customer registration and login
- Customer profile management
- Password change and recovery pages
- Browse available beauty services
- Book appointments by selecting a date and time
- View appointment booking history
- View invoice history
- Submit enquiries through the contact page

### Admin Module

- Admin authentication
- Dashboard for administrative activities
- View and manage customer records
- Add, edit, and manage beauty services
- View all appointments
- Approve or reject appointment requests
- Search and review appointment records
- Manage invoices and billing records
- View and manage customer enquiries
- Generate sales reports
- Generate date-wise reports
- Update administrative profile and password

## Technology Stack

| Component | Technology |
|---|---|
| Frontend | HTML, CSS, JavaScript |
| Styling | Bootstrap |
| Backend | PHP |
| Database | MySQL |
| Database Connectivity | MySQLi |
| Local Development Environment | XAMPP / WAMP / LAMP |

## Project Structure

```text
Beauty-Parlour-Management-System-PHP/
│
├── bpms/
│   ├── admin/
│   │   ├── Dashboard and administration pages
│   │   ├── Appointment management
│   │   ├── Customer management
│   │   ├── Service management
│   │   ├── Invoice management
│   │   ├── Reports
│   │   ├── css/
│   │   ├── js/
│   │   └── includes/
│   │
│   ├── assets/
│   │   ├── css/
│   │   ├── js/
│   │   ├── images/
│   │   └── videos/
│   │
│   ├── includes/
│   ├── index.php
│   ├── services.php
│   ├── book-appointment.php
│   ├── booking-history.php
│   ├── invoice-history.php
│   ├── profile.php
│   ├── login.php
│   ├── signup.php
│   └── bpmsdb.sql
│
└── Readme.txt
```

## Installation and Setup

Follow these steps to run the project locally.

### 1. Install the Requirements

Install a local PHP development environment such as [XAMPP](https://www.apachefriends.org/) that includes Apache, PHP, and MySQL.

### 2. Clone the Repository

```bash
git clone <YOUR-GITHUB-REPOSITORY-URL>
```

### 3. Move the Project Folder

Extract the project and copy the `bpms` folder into the XAMPP web directory:

```text
C:\xampp\htdocs\
```

The expected application location is:

```text
C:\xampp\htdocs\bpms\
```

### 4. Start Apache and MySQL

Open the XAMPP Control Panel and start:

- Apache
- MySQL

### 5. Create the Database

Open phpMyAdmin:

```text
http://localhost/phpmyadmin
```

Create a database named:

```text
bpmsdb
```

### 6. Import the Database

1. Select the `bpmsdb` database.
2. Open the **Import** tab.
3. Select the `bpms/bpmsdb.sql` file from the project.
4. Click **Import** or **Go**.

The SQL file contains the database tables and sample records required by the application.

### 7. Configure Database Connection

The database connection is configured in:

```text
bpms/includes/dbconnection.php
bpms/admin/includes/dbconnection.php
```

The supplied configuration uses:

```php
$con = mysqli_connect("localhost", "root", "", "bpmsdb");
```

Adjust the host, username, password, and database name if your local MySQL configuration is different.

### 8. Run the Application

Open the customer-facing application:

```text
http://localhost/bpms/
```

Open the admin panel:

```text
http://localhost/bpms/admin/
```

## Demo Login Credentials

The original project documentation provides the following credentials.

**Admin Panel**

```text
Username: admin
Password: Test@123
```

**Customer Login**

```text
Email: johndoe12@gmail.com
Password: Test@123
```

You can also register a new customer account through the signup page.

*Note: These are sample credentials from the supplied project database/documentation. Change default credentials before using the application beyond a local demonstration.*

## Database Overview

The supplied SQL database is named `bpmsdb`.

Its main tables include:

| Table | Purpose |
|---|---|
| `tbladmin` | Administrator account details |
| `tbluser` | Customer account details |
| `tblservices` | Beauty parlour services and costs |
| `tblbook` | Appointment booking records |
| `tblinvoice` | Invoice and billing records |
| `tblcontact` | Customer enquiries |
| `tblpage` | Editable page and contact information |

## Application Workflow

1. Customers create an account or log in.
2. Customers explore the available beauty services.
3. Customers submit appointment requests.
4. Administrators review appointment requests.
5. Administrators approve or reject appointments.
6. Customer and appointment records can be managed through the admin panel.
7. Billing records and invoices can be maintained.
8. Administrators can review enquiries and generate business reports.

## Project Purpose

This project demonstrates the development of a database-driven web application for a beauty parlour. It brings customer-facing appointment functionality and administrative management features together in one system.

## Important Notes

- This repository contains a PHP/MySQL application intended for local development and demonstration.
- The project requires a configured PHP server and MySQL database.
- The application uses the database credentials configured in its PHP connection files.
- The supplied database includes sample records.
- The project should be security-reviewed before deployment in a production environment. In particular, the original source uses MD5 password hashing and should not be treated as production-ready authentication.


---

*Beauty Parlour Management System — PHP, MySQL and Bootstrap.*
