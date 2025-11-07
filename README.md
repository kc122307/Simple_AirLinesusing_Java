# ✈️ KC AIRWAYS - Airline Ticket Booking and Management System

This project is a comprehensive desktop application developed in Java for managing flights, passengers, ticket bookings, and cancellations for an airline named **KC AIRWAYS**. It utilizes a **MySQL database** to handle all data persistence.

## ✨ Features

* **Flight Management (`Flights.java`):**
    * Add, Edit, and Delete new flight routes, including flight code, source, destination, date, and number of seats.
    * Display a full list of all available flights in a table view.
* **Passenger Management (`Passengers.java`):**
    * Add, Edit, and Delete passenger details (Name, Nationality, Gender, Passport No., Address, Phone).
    * Automatic generation of a unique Passenger ID.
* **Ticket Booking (`TicketBookings.java`):**
    * Book tickets by selecting a Passenger ID and Flight Code.
    * Automatically fetches passenger details (name, nationality, passport, gender) upon selecting ID.
    * Saves the booking into the `bookingsTbl` in the database.
* **Ticket Cancellation (`Cancellation.java`):**
    * Cancel existing tickets by Ticket ID.
    * Displays the corresponding Flight Code and Date.
    * Records the cancellation in the `cancellationTbl`.
* **Authentication (`Login.java`):**
    * Simple hardcoded administrative login for securing access to the management features.
* **Main Dashboard (`MainForm.java`):**
    * Central hub to navigate between Flights, Passengers, Tickets, and Cancellation modules.

## 🛠️ Technology Stack

* **Language:** Java
* **GUI Framework:** Java Swing / AWT (using NetBeans Form Designer/GUI Builder)
* **Database:** MySQL
* **Database Connectivity:** JDBC (Java Database Connectivity)
* **External Library:** `rs2xml.jar` (Used for easily populating JTables from SQL `ResultSet` in the classes like `Flights.java` and `TicketBookings.java`).

## ⚙️ Setup and Installation

### Prerequisites

1.  **Java Development Kit (JDK):** Ensure you have a suitable version of Java installed.
2.  **NetBeans IDE** (Recommended, as the project appears to be built using its GUI builder).
3.  **MySQL Server:** A running instance of a MySQL database.

### Database Setup

1.  Create a database named `airlinesdb` on your MySQL server.
2.  Create the necessary tables (`FlightTbl`, `PassengersTbl`, `bookingsTbl`, `cancellationTbl`). *Note: You will need to infer the exact schema from the SQL queries in the Java files.*
3.  Ensure your **JDBC Connector** (e.g., `mysql-connector-java-x.x.x.jar`) is in the project libraries.
4.  Update the connection string in all files (`Flights.java`, `TicketBookings.java`, `Passengers.java`, `Cancellation.java`) if your database credentials are not `root` and an empty password:
    ```java
    Con = DriverManager.getConnection("jdbc:mysql://localhost:3306/airlinesdb","root","");
    ```

### Running the Application

1.  Open the project in **NetBeans** (or your preferred IDE).
2.  Run the **`Login.java`** file.
3.  Use the hardcoded credentials found in `Login.java` to access the application:
    * **Username:** `admin`
    * **Password:** `1234`

## 📂 Project Structure Overview

| File | Description |
| :--- | :--- |
| **`Login.java`** | Handles user authentication (admin login). |
| **`MainForm.java`** | The main navigation menu/dashboard. |
| **`Flights.java`** | CRUD operations for managing flight details. |
| **`Passengers.java`** | CRUD operations for managing passenger details. |
| **`TicketBookings.java`**| Interface for creating new ticket bookings. |
| **`Cancellation.java`**| Interface for canceling existing tickets. |
| `Airlines.java` | Main class (currently empty). |

---

Do you want to focus the thumbnail more on the **Java/Code** aspect, or perhaps modify the styling?
