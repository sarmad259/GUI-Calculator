# GUI Calculator (C# WinForms + MySQL)

A **simple yet functional calculator** built using **C# Windows Forms (WinForms)**. It supports **basic arithmetic operations** and stores calculation results in a **MySQL database** in the background.

## 🔹 Features
✅ Perform **basic arithmetic operations** (+, -, *, /)  
✅ Stores results in a **MySQL database** automatically  
✅ User-friendly **Windows GUI interface**  
✅ **History tracking** (fetch past calculations from the database)  
✅ Developed in **C# (.NET Framework) + MySQL**  

## 🔹 Installation & Setup
### **1️⃣ Install Required Software**
- Install **Visual Studio** ([Download Here](https://visualstudio.microsoft.com/))
- Install **MySQL Server** ([Download Here](https://dev.mysql.com/downloads/))
- Install **MySQL Connector for .NET** ([Download Here](https://dev.mysql.com/downloads/connector/net/))

### **2️⃣ Clone the Repository**
```bash
 git clone https://github.com/sarmad259/GUI-Calculator.git
 cd GUI-Calculator
```

### **3️⃣ Configure the MySQL Database**
1. Open MySQL and create a new database:
```sql
CREATE DATABASE CalculatorDB;
```
2. Use the following SQL to create a **table** for storing results:
```sql
CREATE TABLE calculations (
    id INT AUTO_INCREMENT PRIMARY KEY,
    expression VARCHAR(255) NOT NULL,
    result DOUBLE NOT NULL,
    timestamp TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```
3. Update **database connection string** in `Form1.cs`:
```csharp
string connectionString = "server=localhost;database=CalculatorDB;user=root;password=yourpassword;";
```

### **4️⃣ Run the Application**
1. Open `GUI-Calculator.sln` in **Visual Studio**.
2. Build & Run the project (`F5`).
3. Perform calculations & check the MySQL database for stored results!


## 🔹 Future Improvements
🔹 Add support for **scientific functions (sin, cos, log, etc.)**  
🔹 Implement a **dark mode UI**  
🔹 Allow users to **export history as a CSV file**  

