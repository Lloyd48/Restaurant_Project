# 🍽️ Restaurant Management System

A desktop-based restaurant automation application built with **Python**, **CustomTkinter**, and **MySQL**. The system is designed to streamline restaurant operations, featuring secure user authentication, inventory tracking, order management, dynamic table statuses, and comprehensive audit logs.

---

## 🚀 Features

- **🔐 Secure Authentication**: User login and registration powered by **SHA-256** password hashing.
- **📦 Inventory & Menu Management**: Full CRUD operations for products (food & beverages) displayed via `ttk.Treeview`.
- **🛎️ Order & Table Automation**:
  - Live table status tracking (displays tables as `Full` or `Empty`).
  - Automated stock reduction upon order placement with transaction rollback safety.
  - Multi-item batch ordering support.
- **💰 Financial Tracking**: Dynamic total revenue calculation directly integrated from database queries.
- **📜 Audit & Activity Logging**: Logs personnel actions (logins, registrations, product/order updates) with date-based filtering.
- **🎨 Modern User Interface**: Responsive dark-themed desktop GUI crafted with CustomTkinter.

---

## 🛠️ Tech Stack

- **Language**: Python 3.x
- **GUI Framework**: [CustomTkinter](https://github.com/TomSchimansky/CustomTkinter), Tkinter (`ttk.Treeview`)
- **Database**: MySQL Server
- **Security**: Python `hashlib` (SHA-256)
- **Environment Management**: `python-dotenv`

---

## 📋 Database Schema

The database consists of four primary relational tables:

- **`users`**: Manages accounts (`username`, `password`, `phone`, `email`).
- **`products`**: Stores menu items (`product_id`, `product_name`, `product_price`, `product_stock`, `category`).
- **`orders`**: Records active customer orders (`order_id`, `product_name`, `product_quantity`, `drink_name`, `drink_quantity`, `total_price`, `table_number`).
- **`actions`**: Tracks system activities for auditing (`id`, `employee`, `action`, `action_time`).

---

## ⚙️ Installation & Setup

### 1. Clone the Repository
```bash
git clone [https://github.com/your-username/your-repository-name.git](https://github.com/your-username/your-repository-name.git)
cd your-repository-name
Install Dependencies:
pip install customtkinter mysql-connector-python python-dotenv
Configure Database Credentials:
DB_PASSWORD=your_mysql_root_password
Run Application:
python main.py
License
