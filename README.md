

# 🧾 Customer Management System (Java Swing + MySQL)

A desktop-based application built using Java Swing and AWT for managing customer information efficiently. The system supports full CRUD functionality, user authentication, and an interactive graphical interface for data entry, display, and updates.

---

## 📌 Features

- **User-Friendly Data Entry**
  - Forms for customer details: Name, Amount Paid, Address, and Company Name.
  - Real-time input validation.

- **Data Management**
  - Create, Read, Update, and Delete (CRUD) customer records.
  - Display data in a searchable and sortable table.

- **User Experience Enhancements**
  - Dialogs for alerts and confirmations.
  - Keyboard shortcuts for faster navigation.

- **Security**
  - Optional user authentication (Signup/Login).

---

## 🛠️ Technologies Used

- Java (Core)
- Swing & AWT (GUI)
- JDBC (Database Connectivity)
- MySQL (Database)

---

## 🧱 Application Structure

### GUI Components
- Signup Form
- Login Form
- Customer Dashboard
- Show Table with sorting & filtering

### MVC Design Pattern
- **Model** – `Customer`, `CustomerDAO` (Database operations)
- **View** – Java Swing Forms
- **Controller** – Event handling and GUI-DB interaction logic

### Other Design Patterns
- **Observer** – Updates UI when data changes.
- **Singleton** – For managing the database connection.

---

## 🗃️ Database Schema

### `Customer_info` Table
| Column | Type | Description |
|--------|------|-------------|
| ID     | INT (PK) | Unique customer ID |
| Name   | VARCHAR | Customer's name |
| Email  | VARCHAR | Email address |

### `Customer_details` Table
| Column        | Type | Description |
|---------------|------|-------------|
| cst_id        | INT (FK) | Links to Customer_info.ID |
| cst_name      | VARCHAR  | Customer's name |
| cst_payment   | DECIMAL  | Payment amount |
| cst_address   | VARCHAR  | Customer address |
| Company       | VARCHAR  | Company name |

> Relationship: One-to-many between `Customer_info` and `Customer_details`.

---

## 🚀 Navigation Flow

1. **Main Window:** Signup form appears.
2. **Login Window:** After signup/login, user accesses dashboard.
3. **Dashboard:** Add/Update/Delete customers, and display data in a table.
4. **Table View:** Sort and view all customers. Options to Logout or Load More.

---

## 🧩 How to Run the Project

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/customer-management-system.git
   cd customer-management-system
````

2. **Setup MySQL Database**

   * Create the database and tables as described in the schema section.
   * Update DB credentials in your Java code (usually in `DBConnection` or `CustomerDAO` class).

3. **Compile and Run**

   * Open the project in any Java IDE (like IntelliJ or NetBeans).
   * Compile and run the `CustomerManagementApp` main class.

---

## 📈 Future Enhancements

* Export reports to PDF/Excel
* Multi-user support
* Admin panel with analytics
* Dark mode UI

---

## 🤝 Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

---