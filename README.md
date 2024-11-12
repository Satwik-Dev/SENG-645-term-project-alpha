UMBC Retriever Essentials – Smart Grocery & Food Waste App
This project is a web-based inventory management system developed for the Retriever Essentials program at UMBC. It aims to support food inventory tracking, expiration alerts, and meal recommendations for students. The system is structured with two primary user roles: administrators, who manage inventory, and students, who monitor and control their inventory usage.
Table of Contents
•	Features
•	Tech Stack
•	Project Structure
•	Installation
•	Usage
•	User Roles
•	API Endpoints
•	Screenshots
•	Future Enhancements
________________________________________
Features
•	Inventory Management: Track items with categories, quantities, and expiration dates.
•	Expiration Alerts: Notify users about items that are close to expiration.
•	AJAX Integration: Real-time updates for quantity adjustments and inventory filtering without reloading the page.
•	Barcode or Manual Entry: Admins can add or update items in the inventory either by scanning a barcode or using manual entry.
•	Role-Based Access:
o	Admin: Full access to manage the inventory, including adding, updating, and deleting items.
o	Student: Limited access to view inventory items and track their usage.
________________________________________
Tech Stack
•	Frontend: HTML, CSS, JavaScript, AJAX
•	Backend: Django, Python
•	Database: SQLite (for structured data), MongoDB (for unstructured or scalable data, such as logs or history)
•	Environment: Virtual environment (recommended)
________________________________________
Project Structure
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
    ├── login.html
    ├── password_reset_form.html
    ├── password_reset_done.html
    ├── password_reset_confirm.html
    └── password_reset_complete.html
________________________________________
Installation
1.	Clone the Repository:
git clone https://github.com/yourusername/retriever_essentials.git
cd retriever_essentials
2.	Create and Activate a Virtual Environment:
python -m venv venv
source venv/bin/activate  # On Windows, use venv\Scripts\activate
3.	Install Dependencies:
pip install -r requirements.txt
4.	Configure the Database:
o	By default, the project uses SQLite for structured data and MongoDB for unstructured data.
o	Make sure MongoDB is installed and running on your system if you plan to use it for logs or other scalable data.
5.	Apply Migrations:
python manage.py makemigrations
python manage.py migrate
6.	Run the Server:
python manage.py runserver
The application will be available at http://127.0.0.1:8000.
________________________________________
Usage
Administrator (Admin) Dashboard
1.	Log in as an admin user.
2.	Access the admin dashboard to add, update, or delete items in the inventory.
3.	Use the Update Quantity feature to adjust quantities in real time.
4.	Use the Barcode or Manual Entry option to add or update items efficiently.
Student Dashboard
1.	Log in as a student user.
2.	View the inventory list categorized by item type and expiry status.
3.	Track inventory usage and receive notifications for items that are close to expiration.
________________________________________
User Roles
•	Admin:
o	Access to inventory management features, including adding, updating, and deleting items.
o	Can update item quantities and use barcode/manual entry for inventory updates.
•	Student:
o	View-only access to inventory with details on item classifications and expiration alerts.
o	Cannot add or modify inventory items.
________________________________________
API Endpoints
The system includes a set of views and AJAX-based interactions for real-time data updates.
Endpoint	Method	Description
/inventory/	GET	Display the inventory list
/inventory/update/<id>/	POST	Update item quantity
/client/	GET	Access client page (Admin only)
/login/	GET	Login page
/logout/	GET	Logout
/password_reset/	GET	Request password reset
/password_reset_confirm/	GET	Confirm password reset
________________________________________
Screenshots
Include screenshots here (for example, inventory_list.html showing the inventory list, and client_page.html for the client page with inventory management options).
________________________________________
Future Enhancements
•	Enhanced Role Management: Implement finer-grained permissions for different types of admin roles.
•	Advanced Analytics: Integrate data analytics to provide insights into food consumption patterns and reduce waste.
•	Real-Time Notifications: Implement email or SMS notifications for items that are about to expire.
•	Machine Learning Integration: Use machine learning to suggest optimal usage and meal plans based on inventory items.
________________________________________
License
This project is licensed under the MIT License. See the LICENSE file for more details.
________________________________________

