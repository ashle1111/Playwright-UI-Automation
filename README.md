# Playwright UI Automation Technical Assessment

This project is a UI automation suite developed using [Microsoft Playwright](https://playwright.dev/dotnet/) and [NUnit](https://nunit.org/). It automates various user interactions on the [Automation Exercise](https://automationexercise.com) website, focusing on functionalities like shopping cart operations.

---

## 📋 Table of Contents

- [Project Overview](#project-overview)
- [Technologies Used](#technologies-used)
- [Setup Instructions](#setup-instructions)
- [Running Tests](#running-tests)
- [Test Scenarios](#test-scenarios)
- [Project Structure](#project-structure)

---

## 📌 Project Overview
The primary objective of this project is to validate the shopping cart functionality of the Automation Exercise website. The automation suite performs actions such as adding products to the cart, updating quantities, and verifying cart total.

---

## 🛠️ Technologies Used
- **[Microsoft Playwright for .NET](https://playwright.dev/dotnet/)**: For browser automation.
- **[NUnit](https://nunit.org/)**: As the testing framework.
- **.NET 8.0 SDK**: The development platform.
- **C#**: Programming language.

---

## ⚙️ Setup Instructions

1. **Clone the Repository**:

   ```bash
   git clone https://github.com/yourusername/PlaywrightTests.git
   cd PlaywrightTests
   ```

2. **Install Dependencies**:

   Ensure you have the [.NET 8.0 SDK](https://dotnet.microsoft.com/download/dotnet/8.0) installed. Then, restore the project dependencies:

   ```bash
   dotnet restore
   ```

3. **Install Playwright Browsers**:

   ```bash
   playwright install
   ```

---

## 🚀 Running Tests

To execute all test:

```bash
dotnet test
```

To run a specific test case:

```bash
dotnet test --filter "Name=Cart_ShouldIncrementQty_WhenSameItemAddedTwice"
```

To run tests with detailed console output:

```bash
dotnet test --logger:"console;verbosity=detailed"
```

---

## 🧪 Test Scenarios

The automation suite covers the following scenarios:

1. **Add Product to Cart**:
   - Navigate to the productpage.   
   - Add a product to thecart.   
   - Verify the quantity is updated to 1.

2. **Update Product Quantity**:
   - Navigate to the product detailpage.   
   - Increase the quantity to 2.   
   - Add to cart and verify the quantity is updated accordingly.

3. **Remove Product from Cart**:
   - Navigate to the cartpage.   
   - Remove the product from thecart.   
   - Verify the cart is empty.

---

## 📁 Project Struture

```plaintext
PlaywrightTests/
├── Api/
│   └── ApiHelper.cs
├── Pages/
│   └── CartPage.cs
│   └── ProductsPage.cs
│   └── RegistrationPage.cs
├── Tests/
│   └── CartTests.cs
│   └── ProductSearchTests.cs
│   └── RegistrationTests.cs
│   └── TestBase.cs
├── Utilities/
│   └── TestDataGenerator.cs
├── PlaywrightTests.csproj
└── README.md
```

- **Pages/**: Contains page object models for different pages.
- **Test/**: Houses the test classes.
- **Utilities/**: Generate random data for registration.

- **API Verification** - Line no. 41 - RegistrationTests.cs

- **Run same Tests in Multiple Data** - ProductSearchTests.cs From Line no. 16. 
