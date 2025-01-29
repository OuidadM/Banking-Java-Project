# Banking-Java-Project
Bank transaction management application following ISO 20022 standards, allowing user registration, authentication, and secure money transfers, including single, multiple, and bulk payments.

# Application Execution Point  

To start the application, please run the **App.java** file located in:  
`com.Application` under `src.main.java`.  

## Project Structure and Registration Process  

### Registration  

To register in the application, the user must provide the necessary information in accordance with the **ISO 20022** standard:  

- **Name**: Maximum length of 144 characters, minimum of 2 characters.  
- **IBAN**: A valid IBAN must be provided.  
- **Email**: A valid email address is required.  
- **Password**: A password and confirmation must be provided.  
- **Bank**: The user must select a bank and provide its **BIC** (must match the database records).  
- **Identification Document**: The user must provide a unique identification document, such as:  
  - National identity card number.  
  - Passport identifier.  
- **Other Fields**: Optional fields are available.  

A **unique identifier** will be automatically assigned to each user upon registration.  

Finally, a **registration receipt** will be sent via email to the user.  

## Authentication  

The user can log into the application using their **unique identifier** (sent via email) and the **password** set during registration.  

## Home Interface  

The home interface allows users to view their **10 most recent transactions**.  

### Key Features  

#### Displaying Recent Transactions  

- Transactions are listed in **descending order** (newest to oldest).  
- Each transaction displays details including:  
  - **Date of transaction**  
  - **Beneficiary**  
  - **Amount**  
  - **Transaction type**  
  - **Transaction reason**  

#### Navigation to Transaction History  

- The user can return to this interface at any time by clicking the **History** button.  
- This interface provides a **quick and detailed view** of the most recent transactions for efficient financial management.  

## Features  

### Adding an Account  

- Users can add a **bank account** with a valid **IBAN** (ISO 20022-compliant).  
- This allows users to perform transactions from the newly added account.  
- Full IBAN validation ensures compliance with international format rules.  
- Unit tests have been implemented to verify IBAN validity and feature functionality.  

### Adding a Beneficiary  

- Users can register a **beneficiary** to send transactions to.  
- To add a beneficiary, the user must provide:  
  - **Beneficiary's full name**  
  - **Beneficiary's IBAN**  

## Single Transfers  

This feature allows users to perform a **single transfer** with the following options:  

### IBAN Selection  

- The user can select their own IBAN if they have multiple accounts.  

### Beneficiary Selection  

- Search for a **beneficiary** using their IBAN.  
- Select a previously added beneficiary from the **beneficiary list**.  

### Transaction Details  

- **Amount**: Mandatory field.  
- **Currency**: Must be specified.  
- **Transfer reason**: Optional but can be provided.  
- **Payment method**: Optional, chosen based on user preference.  

This feature ensures that all transactions meet mandatory requirements (**amount and currency**) while allowing flexibility with optional fields (**reason and payment method**).  

## Multiple Transfers  

The **multiple transfer** feature allows users to perform **up to three transfers** in a single operation, following **ISO 20022** standards.  

### Steps & Key Features  

#### Selecting the User's Account  

- If the user has multiple accounts, they must first select the account to use.  

#### Defining Transfer Details  

For each transfer, the user must provide:  

- **Beneficiary**:  
  - Select an existing beneficiary.  
  - Add a new beneficiary using an **IBAN search**.  
- **Transaction Amount**  
- **Currency Used**  

#### Additional Options  

- **Execution Date** of the transfer.  
- **Transaction Reason**  
- **Transfer Method** (as per ISO 20022 specifications).  

#### XML File Generation  

- At the end of the process, a **valid XML file** is generated in compliance with **ISO 20022**.  
- The file is automatically saved in:  
  - `Transaction_XML/VirementMultiple`  

This feature ensures **efficient multiple transfer management** while maintaining **ISO 20022 compliance**.  

## Bulk Transfers  

The **bulk transfer** feature allows users to perform **up to 5000 transfers** in a **single operation**, following **ISO 20022** standards.  

### Details  

#### Beneficiaries  

- Users can select an existing **beneficiary** or search for an IBAN to add a **new one**.  

#### Required Information  

- **Beneficiary** for each transfer.  
- **Transaction Amount**  
- **Currency Used**  

#### Additional Options  

- **Set an execution date** for each transfer.  
- **Choose the appropriate payment method**.  
  # Login Page:
  ![Login page](https://github.com/OuidadM/Banking-Java-Project/blob/25695959d4827beb3783207872f621be012c497b/login.jpg)

  # Sign up page:
  ![sign up 1](https://github.com/OuidadM/Banking-Java-Project/blob/25695959d4827beb3783207872f621be012c497b/signup_1.jpg)
  ![sign up 2](https://github.com/OuidadM/Banking-Java-Project/blob/25695959d4827beb3783207872f621be012c497b/signup_2.jpg)

  # Home page:
  ![Home page](https://github.com/OuidadM/Banking-Java-Project/blob/25695959d4827beb3783207872f621be012c497b/home.jpg)

  # Add account:
  ![add account page](https://github.com/OuidadM/Banking-Java-Project/blob/25695959d4827beb3783207872f621be012c497b/add_account.jpg)
  
  # Add beneficiary:
  ![add beneficiary page](https://github.com/OuidadM/Banking-Java-Project/blob/25695959d4827beb3783207872f621be012c497b/Add_beneficiary.jpg)

  # Search beneficiary:
  ![search beneficiary page](https://github.com/OuidadM/Banking-Java-Project/blob/25695959d4827beb3783207872f621be012c497b/search_beneficiary.jpg)
  
  # Single transfer:
  ![single transfer page](https://github.com/OuidadM/Banking-Java-Project/blob/c709b3c7ae8b12e4c808d9221064f6b77daaca87/virement_simple.jpg)

  # Multiple transfer:
  ![first transfer](https://github.com/OuidadM/Banking-Java-Project/blob/c709b3c7ae8b12e4c808d9221064f6b77daaca87/virement_multiple_1.jpg)
  ![second transfer](https://github.com/OuidadM/Banking-Java-Project/blob/5688a2155de90434f7aeaff0e496eb9658df7dc3/virement_multiple_2.jpg)
  ![third transfer](https://github.com/OuidadM/Banking-Java-Project/blob/5688a2155de90434f7aeaff0e496eb9658df7dc3/virement_multiple_3.jpg)
  
