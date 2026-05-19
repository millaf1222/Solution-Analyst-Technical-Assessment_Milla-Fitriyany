# Solution-Analyst-Technical-Assessment_Milla-Fitriyany


## Project Overview
This project is developed as part of a Solution Analyst technical assessment.  
It provides a high-level and detailed design for a mobile loan application system, covering user flow, system architecture, API design, and screen behavior.

The design illustrates how users interact with the system from authentication, loan submission, document verification, to payment processing.

---

## Features Scope
The application includes the following main features:

- User Authentication (Login, Register, OTP Verification)
- Loan Application and Submission
- Loan Status Monitoring (Approved, Pending, Rejected)
- Installment and Payment Processing
- Document Upload and Verification
- Notifications
- User Profile Management

---

## High Level Architecture
The system consists of the following components:

- Mobile Application  
  Handles user interaction and user interface

- Backend API  
  Manages business logic such as authentication, loan processing, and payment handling

- Database  
  Stores user data, loan data, installments, payments, and documents

- External Services  
  Payment gateway integration for processing transactions

---

## Screen Flow
The screen flow represents the end-to-end user journey:

1. Splash Screen → Login or Dashboard  
2. Login or Register → OTP Verification → Success  
3. Dashboard → Loan Application  
4. Apply Loan → Review → Submit  
5. Loan Status → Loan Detail  
6. Installment → Payment Flow  
7. Document Upload → Verification Status  
8. Notifications and Profile  

This flow covers the full lifecycle from user onboarding to loan repayment.

---

## Entity Relationship Diagram (ERD)
The system includes the following entities:

- User
- Loan
- Installment
- Payment
- Document

Relationships:
- One User can have multiple Loans (history)
- One User can only have one active loan at a time
- One Loan can have multiple Payments  

---

## API Design
The design focuses on three core APIs:

### Login API
- Handles user authentication  
- Validates user credentials  
- Returns authentication token if successful  

### Loan Submission API
- Handles loan application process  
- Validates active loan and required data  
- Stores loan with Pending status  

### Payment API
- Handles installment payments  
- Integrates with payment gateway  
- Updates payment status and remaining balance  

---

## Screen Behavior
Each screen is designed with behavior aligned to the screen flow.

### Splash Screen
- Checks authentication token  
- If valid, navigate to Dashboard  
- If not, navigate to Login  

### Login Screen
- User inputs credentials  
- Validates input  
- Calls Login API  
- Success navigates to Dashboard  
- Failure shows error message  

### Dashboard
- Fetches user and loan data  
- Provides navigation to key features:
  - Apply Loan
  - Loan List
  - Payment
  - Upload Document
  - Notifications
  - Profile  

### Loan Flow
- User inputs loan details  
- Reviews and submits loan  
- Calls Loan API  
- Displays loan status  

### Payment Flow
- User selects payment method  
- Confirms payment  
- System processes payment  
- Displays result (success or failure)  

All screen behaviors are aligned with the defined user journey and business process.

---

## Notes
- This design focuses on clarity and completeness based on assessment requirements  
- Implementation details are simplified to emphasize system design  
- All components are aligned across screen flow, API design, and data model  

---

## Author
Solution Analyst Technical Assessment Submission
