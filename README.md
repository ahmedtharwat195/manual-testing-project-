Manual Testing Project – Guru99 Bank (Demo)
Manual test suite for the Manager Dashboard of Guru99 Bank Demo, covering functional testing, UI testing, and bug reporting across four core modules.

📋 Project Overview
ItemValueApplication Under TestGuru99 Bank – Manager DashboardURLhttps://demo.guru99.com/V1/index.phpTesting TypeManual Functional & UI TestingTotal Test Cases92Executed92Passed47Failed42Blocked3Bugs Reported19

🗂️ Test Sheets
1. UI Testing
Covers visual and layout issues across the manager dashboard.
Test Case IDDescriptionStatustc_ui_testing_001Footer alignment across different sidebar categories❌ Fail

2. Login Functionality (14 Test Cases)
Tests for the manager login page including valid/invalid credentials, reset button behavior, and session security.
CategoryTest IDsPass/FailValid logintc_Login_001✅ PassInvalid credentialstc_Login_002, 006, 007✅ PassMissing fieldstc_Login_003, 004, 005✅ PassReset buttontc_Login_011, 012, 013✅ PassPassword maskingtc_Login_014✅ PassCase sensitivitytc_Login_008❌ FailSession after back buttontc_Login_009❌ FailSession after logouttc_Login_010❌ Fail

3. Add New Customer Form (58 Test Cases)
Thorough validation testing for all input fields on the New Customer form.
Fields Covered:

Customer Name, Address, City, State
Date of Birth, PIN, Telephone, Email, Gender

Validation Types Tested Per Field:

Valid input acceptance
Blank / empty input
Special characters
Numbers where not allowed
Whitespace-only input
First character as space
Arabic characters
Min/max length constraints

Notable Failures:

Space between words in Customer Name rejected with wrong error message (bug_005)
Address field shows no validation errors on blank or invalid input (bug_007)
Email field accepts invalid formats including spaces, Arabic chars, and special characters (bug_015)
Backend fails on customer creation submit (bug_016)
Two test cases blocked due to backend failure (tc_add_new_customer_057, 058)


4. Add New Account Form (19 Test Cases)
Tests for adding a bank account to an existing customer.
Fields Covered: Customer ID, Account Type (dropdown), Initial Deposit
Key Scenarios:

Valid account creation
Customer ID not associated with manager
Customer ID blank / special chars / characters / leading space
Account type dropdown options
Initial deposit: valid (≥500), invalid (<500), blank, characters, special chars, whitespace

Notable Failures:

All customer ID validation shows no errors (bug_018)
All initial deposit validation shows no errors (bug_019)
Backend fails on account creation (bug_017)
1 test case blocked due to backend dependency


🐛 Bug Report Summary (19 Bugs)
By Severity
SeverityCount🔴 Critical5🟠 High1🟡 Medium4🔵 Low9
Critical Bugs
Bug IDTitlePrioritybug_002Login accepts case-insensitive credentialsHighbug_003Browser back button bypasses session logoutHighbug_004Direct URL access after logout bypasses sessionHighbug_016Backend failure on new customer creationHighbug_017Backend failure on new account creationHigh
High / Medium Bugs
Bug IDTitleSeveritybug_001Footer overlaps sidebar in manager dashboardMediumbug_005Customer name field rejects spaces between wordsMediumbug_010Date of Birth field accepts large invalid numbersMediumbug_015Email field accepts various invalid formatsMediumbug_007Address field allows invalid/blank input with no errorHigh
Low Bugs (9)
Mostly incorrect error messages displayed for whitespace-only, leading-space, or Arabic character inputs across: Customer Name, City, State, PIN, Telephone fields. Also includes missing asterisk indicator on Telephone label and no minimum length on Telephone field.

🛠️ Tools Used
ToolPurposeMicrosoft ExcelTest case documentation & bug trackingBrowser DevToolsManual test execution & observationGuru99 Bank DemoApplication under test

📁 File Structure
Manual_Project.xlsx
├── UI testing           – UI layout test cases
├── Login Functionality  – Login module test cases
├── Add New Customer Functionality – Form validation test cases
├── Add new account form – Account creation test cases
├── Bug Report           – All reported bugs with steps to reproduce
└── Test Summary         – Metrics overview
