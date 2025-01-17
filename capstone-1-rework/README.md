# **Accounting Ledger Application - Version 2.0**

## **Project Overview**

This Java-based application simulates a financial ledger system, allowing users to manage transactions, view reports, and keep track of their financial activities. The application is structured using multiple packages, each focused on specific functionality, ensuring the code is modular, scalable, and easy to maintain.

In **Version 2.0**, several improvements are made to enhance the functionality, user experience, and code quality. These improvements include refined user interfaces, enhanced reporting features, and performance optimizations.

## **Project Structure**

### **Packages and Classes Overview**

- **`ledger` package**: Contains the main entry point for the application.
    - **`LedgerApp`**: The main class that runs the application, handles user input, and manages the flow of the program.

- **`models` package**: Contains the core data structure classes.
    - **`Transaction`**: Represents a financial transaction, including attributes like date, description, vendor, and amount. It also provides methods for formatting and validating transaction data.

- **`services` package**: Contains services for handling specific application logic and functionalities.
    - **`DateTimeHandlerService`**: Provides utilities for working with dates and times, such as formatting and parsing.
    - **`FileHandlerService`**: Responsible for reading from and writing to files (e.g., `transactions.csv`).
    - **`PrintScreenService`**: Manages output to the user interface, including displaying reports and transaction data.
    - **`TransactionProcessingService`**: Handles the core logic for processing and managing transactions, including adding new transactions, filtering, and generating reports.

## **New Features in Version 2.0**

1. **Enhanced User Interface**:
    - Refined menu options for better navigation.
    - Improved error handling and validation messages for a smoother user experience.

2. **Improved Reporting**:
    - Additional filtering options for transaction reports (by date range, by category).
    - Enhanced report formatting for better readability.

3. **File Management**:
    - Automatic backup of transactions at regular intervals.
    - Improved CSV file handling and validation to prevent data loss.

4. **Performance Optimizations**:
    - Refactored code for faster reading/writing to CSV files.
    - Optimized transaction filtering and sorting for faster response times.

## **Features**

### 1. **Home Screen**:
- **Add Deposit**: Record deposits into the ledger.
- **Make Payment**: Record payments and expenses.
- **View Ledger**: View all transactions with filtering options.
- **Exit**: Close the application safely.

### 2. **Ledger Screen**:
- **View All Transactions**: See the complete transaction history.
- **View Only Deposits**: Filter and view only deposit transactions.
- **View Only Payments**: Filter and view only payment transactions.
- **Access Reports**: Generate transaction reports based on various time periods.

### 3. **Reports**:
- **Month to Date**: View transactions made within the current month.
- **Previous Month**: View transactions from the previous month.
- **Year to Date**: View transactions from the start of the current year.
- **Previous Year**: View transactions from the previous year.
- **Search by Vendor**: Filter transactions by vendor name.
- **Date Range Filter**: Custom filter for transactions between any two dates.
- **Category Filter**: Filter by transaction category (e.g., Rent, Supplies, etc.).

## **Components**

### **LedgerApp Class** (`ledger` package)
- The main entry point of the application that interacts with users via a text-based interface. It calls services like `TransactionProcessingService` to handle user input, and outputs results using `PrintScreenService`.

### **Transaction Class** (`models` package)
- Represents a single financial transaction, with attributes such as date, description, vendor, and amount. This class also provides methods to format transaction data and validate input.

### **DateTimeHandlerService Class** (`services` package)
- Handles date and time formatting, parsing, and validation. Ensures consistent handling of time-related data across the application.

### **FileHandlerService Class** (`services` package)
- Responsible for managing file operations, particularly reading and writing the `transactions.csv` file. This ensures that data is saved persistently between sessions.

### **PrintScreenService Class** (`services` package)
- Provides methods for outputting formatted transaction reports and user-friendly messages on the console.

### **TransactionProcessingService Class** (`services` package)
- The core service for processing transactions. This class adds, updates, and filters transactions based on various criteria. It also manages the generation of reports for the user.

## **Getting Started**

### **Prerequisites**
- **Java Development Kit (JDK)**: Ensure that JDK 11 or higher is installed on your machine.
- **IDE or Text Editor**: You can use IntelliJ IDEA, Eclipse, or any Java-supported IDE for development.

### **Installation**
1. **Clone or Download the Repository**:
    - Clone the project using Git or download the ZIP file.
    - ```bash
     git clone https://github.com/tiermcg/capstone-1-revamp-
     ```
2. **Open the Project in Your IDE**.
3. **Create or Verify the `transactions.csv` File**:
    - Ensure the `transactions.csv` file is in the root directory. It will be auto-generated during the first run if not present.

### **Running the Application**
1. **Compile the Java Files**:
    - Use your IDE's build tools or the command line to compile all `.java` files.
    - Example: `javac Main.java LedgerApp.java Transaction.java DateTimeHandlerService.java FileHandlerService.java PrintScreenService.java TransactionProcessingService.java`

2. **Run the LedgerApp Class**:
    - Execute the `LedgerApp` class to start the application.
    - Example: `java LedgerApp`

3. **Follow the Instructions**:
    - The program will display a text-based menu where you can choose options to add transactions, generate reports, or view your ledger.

## **Usage**
- **Menu Navigation**: Choose options from the home screen to add deposits, make payments, or view transaction reports.
- **Input Validation**: The application ensures that only valid input is accepted, providing error messages when necessary.
- **Error Handling**: The system will guide you with clear error messages in case of invalid input or issues during the transaction process.

## **License**
This project is licensed under the MIT License.
