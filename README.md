# User Registration System

## Project Overview

This is a **User Registration System** built using **PHP** and **MySQL**. The system allows users to register with their **name** and **email**. The system validates the input data, checks for duplicates, and stores the user information in a **MySQL** database. The registration process is user-friendly and can be easily integrated into any web application requiring a user registration feature.

## Features

- **User Registration:**
  - Allows users to register by entering their name and email address.
  - Registration is stored in the **MySQL** database.
- **Input Validation:**
  - Checks if the name and email fields are not empty.
  - Validates that the email format is correct using regular expressions.
  - Ensures that the email entered is unique (i.e., not already in the database).
- **Error Handling:**
  - Displays error messages for missing or incorrect inputs (e.g., missing name or invalid email format).
  - Checks for duplicate email entries and prevents multiple registrations with the same email.
- **Responsive Design:**
  - The registration form uses **Bootstrap** to ensure a clean and responsive layout that works well on both desktop and mobile devices.
- **Success and Error Notifications:**
  - After a successful registration, a confirmation message is displayed.
  - Error messages are shown when validation fails or if there are issues during database operations.
  
## Technologies Used

- **PHP**: A server-side scripting language used to process form submissions and interact with the database.
- **MySQL**: A relational database management system used to store user information (name and email).
- **Bootstrap**: A front-end framework used to design a responsive user interface.
- **JavaScript**: Client-side scripting for additional form validation before submission.

## Installation Instructions

### Prerequisites

To run this project locally, make sure you have the following software installed:

- **XAMPP** or **WAMP** (or any PHP server environment).
- **PHP** version 7.0 or higher.
- **MySQL** (usually included with XAMPP/WAMP).
- **phpMyAdmin** (for managing MySQL databases).

### Step 1: Set Up XAMPP/WAMP

1. Download and install **[XAMPP](https://www.apachefriends.org/index.html)** or **[WAMP](https://www.wampserver.com/en/)** on your computer.
2. Open the XAMPP/WAMP control panel and start the **Apache** and **MySQL** services.
   - Apache (for running PHP).
   - MySQL (for managing the database).

### Step 2: Create Database and Table

1. Open **phpMyAdmin** in your browser by going to `http://localhost/phpmyadmin/`.
2. Create a new database called `login` (or use a different name if desired).
3. Create a new table called `users` with the following structure:

   ```sql
   CREATE TABLE IF NOT EXISTS users (
       id INT AUTO_INCREMENT PRIMARY KEY,
       name VARCHAR(255) NOT NULL,
       email VARCHAR(255) NOT NULL UNIQUE
   );
