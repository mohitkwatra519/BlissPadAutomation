README: submitOrder Test Case – BlissPads Automation Framework
📌 Overview
This TestNG-based test case performs an end-to-end order submission flow for BlissPads, validating product selection, cart updates, and payment initiation. It uses data-driven testing, custom logging, and exception handling to ensure clarity and traceability.

🚀 Test Flow Summary
1️⃣ Launch application
2️⃣ Navigate to Sanitary Napkins section
3️⃣ Apply product filters
4️⃣ Select product
5️⃣ Select pack
6️⃣ Increase quantity
7️⃣ Add product to cart
8️⃣ Verify free shipping message
9️⃣ Verify product name
🔟 Proceed to checkout
1️⃣1️⃣ Switch to payment iframe
1️⃣2️⃣ Enter phone number


🧪 Test Data
- Driven via @DataProvider using HashMap<String, String>
- Fields:
- freeship: Expected free shipping message
- prodName: Expected product name in cart
- phoneNum: Phone number for checkout

📋 Logging Strategy
- INFO: Major steps and outcomes
- DEBUG: Test data preparation
- ERROR: Assertion failures and exceptions
- Visual separators: Box-style logs for test start/end
- Expected vs Actual: Logged before assertions for clarity

⚠️ Exception Handling
- AssertionError: Logged with message and stack trace
- Exception: Catches runtime issues (e.g., element not found, click failures)
- Custom exceptions like FrameworkException used for clarity

🧰 Dependencies
- TestNG 7.11.0
- Log4j2 via SLF4J bridge
- Custom utilities:
- LoggerUtil: Centralized logger
- BaseTest: Application launcher and driver setup
- Listeners: Screenshot capture and reporting

📸 Reporting & Screenshots
- Enabled via @Listeners(TestComponent.Listeners.class)
- Screenshots captured on failure
- Logs integrated with reporting tools (e.g., ExtentReports, if configured)

✅ Best Practices Followed
- Modular page objects (HomePage, ProductPage, etc.)
- Clear step numbering for traceability
- Reusable logging and exception patterns
- Data-driven design for scalability
- Clean separation of test logic and utilities
