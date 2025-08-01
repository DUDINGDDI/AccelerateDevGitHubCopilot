출시 예정

# Library App

## Description

Library App is a modular library management system built with .NET 8.0 and C#. It provides a console-based interface for managing patrons, books, and loans, with data persisted in JSON files. The application is organized into core, infrastructure, and presentation layers, and is designed for extensibility and testability.

## Project Structure

- AccelerateDevGitHubCopilot.sln
- README.md
- src/
  - Library.ApplicationCore/
    - Library.ApplicationCore.csproj
    - Entities/
    - Enums/
    - Interfaces/
    - Services/
  - Library.Console/
    - appSettings.json
    - CommonActions.cs
    - ConsoleApp.cs
    - ConsoleState.cs
    - Library.Console.csproj
    - Json/
      - Authors.json
      - Books.json
      - BookItems.json
      - Loans.json
      - Patrons.json
    - Program.cs
  - Library.Infrastructure/
    - Library.Infrastructure.csproj
    - Data/
      - JsonData.cs
      - JsonPatronRepository.cs
      - JsonLoanRepository.cs
- tests/
  - UnitTests/
    - LoanFactory.cs
    - UnitTests.csproj

## Key Classes and Interfaces

- **Entities**
  - `Patron`, `Loan`, `Book`, `BookItem`, `Author`  
    *(src/Library.ApplicationCore/Entities/)*
- **Enums**
  - `MembershipRenewalStatus`, `ConsoleState`, etc.  
    *(src/Library.ApplicationCore/Enums/, src/Library.Console/)*
- **Interfaces**
  - `IPatronRepository`, `ILoanRepository`, `IPatronService`, `ILoanService`  
    *(src/Library.ApplicationCore/Interfaces/)*
- **Services**
  - `PatronService`, `LoanService`  
    *(src/Library.ApplicationCore/Services/)*
- **Infrastructure**
  - `JsonData` – Loads and saves all data from/to JSON files  
    *(src/Library.Infrastructure/Data/JsonData.cs)*
  - `JsonPatronRepository`, `JsonLoanRepository` – Data access for patrons and loans  
    *(src/Library.Infrastructure/Data/)*
- **Console Application**
  - `ConsoleApp` – Main console UI logic  
    *(src/Library.Console/ConsoleApp.cs)*
  - `Program.cs` – Application entry point and dependency injection setup  
    *(src/Library.Console/Program.cs)*

## Usage

1. **Build the project**  
   Open a terminal in the repository root and run:
   ```sh
   dotnet build