from pathlib import Path

# 🎂 Cake Shop Website (PHP + MySQL)

This project is a complete Cake Shop E-Commerce platform built using PHP and MySQL (phpMyAdmin). It features both customer and admin functionalities for managing cake raw materials and orders.

---

## 🖥️ Frontend (User Interface)

### 🔹 Homepage
- Displays featured products, categories, and latest offers.

### 🔹 Categories Page
- Showcases cake raw materials grouped by:
  - Flavors
  - Creams
  - Toppings
  - Tools

### 🔹 Product Page
- Displays:
  - Name
  - Product image
  - Description
  - Price
  - Stock availability

### 🔹 Cart Page
- Allows users to:
  - Add/remove products
  - View total price
  - Proceed to checkout

### 🔹 Login & Registration
- Separate sign-up/login for:
  - Cake Shop Owners
  - Retail Customers

### 🔹 Payment Integration
- Supports:
  - PayPal
  - Razorpay
  - Manual Bank Transfer

---

## 🔧 Backend (Admin Panel & Database)

### 🔹 User Roles
- **Cake Shop Owners**: Get wholesale discounts.
- **Retail Customers**: Pay standard prices.
- **Admin**: Manages products, users, and orders.

### 🔹 Admin Dashboard
- Add/edit/delete products with:
  - Name
  - Description
  - Images
  - Prices
- Manage users and apply discounts to approved shop owners.
- View and process user orders.

---

## 🗃️ Database Structure (MySQL via phpMyAdmin)

### `users` Table
| Field       | Type     | Description                          |
|-------------|----------|--------------------------------------|
| id          | INT      | Primary Key                          |
| name        | VARCHAR  | Full name                            |
| email       | VARCHAR  | Unique email                         |
| password    | VARCHAR  | Hashed password                      |
| role        | ENUM     | 'shop_owner', 'retail'               |

### `products` Table
| Field       | Type     | Description                          |
|-------------|----------|--------------------------------------|
| id          | INT      | Primary Key                          |
| name        | VARCHAR  | Product name                         |
| category    | VARCHAR  | Product category                     |
| description | TEXT     | Product details                      |
| price       | FLOAT    | Price of product                     |
| stock       | INT      | Quantity available                   |
| image       | VARCHAR  | Path to product image                |

### `orders` Table
| Field       | Type     | Description                          |
|-------------|----------|--------------------------------------|
| id          | INT      | Primary Key                          |
| user_id     | INT      | Linked to `users.id`                 |
| total       | FLOAT    | Total order price                    |
| status      | VARCHAR  | Order status (pending/complete)      |

### `cart` Table
| Field       | Type     | Description                          |
|-------------|----------|--------------------------------------|
| id          | INT      | Primary Key                          |
| user_id     | INT      | Linked to `users.id`                 |
| product_id  | INT      | Linked to `products.id`              |
| quantity    | INT      | Product quantity                     |

---

## 🛠️ Tech Stack

- ✅ Frontend: **HTML, CSS, JavaScript**
- ✅ Backend: **PHP**
- ✅ Database: **MySQL (phpMyAdmin)**
- ✅ Security: Password hashing and input validation

---

## 📂 Project Structure

