# UMBC Retriever Essentials – Smart Grocery & Food Waste App

This project is a web-based inventory management system developed for the Retriever Essentials program at UMBC. It aims to support food inventory tracking, expiration alerts, and meal recommendations for students. The system is structured with two primary user roles: administrators, who manage inventory, and students, who monitor and control their inventory usage.

## Table of Contents
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Usage](#usage)
- [User Roles](#user-roles)
- [API Endpoints](#api-endpoints)
- [Screenshots](#screenshots)
- [Future Enhancements](#future-enhancements)

---

## Features

- **Inventory Management**: Track items with categories, quantities, and expiration dates.
- **Expiration Alerts**: Notify users about items that are close to expiration.
- **AJAX Integration**: Real-time updates for quantity adjustments and inventory filtering without reloading the page.
- **Barcode or Manual Entry**: Admins can add or update items in the inventory either by scanning a barcode or using manual entry.
- **Role-Based Access**: 
  - **Admin**: Full access to manage the inventory, including adding, updating, and deleting items.
  - **Student**: Limited access to view inventory items and track their usage.

---

## Tech Stack

- **Frontend**: HTML, CSS, JavaScript, AJAX
- **Backend**: Django, Python
- **Database**: SQLite (for structured data), MongoDB (for unstructured or scalable data, such as logs or history)
- **Environment**: Virtual environment (recommended)

---

## Project Structure

```plaintext
retriever_essentials_umbc/
├── client/
│   ├── views.py
│   ├── urls.py
│   └── templates/
│       └── client/
│           ├── admin_dashboard.html
│           ├── student_dashboard.html
│           └── client_page.html
├── inventory/
│   ├── views.py
│   ├── urls.py
│   └── templates/
│       └── inventory/
│           ├── inventory_list.html
│           └── update_inventory.html
├── retriever_essentials_umbc/
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py
└── templates/

