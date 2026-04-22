# 🎨 Lippan Art Order Management System (ERP Lite)

A desktop-based Order Management System built using **Python (Tkinter)** and **MySQL**, designed for managing Lippan Art business operations like orders, customers, billing, and sales analytics.

---

## 🚀 Features

✨ Customer & Order Management

* Add, update, delete orders
* Auto customer creation using phone number
* Search orders by customer name

💰 Billing System

* Automatic total calculation with discount (%)
* Generate professional bill instantly
* Display subtotal, discount amount, and final total

📊 Data Visualization

* Pie chart for order distribution
* Sales graph (Pending vs Completed)
* Total sales calculator

📅 Smart Enhancements

* Auto date tracking for each order
* Highlight completed orders in green
* Sort orders by total amount

---

## 🖥️ Tech Stack

* **Frontend:** Tkinter (Python GUI)
* **Backend:** MySQL Database
* **Language:** Python
* **Libraries:**

  * `mysql-connector-python`
  * `matplotlib`

---

## 📂 Project Structure

```
Lippan-ERP-Lite/
│
├── main.py
├── database.sql
├── README.md
└── assets (optional screenshots)
```

---

## ⚙️ Installation & Setup

### 1️⃣ Clone the repository

```
git clone https://github.com/Dishankcodes/Lippan-ERP-Lite.git
cd Lippan-ERP-Lite
```

### 2️⃣ Install dependencies

```
pip install mysql-connector-python matplotlib
```

### 3️⃣ Setup MySQL Database

Run this SQL:

```sql
CREATE DATABASE lippan_db;

USE lippan_db;

CREATE TABLE customers (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100),
    phone VARCHAR(15)
);

CREATE TABLE orders (
    id INT AUTO_INCREMENT PRIMARY KEY,
    customer_id INT,
    design VARCHAR(100),
    quantity INT,
    price FLOAT,
    discount FLOAT,
    status VARCHAR(20),
    total FLOAT,
    order_date TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    FOREIGN KEY (customer_id) REFERENCES customers(id)
);
```

---

### 4️⃣ Run the application

```
python main.py
```

---

## 📸 Screenshots (Add Later)

* Dashboard UI
* Order Table
* Generated Bill
* Graphs

---

## 💡 Future Improvements

* Export bill as PDF 🧾
* Login system 🔐
* Inventory management 📦
* Monthly sales reports 📊
* Dark UI theme 🌙

---

## 👨‍💻 Author

**Dishank Prajapati**
📍 Ahmedabad, India

---

## ⭐ Support

If you like this project, give it a ⭐ on GitHub!

---
