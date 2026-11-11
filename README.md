# ChaJoy – Online Beverage Ordering System

## Project Overview

ChaJoy is a web-based online beverage ordering system developed as part of a university Web Technologies project. The platform provides a convenient way for customers to explore beverages, manage shopping carts, place orders, and track deliveries.

The system incorporates three user roles: Customer, Admin, and Delivery Personnel. Each role has a dedicated interface and specific functionalities to support the overall ordering and delivery process.

The project follows a simple Model-View-Controller (MVC) architecture using PHP and MySQL, with AJAX and JSON for asynchronous operations.

## Technologies Used

- **Frontend:** HTML5, CSS3, JavaScript
- **Backend:** PHP
- **Database:** MySQL
- **Asynchronous Communication:** AJAX and JSON
- **Architecture:** Model-View-Controller (MVC)
- **Development Environment:** XAMPP / WAMP

## Key Features

### Customer Module
- User registration and login with server-side validation.
- Browse beverages by category.
- Search and filter beverages using AJAX.
- View beverage details and availability.
- Add beverages to the shopping cart.
- Update quantities and remove cart items.
- Place orders with delivery information.
- Select Cash on Delivery (COD) or Online as the payment method.
- Track order status.
- View order history.
- Update personal profiles and change passwords.

### Admin Module
- Admin dashboard with order and business statistics.
- Manage beverages (Add, View, Update, and Delete).
- Manage beverage categories.
- View and manage customer information.
- Manage delivery personnel.
- View and process customer orders.
- Update order statuses using AJAX.
- Assign delivery personnel to orders.

### Delivery Personnel Module
- Dedicated delivery dashboard.
- View assigned orders.
- Access order and customer delivery information.
- Update delivery status.
- Mark orders as picked up or delivered using AJAX.

## Project Architecture

ChaJoy follows the Model-View-Controller (MVC) architectural pattern to organize application logic and maintain a structured codebase.

- **Model:** Handles database operations and data management.
- **View:** Manages the user interface and presentation.
- **Controller:** Processes user requests and coordinates application logic.

All application requests are routed through a central entry point (`index.php`).

## Project Directory Structure

```text
ChaJoy/
│
├── config/
│   ├── config.php
│   └── database.php
│
├── controllers/
│   ├── AdminController.php
│   ├── AuthController.php
│   ├── BeverageController.php
│   ├── CartController.php
│   ├── CustomerController.php
│   ├── DeliveryController.php
│   └── OrderController.php
│
├── database/
│   └── chajoy_db.sql
│
├── includes/
│   └── functions.php
│
├── models/
│   ├── Beverage.php
│   ├── Cart.php
│   ├── Category.php
│   ├── Delivery.php
│   ├── Order.php
│   ├── Payment.php
│   └── User.php
│
├── public/
│   ├── css/
│   ├── js/
│   └── images/
│
├── views/
│   ├── admin/
│   ├── auth/
│   ├── customer/
│   ├── delivery/
│   └── layouts/
│
├── index.php
└── README.md
```

## Installation and Setup

Follow these steps to run the project locally.

### Prerequisites

- XAMPP or WAMP
- PHP
- MySQL
- Web browser

### Step 1: Clone the Repository

Open Git Bash and execute:

```bash
git clone https://github.com/SadiaAfrin-hub/ChaJoy-Online_Beverage_Ordering_System.git
```

### Step 2: Move the Project Folder

Copy the downloaded `ChaJoy` folder into the XAMPP `htdocs` directory.

```text
C:\xampp\htdocs\ChaJoy
```

### Step 3: Start Apache and MySQL

1. Open the XAMPP Control Panel.
2. Start Apache.
3. Start MySQL.

### Step 4: Create the Database

1. Open phpMyAdmin:

   `http://localhost/phpmyadmin`

2. Create a new database named:

   `ChaJoy`

3. Select the newly created database.
4. Open the Import tab.
5. Choose `database/chajoy_db.sql` from the project directory.
6. Click Import.

The SQL file creates the required tables and inserts sample data, including user accounts, beverage categories, and beverages.

### Step 5: Configure Database Connection

Open:

`config/database.php`

Ensure the database configuration matches your local MySQL settings.

Default project configuration:

```php
$db_host = "localhost";
$db_user = "root";
$db_pass = "";
$db_name = "ChaJoy";
$db_port = 3307;
```

Update these values if your local MySQL configuration is different.

### Step 6: Run the Application

Open your browser and visit:

`http://localhost/ChaJoy/`

The ChaJoy application should now be accessible locally.

## Sample Login Credentials

The database includes sample accounts for testing different user roles.

| Role | Email |
|---|---|
| Admin | admin@chajoy.com |
| Delivery Personnel | delivery@chajoy.com |
| Customer | customer@chajoy.com |
| Customer | test@chajoy.com |

**Default password:** `password123`

These are demonstration credentials intended for local testing only.

## Security and Implementation

The project incorporates several fundamental security and development practices:

- Password hashing and verification using PHP's `password_hash()` and `password_verify()`.
- Server-side form validation.
- Prepared SQL statements to reduce SQL injection risks.
- Output sanitization using `htmlspecialchars()`.
- Session-based authentication.
- Role-based access control.
- AJAX requests with JSON responses.
- Database operations using MySQLi.

## Learning Outcomes

This project demonstrates practical implementation of:

- PHP conditional statements, loops, and string manipulation.
- Form handling and server-side validation.
- Session management and authentication.
- MySQL database connectivity and CRUD operations.
- MVC-based application organization.
- AJAX and JSON communication.
- Role-based application functionality.
- Dynamic content management.

## Project Information

**Project Name:** ChaJoy – Online Beverage Ordering System

**Project Type:** Academic Web Technologies Project

**Backend:** PHP

**Database:** MySQL

**Architecture:** MVC

**Repository:** [ChaJoy – GitHub](https://github.com/SadiaAfrin-hub/ChaJoy-Online_Beverage_Ordering_System)

---

Developed as an academic project to demonstrate practical web application development using PHP, MySQL, JavaScript, and modern web technologies.
