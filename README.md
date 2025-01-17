# Bank Management System

This project is a **Bank Management System** implemented in C++. It provides functionalities to manage clients' data, including adding, updating, deleting, and listing client records. The data is stored in a text file (`ClientsRecord.txt`) for persistence. This is the first version of the system, and a second version with additional features, titled **Bank Extension**, is planned.

---

## Features

1. **List Clients:** Display all clients with their details, including account number, name, balance, etc.
2. **Add New Client:** Add a new client to the system by providing account number, PIN code, name, phone number, and balance.
3. **Update Client Info:** Update existing client information such as name, phone number, or balance.
4. **Delete Client:** Remove a client from the system after confirmation.
5. **Find Client:** Search for a client by their account number and display their details.
6. **Persistent Storage:** Client data is saved and loaded from `ClientsRecord.txt`.

---

## File Structure

- **`Bank_Project.cpp`:** Main source code containing all the program logic.
- **`ClientsRecord.txt`:** File where client data is stored in the format:
  ```
  AccountNumber#//#PinCode#//#Name#//#Phone#//#Balance
  ```
- **`.gitignore`:** Standard Git ignore file.
- **`README.md`:** Project documentation (this file).
- **`Bank_Project.sln`:** Solution file for Visual Studio.

---

## How It Works

### Main Menu

The application starts with a main menu offering the following options:

1. Show Client List
2. Add New Client
3. Delete Client
4. Update Client Info
5. Find Client
6. Exit

### Client Data Structure

Each client is represented using the `stClient` structure:

```cpp
struct stClient {
    string AccountNumber;
    string PinCode;
    string Name;
    string Phone;
    double AccountBalance;
    bool MarkForDelete;
};
```

### Core Functions

#### Data Manipulation:
- `AddNewClient()`
- `DeleteClientByAccountNumber()`
- `UpdateClientByAccountNumber()`

#### File Handling:
- `LoadDataFromFileToVector()`
- `SaveClientDataToFile()`
- `AddDataLineToFile()`

#### Utility Functions:
- `SpiltEachWord()`: Splits a string by a delimiter.
- `ConvertLineToRecord()`: Converts a line from the file into an `stClient` object.
- `ConvertRecordToLine()`: Converts an `stClient` object into a formatted string.

---

## How to Run

1. Clone the repository or download the source code.
2. Open `Bank_Project.sln` in Visual Studio.
3. Build and run the project.
4. Use the main menu to navigate through the application.

### Example Usage

#### Adding a New Client:
1. Select **Add New Client** from the menu.
2. Enter the following details:
   - Account Number
   - PIN Code
   - Name
   - Phone Number
   - Account Balance
3. The client will be added to `ClientsRecord.txt`.

#### Listing Clients:
1. Select **Show Client List** from the menu.
2. View all clients in a table format.

---

## Data Format

The client data is stored in `ClientsRecord.txt` with the following format:

```
AccountNumber#//#PinCode#//#Name#//#Phone#//#Balance
```

### Example:

```
123456#//#1234#//#John Doe#//#1234567890#//#1500.75
234567#//#5678#//#Jane Smith#//#9876543210#//#2500.50
```

---

## Dependencies

- **C++ Standard Library**:
  - `<iostream>`: For input/output operations.
  - `<vector>`: To store and manage the list of clients.
  - `<string>`: For string manipulation.
  - `<fstream>`: For file handling.
  - `<iomanip>`: For formatted output.

---

## Future Enhancements

1. Implement user authentication for better security.
2. Add support for multiple users with different roles (e.g., admin, teller).
3. Enhance the user interface with a graphical UI.
4. Encrypt client data for added security.

---

## Author

This project was developed by **KhalidSyntax**. Feel free to contribute or suggest improvements!

---

## Note

This is the first version of the Bank Management System. A second version, called **Bank Extension**, will be uploaded soon with additional features and improvements.

