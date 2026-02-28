# Bank Account Management System

A robust, event-driven bank account management system built with Java and Maven, implementing the **CQRS (Command Query Responsibility Segregation)** architectural pattern.

## 📋 Project Overview

This project demonstrates a modern approach to building scalable financial services applications using event sourcing and command-query segregation principles. It separates read and write operations into distinct modules for improved performance, scalability, and maintainability.

## 🏗️ Project Structure

```
Bank-Account/
├── account.cmd/          # Command module - handles account operations (deposits, withdrawals, etc.)
├── account.common/       # Common module - shared utilities, models, and interfaces
├── account.query/        # Query module - handles account information retrieval
├── pom.xml              # Maven parent project configuration
└── .gitignore           # Git ignore rules
```

### Module Descriptions

- **account.cmd**: Processes commands and handles state changes to bank accounts
- **account.common**: Contains shared domain models, DTOs, events, and utilities used across modules
- **account.query**: Provides query capabilities for retrieving account information efficiently

## 🛠️ Technology Stack

- **Language**: Java
- **Build Tool**: Maven
- **Architecture**: CQRS (Command Query Responsibility Segregation)
- **Pattern**: Event Sourcing

## 🚀 Getting Started

### Prerequisites

- Java JDK 11 or higher
- Maven 3.6 or higher

### Installation

1. Clone the repository:
```bash
git clone https://github.com/JulianFicher/Bank-Account.git
cd Bank-Account
```

2. Build the project:
```bash
mvn clean install
```

3. Run the application:
```bash
mvn spring-boot:run
```

## 📝 Features

- ✅ Account creation and management
- ✅ Deposit and withdrawal operations
- ✅ Account balance queries
- ✅ Transaction history tracking
- ✅ Event-driven architecture

## 🔄 CQRS Architecture

The project implements CQRS to separate:
- **Command Side** (account.cmd): Handles all write operations that modify state
- **Query Side** (account.query): Optimized for read operations and data retrieval

This separation allows independent scaling and optimization of each side based on specific requirements.

## 💡 How It Works

1. **Commands** are sent to the command module to perform operations (create account, deposit, withdraw)
2. **Events** are generated as a result of successful commands
3. **Events** are stored and propagated to the query module
4. **Queries** are executed against the query module to retrieve current state

## 📦 Building

Build the entire project with Maven:

```bash
mvn clean package
```

## 🧪 Testing

Run tests for all modules:

```bash
mvn test
```

## 📚 API Documentation

For detailed API documentation and usage examples, please refer to the individual module README files.

## 🤝 Contributing

Contributions are welcome! Please feel free to submit pull requests or open issues for bugs and feature requests.

## 📄 License

This project is open source and available under the MIT License.

## 👤 Author

**Julian Fischer**
- GitHub: [@JulianFicher](https://github.com/JulianFicher)

## 📞 Support

For support, please open an issue in the GitHub repository.

---

**Last Updated**: February 2026