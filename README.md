# Real-Time Chat Web Application

A simple and clean real-time chat application built using **PHP**, **MySQL**, and **JavaScript (with Ajax)**. It allows users to register, log in, and exchange messages instantly without refreshing the page.


🔗 **Live Demo:** [Click here to try!](https://coolchatapp.infinityfreeapp.com/?i=1)  
_(Note: Hosted on a free server; please be patient as it may take a few seconds to load.)_


## Features

- **Real-time messaging**- Send and receive messages without page reload using Ajax.
- **User authentication**- Register and login functionality to keep chats secure.
- **MySQL database**- Stores user credentials and message history.
- **Responsive UI**- Clean and user-friendly chat interface.


## Technologies Used

- **PHP**- Server-side scripting for backend logic.
- **MySQL**- Database to store messages and user information.
- **JavaScript(AJAX)**- For dynamic message sending/receiving without page reloads.
- **HTML & CSS**- For layout and styling.

  
## Project Structure

/Realtime-chat-application
│
├── index.php             Main entry file (homepage or redirect to login)
├── login.php             Login screen for users
├── chat.php              Main chat screen after user logs in
├── users.php             Displays list of users you can chat with
├── header.php            Common top section used on multiple pages
├── style.css             All styling for the pages (colors, layout, etc.)
├── chatapp.sql           The file to create database tables (upload in phpMyAdmin)
├── README.md             (Optional) Project documentation
│
├── /php                  All backend logic (handles requests)
│   ├── config.php        DB connection file (edit with host/user/pass/dbname)
│   ├── signup.php        Handles sign-up form data and saves to DB
│   ├── login.php         Checks login info from the user(Login validation)
│   ├── logout.php        Logs user out (clears session)
│   ├── users.php         Sends list of users to frontend(Fetches all user list)
│   ├── search.php        Finds users by name/email
│   ├── data.php          Stores user session and helper functions
│   ├── get-chat.php      Loads messages between 2 users
│   ├── insert-chat.php   Saves new messages to the database
│
├── /javascript           All frontend logic (JavaScript files)
│   ├── chat.js           Handles sending/receiving messages using AJAX
│   ├── login.js          Validates login form and sends to PHP
│   ├── signup.js         Validates signup form and sends to PHP
│   ├── pass-show-hide.js Show/hide password when clicked
│   └── users.js          Handles live user list and updates



## 📁 Project Structure

Realtime-chat-application/
├── index.php             # Main entry file (homepage or redirect to login)
├── login.php             # Login screen for users
├── chat.php              # Main chat screen after user logs in
├── users.php             # Displays list of users you can chat with
├── header.php            # Common top section used on multiple pages
├── style.css             # Styling for the pages (colors, layout, etc.)
├── chatapp.sql           # SQL file to create database tables (upload in phpMyAdmin)
├── README.md             # (Optional) Project documentation
│
├── php/                  # All backend logic (handles PHP requests)
│   ├── config.php        # DB connection config (edit with host/user/pass/dbname)
│   ├── signup.php        # Handles user registration data
│   ├── login.php         # Checks login info from user (validation)
│   ├── logout.php        # Logs user out (clears session)
│   ├── users.php         # Sends list of users to frontend (chat list)
│   ├── search.php        # Finds users by name/email
│   ├── data.php          # Stores session & helper functions
│   ├── get-chat.php      # Loads messages between users
│   ├── insert-chat.php   # Saves new messages to the database
│
├── javascript/           # All frontend logic (JavaScript files)
│   ├── chat.js           # Handles AJAX for sending/receiving messages
│   ├── login.js          # Validates login form and sends request
│   ├── signup.js         # Validates signup form and sends request
│   ├── pass-show-hide.js # Toggle password visibility
│   └── users.js          # Live user list updates




## Setup Instructions

### 1️⃣ Create a MySQL Database:

- Login to phpMyAdmin.
- Create a new database named: chatapp
- Click Import → Select the file chatapp.sql → Click Go to import tables.

### 2️⃣ Update Database Credentials:

- Open php/config.php

- Update the values as per hosting or local setup:
         $conn = mysqli_connect("localhost", "username", "password", "chatapp");

- Replace "username" and "password" with actual values.  

### 3️⃣ Deploy or Run Locally:

📌 Locally (XAMPP):

- Copy the entire project folder to htdocs inside XAMPP directory.
- Start Apache and MySQL via XAMPP.
      Visit: http://localhost/Realtime-chat-application

🌐 On Hosting (like InfinityFree):

- Create a MySQL database on the hosting panel.
- Import the chatapp.sql into the hosting database via phpMyAdmin.
- Upload all files (unzipped) inside the htdocs or main directory using File Manager.
- Update the config.php with hosting DB credentials.

