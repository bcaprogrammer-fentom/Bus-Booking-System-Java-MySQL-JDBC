# 🚌 Bus-Booking-System-Java-MySQL-JDBC


A desktop-based bus ticket booking application built using **Java Swing** and **MySQL**. This GUI app allows users to select source/destination, choose date and time, input passenger details, and book tickets. Bookings are saved in a local MySQL database and also exported to a text file.

---

## 📋 Features

- User-friendly GUI built with **Java Swing**
- Date picker using **JCalendar**
- Select source and destination cities
- Choose time and travel date
- Calculates and displays payable amount
- Booking history stored in `BusBooking.txt`
- MySQL database integration for storing bookings

---

## 💻 Technologies Used

| Tech            | Version     |
|-----------------|-------------|
| Java            | 8+          |
| Java Swing      | GUI Toolkit |
| MySQL           | 5.7+        |
| JDBC Driver     | MySQL JDBC Connector |
| JCalendar       | for date selection |
| NetBeans / VS Code | Supported IDEs |

---

## 🗃️ Database Setup

1. **Create the Database**

```sql
CREATE DATABASE busbooking;
Create the Table


USE busbooking;

CREATE TABLE book (
    ID INT AUTO_INCREMENT PRIMARY KEY,
    User_Name VARCHAR(100),
    S_Source VARCHAR(100),
    destination VARCHAR(100),
    No_of_passenger INT,
    Time VARCHAR(20),
    DOJ DATE,
    Paid_amt INT
);

Update JDBC Credentials in Java Code
Ensure your Java file has the correct DB credentials:

c = DriverManager.getConnection("jdbc:mysql://localhost/busbooking", "root", "your_mysql_password");

📂 Project Structure
bash

BusBookingSystem-Java/
│
├── booking.java             # Main Java Swing application
├── BusBooking.txt           # Output file containing booking summaries
├── README.md                # Project description
└── /lib                     # Include JCalendar JAR and JDBC Connector
📦 Requirements
Java Development Kit (JDK) 8 or higher

MySQL Server

MySQL JDBC Driver (mysql-connector-java-x.x.xx.jar)

JCalendar Library (jcalendar-x.x.jar)

IDE like NetBeans or Visual Studio Code

▶️ How to Run
Clone this repository:

bash

git clone https://github.com/your-username/BusBookingSystem-Java.git
cd BusBookingSystem-Java

bash

javac -cp "lib/*" -d bin src/booking.java
 java -cp "bin;lib/*" booking
Open the project in your preferred Java IDE (e.g., VS Code or NetBeans).

Add external libraries:

mysql-connector-java-x.x.xx.jar

jcalendar-x.x.jar

Run the booking.java file.

📄 Sample Output

*************************************
Name of User: John Doe
TO: Pune
From: Mumbai
No of Passenger: 2
Time: 8:00 am
Date of Journey: 2025-07-20
Payble Amount: 400
*************************************
📁 Text File Output
Bookings are also saved to BusBooking.txt in the project directory.

🛠️ Future Enhancements
Admin panel for managing bookings

Email or SMS confirmations

Online payment integration

More advanced seat selection system

🙌 Contribution
Feel free to fork the project, raise issues, or submit pull requests. All contributions are welcome!

📜 License
This project is licensed under the MIT License.


