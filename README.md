# CalculatorApp.API

## Overview

**CalculatorApp.API** is a simple web API developed using ASP.NET Core. It provides basic calculator functionality for performing arithmetic operations such as addition, subtraction, multiplication, and division. The API is designed to demonstrate the implementation of RESTful API principles using ASP.NET Core.

## Features

- **Addition**: Add two numbers.
- **Subtraction**: Subtract one number from another.
- **Multiplication**: Multiply two numbers.
- **Division**: Divide one number by another.
- **Error Handling**: Returns meaningful error responses for invalid inputs (e.g., division by zero).

## Technologies Used

- **Backend**: ASP.NET Core 6
- **Language**: C#
- **Testing**: Unit tests with xUnit
- **Tools**: Visual Studio, Postman (for API testing)

## Endpoints

The API has the following endpoints:

| Method | Endpoint                 | Description                        |
|--------|--------------------------|------------------------------------|
| `GET`  | `/api/calculator/add`    | Adds two numbers.                  |
| `GET`  | `/api/calculator/subtract` | Subtracts the second number from the first. |
| `GET`  | `/api/calculator/multiply` | Multiplies two numbers.             |
| `GET`  | `/api/calculator/divide`   | Divides the first number by the second.  |

### Sample Request

To perform an addition, send a `GET` request to the following endpoint:

```
GET /api/calculator/add?num1=5&num2=10
```

### Sample Response

```json
{
  "result": 15
}
```

## Getting Started

### Prerequisites

- .NET SDK 6.0 or later
- Visual Studio or Visual Studio Code
- Git
- Postman (optional for testing)

### Installation

1. **Clone the repository**:

   ```bash
   git clone https://github.com/miles-akio/CalculatorApp.API.git
   cd CalculatorApp.API
   ```

2. **Build the project**:

   ```bash
   dotnet build
   ```

3. **Run the project**:

   ```bash
   dotnet run
   ```

4. The API will be available at `https://localhost:5001` (or the specified port).

### Running Tests

To execute unit tests:

```bash
dotnet test
```

## Usage

You can use tools like **Postman** or **curl** to test the API endpoints. Below are some example requests:

- **Addition**: `GET https://localhost:5001/api/calculator/add?num1=10&num2=20`
- **Subtraction**: `GET https://localhost:5001/api/calculator/subtract?num1=30&num2=10`
- **Multiplication**: `GET https://localhost:5001/api/calculator/multiply?num1=5&num2=3`
- **Division**: `GET https://localhost:5001/api/calculator/divide?num1=10&num2=2`

## Project Structure

```
CalculatorApp.API/
├── Controllers/           # API Controllers
├── Models/                # Data models
├── Services/              # Business logic
├── Tests/                 # Unit tests
├── CalculatorApp.API.csproj
├── Program.cs
└── README.md
```

## Error Handling

The API includes error handling for cases such as:

- **Division by Zero**: Returns a `400 Bad Request` with an appropriate message.
- **Invalid Input**: Returns `400 Bad Request` if inputs are not valid numbers.

## Future Improvements

- Add support for more complex mathematical operations.
- Implement authentication for the API.
- Add Swagger/OpenAPI documentation for better API exploration.

## Contributing

Contributions are welcome! Please fork the repository and create a pull request for any changes. For major changes, please open an issue first to discuss what you would like to change.

1. **Fork the repository**
2. **Create a new branch** (`git checkout -b feature-branch`)
3. **Commit your changes** (`git commit -m 'Add some feature'`)
4. **Push to the branch** (`git push origin feature-branch`)
5. **Create a pull request**

## Contact

Created by [Miles Shinmachi](https://github.com/miles-akio) - feel free to reach out!
