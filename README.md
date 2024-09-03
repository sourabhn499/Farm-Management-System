# 🌾 Farm Management System

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Flask](https://img.shields.io/badge/Flask-1.1.2-green)
![SQLite](https://img.shields.io/badge/SQLite-3.32.3-lightgrey)
![HTML](https://img.shields.io/badge/HTML-5-orange)
![CSS](https://img.shields.io/badge/CSS-3-blue)
![SQL](https://img.shields.io/badge/SQL-MySQL-yellow)

## Overview

The Farm Management System is a web-based platform designed to facilitate the buying and selling of agricultural products. It enables farmers to sell their products online and allows farmers to purchase tools and seeds directly from sellers. Additionally, farmers can manage their profiles, register, edit, and delete data. Buyers can purchase various agricultural products online and send purchase requests to check the quality of the agro products through emails.

## 🌟 Features

### Farmer Features
- **🔐 User Registration and Authentication**: Farmers can register and login to the system using their credentials.
- **📄 Profile Management**: Farmers can view, edit, and delete their profiles.
- **🌾 Sell Products**: Farmers can list their agricultural products for sale.
- **🛒 Purchase Tools and Seeds**: Farmers can purchase tools and seeds directly from sellers.

### Buyer Features
- **🛒 Browse Products**: Buyers can browse through the list of available agricultural products.
- **🔎 Search and Filter**: Buyers can search for products based on categories, names, or keywords.
- **💌 Send Purchase Requests**: Buyers can send purchase requests to check the quality of the agro products via email.

## 🛠️ Technologies Used

The Farm Management System is developed using the following technologies:

- <span style="color:orange;">**HTML**</span>: For creating the structure and layout of web pages.
- <span style="color:blue;">**CSS**</span>: For styling the web pages and enhancing the user interface.
- <span style="color:green;">**Flask**</span>: A micro web framework for Python used for server-side development and handling backend operations.
- <span style="color:purple;">**SQLite**</span>: A lightweight relational database management system used for storing and managing farm data.
- <span style="color:yellow;">**SQL**</span>: For managing and querying the database.

## 🛠️ Installation

To run the Farm Management System on your local machine, follow these steps:

1. **Clone the repository**
    ```bash
    git clone https://github.com/yourusername/farm-management-system.git
    cd farm-management-system
    ```

2. **Install dependencies**
    ```bash
    pip install -r requirements.txt
    ```

3. **Set up the database**
    - Import the provided SQL dump file (`farmers.sql`) into your MySQL/MariaDB database.
    - Use a database management tool like phpMyAdmin or the MySQL command line.

    ```sql
    -- Import SQL dump
    source /path/to/farmers.sql;
    ```

4. **Configure the application**
    - Update the configuration file `config.py` with your database connection details.

5. **Run the application**
    ```bash
    flask run
    ```

6. **Access the application**
    - Open your web browser and navigate to `http://localhost:5000`.

## ⚙️ System Features

The key features of the Farm Management System include:

- **🔐 User Registration and Authentication**: Farmers and buyers can register and login to the system using their credentials.
- **📄 Profile Management**: Farmers can view, edit, and delete their profiles.
- **🌾 Sell Products**: Farmers can list their agricultural products for sale.
- **🛒 Browse and Purchase Products**: Buyers can browse through the collection of agricultural products, search and filter based on categories, names, or keywords, and purchase products.
- **💌 Send Purchase Requests**: Buyers can send purchase requests to check the quality of the agro products through emails.

## 🏛️ System Architecture

The Farm Management System follows a client-server architecture where the client interacts with the server through a web interface. The server-side logic is implemented using Flask, which handles requests from clients, processes data, and communicates with the database.

## 💻 User Interfaces

The user interfaces are designed to be intuitive and user-friendly. HTML and CSS are used to create visually appealing web pages with responsive design for compatibility across devices.

- **🏠 Home Page**: Displays featured products, categories, and navigation links.
- **📄 Profile Page**: Allows farmers to manage their profile information.
- **🛒 Product Listing Page**: Displays a list of products with search and filter options.
- **🌾 Sell Product Page**: Allows farmers to list their products for sale.
- **💌 Purchase Request Page**: Allows buyers to send purchase requests.

## 🗄️ Database Schema

The Farm Management System employs a relational database model using MySQL/MariaDB to manage various entities efficiently. The database schema includes tables for the following entities:

### `addagroproducts`
- **username**: varchar(50), NOT NULL
- **email**: varchar(50), NOT NULL
- **pid**: int(11), NOT NULL, PRIMARY KEY
- **productname**: varchar(100), NOT NULL
- **productdesc**: text, NOT NULL
- **price**: int(100), NOT NULL

### `farming`
- **fid**: int(11), NOT NULL, PRIMARY KEY
- **farmingtype**: varchar(200), NOT NULL

### `register`
- **rid**: int(11), NOT NULL, PRIMARY KEY
- **farmername**: varchar(50), NOT NULL
- **adharnumber**: varchar(20), NOT NULL
- **age**: int(100), NOT NULL
- **gender**: varchar(50), NOT NULL
- **phonenumber**: varchar(12), NOT NULL
- **address**: varchar(50), NOT NULL
- **farming**: varchar(50), NOT NULL

### `trig`
- **id**: int(11), NOT NULL, PRIMARY KEY
- **fid**: varchar(50), NOT NULL
- **action**: varchar(50), NOT NULL
- **timestamp**: datetime, NOT NULL

### `user`
- **id**: int(11), NOT NULL, PRIMARY KEY
- **username**: varchar(50), NOT NULL
- **email**: varchar(50), NOT NULL
- **password**: varchar(500), NOT NULL

---

Thank you for using the Farm Management System! We hope it helps streamline your farming operations and improve your agricultural business.
