# Finova Market Data Viewer – README

## 1. What is a Payment Gateway?

### Definition

A **payment gateway** is a service that enables online applications to accept and process digital payments in a secure way. It works as a bridge between the customer, the merchant’s application, the bank, and the card network, ensuring that payment information is transmitted safely.

### Why Payment Gateways Are Required in Online Applications

Payment gateways are essential because they:

* Secure sensitive payment details such as card numbers and UPI IDs
* Handle payment authorization and verification
* Reduce fraud and misuse of financial data
* Ensure compliance with security standards like PCI-DSS

Without a payment gateway, an application cannot safely process online transactions.

### Real-World Examples

* **Razorpay** – Popular in India for UPI, cards, wallets, and net banking
* **Stripe** – A global payment platform used by many startups and enterprises
* **PayPal** – A widely used digital wallet and online payment system

---

## 2. Components Involved in Online Payment Processing

### User / Customer

The user is the person who initiates the payment by clicking the “Pay Now” button and providing payment details.

### Frontend (Website / Application)

The frontend:

* Displays the payment interface
* Collects user input
* Sends payment-related requests to the backend server

### Backend (Server)

The backend:

* Receives requests from the frontend
* Communicates securely with the payment gateway
* Stores transaction status and handles validation

### Payment Gateway

The payment gateway:

* Encrypts payment data
* Connects with banks and card networks
* Returns success or failure responses

### Bank / Card Network

The bank or card network:

* Checks account balance and validity
* Approves or rejects the transaction

---

## 3. Payment Flow (Step-by-Step Explanation)

1. The user clicks **Pay Now** on the website or application
2. The frontend sends payment details to the backend server
3. The backend forwards the request to the payment gateway
4. The payment gateway contacts the bank or card network
5. The bank approves or declines the transaction
6. The payment gateway sends the response back to the backend
7. The backend updates the transaction status
8. The frontend displays the final result to the user

---

## 4. Payment Gateway Architecture

### Why the Frontend Alone Cannot Handle Payments

* Frontend code is visible to users
* Sensitive information can be easily exposed
* Secret keys cannot be safely stored

### Why a Backend Server Is Mandatory

* Keeps API keys and credentials secure
* Performs verification and validation
* Acts as a trusted middle layer between frontend and gateway

### Role of APIs in Payment Processing

APIs enable secure communication between:

* Frontend and backend
* Backend and payment gateway
* Payment gateway and bank

They follow a request–response model to complete transactions reliably.

---

## 5. Architecture Diagram (Conceptual)

```
User
  ↓
Frontend (Web / App)
  ↓
Backend Server
  ↓
Payment Gateway
  ↓
Bank / Card Network
```

**Data Flow:** User → Frontend → Backend → Gateway → Bank → Gateway → Backend → Frontend

---

## 6. Security Concepts (Conceptual Overview)

### Why Payment Data Must Be Secured

* Prevents financial fraud
* Protects user privacy
* Maintains trust in online systems

### Why Sensitive Information Must Never Be Stored on the Frontend

* Frontend is accessible to anyone using the browser
* Data can be inspected or manipulated

### Risks of Insecure Payment Handling

* Data breaches
* Unauthorized transactions
* Financial and legal consequences

---

## 7. Relation to This Project (Finova Market Data Viewer)

### Use of APIs in Finova Market Data Viewer

* Fetches live cryptocurrency market data
* Receives data in JSON format
* Updates the UI dynamically based on responses

### Use of APIs in Payment Gateways

* Accept payment requests
* Process transactions
* Return structured responses

### One Key Similarity

Both **market data APIs** and **payment gateway APIs**:

* Use HTTP-based communication
* Return structured data (JSON)
* Require secure and controlled access

---

## DOM Manipulation in This Project

DOM manipulation is used to:

* Read user input from the search field
* Update stock and cryptocurrency information dynamically
* Render price charts using Chart.js

---

## Data Flow in the Finova Market Data Viewer

```
User Input → JavaScript → API Request → API Response → DOM Update → UI Display
```

---

## Simple Project Architecture Diagram

```
Client (Browser)
   ↓
Market Data API (CoinGecko)
   ↓
UI Update (DOM + Chart.js)
```

---

## Screenshots 

* User Interface screenshot
  <img width="1887" height="878" alt="image" src="https://github.com/user-attachments/assets/6bcb814d-4756-4ffa-b313-91994d843533" />


* Chart output screenshot
* Git command screenshots:

  * `git add .`
  * `git commit -m "Initial commit"`
  * `git push`

---

## Final Notes

* No payment gateway integration is implemented in this project
* This project focuses on **conceptual understanding** of payment gateways
* APIs are used only for learning and demonstration purposes


