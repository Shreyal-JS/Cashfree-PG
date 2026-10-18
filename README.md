# Cashfree PG Integration for Event / E-commerce Fee Collection

This project demonstrates a Cashfree Payment Gateway integration for event registration and e-commerce style fee collection. It is designed for scenarios where a user fills out a form, submits payment for an event or order, and the system stores the transaction details in a database while sending a personalized confirmation email.

The app is built with:
- React.js for the frontend
- Express.js for the backend API
- Cashfree PG for secure payment initiation and verification
- Custom handling for order/payment data and confirmation emails

## Features

- Event / product registration form workflow
- Fee/charge collection through Cashfree payment gateway
- Secure order creation and payment verification
- User details + event/order details capture
- Data persistence to database
- Custom confirmation email for:
  - Event details
  - User information
  - Payment status / confirmation
- Ready for sandbox testing with Cashfree

## Tech Stack

- Frontend: React + Vite
- Backend: Node.js + Express
- Payment Gateway: Cashfree PG
- API Communication: Axios
- Environment config: dotenv

## Project Structure

```bash
Cashfee-PG/
├── client/
│   ├── src/
│   ├── package.json
│   ├── vite.config.js
│   └── index.html
├── server/
│   ├── index.js
│   └── package.json
├── README.md
├── SECURITY.md
└── .gitignore
```

## Payment Flow

1. User fills the event / checkout form.
2. Frontend sends a request to the backend to create a Cashfree order.
3. Backend generates an order and returns a payment session ID.
4. Payment is processed using Cashfree checkout in sandbox mode.
5. Backend verifies the payment status.
6. Registrant details and payment info can be saved in a database.
7. Custom invoice / confirmation email is sent to the user.

## Installation

Clone the repository:

```bash
git clone https://github.com/Shreyal-JS/Cashfee-PG.git
cd Cashfee-PG
```

Install frontend dependencies:

```bash
cd client
npm install
```

Install backend dependencies:

```bash
cd ../server
npm install
```

## Environment Setup

Create a `.env` file inside the `server` folder:

```env
CLIENT_ID=your_cashfree_client_id
CLIENT_SECRET=your_cashfree_client_secret
PORT=5000
```

If your implementation includes database and email services, add those environment values as well, for example:

```env
DB_HOST=localhost
DB_USER=your_db_user
DB_PASSWORD=your_db_password
DB_NAME=your_db_name
SMTP_HOST=smtp.example.com
SMTP_PORT=587
SMTP_USER=your_email
SMTP_PASS=your_email_password
```

## Run the Project

Start the backend server:

```bash
cd server
npm run dev
```

Start the frontend app:

```bash
cd client
npm run dev
```

Then open the local frontend URL provided by Vite in the browser.

## Notes

- This project uses Cashfree sandbox mode for testing.
- Replace the sandbox credentials with production credentials before deploying.
- The database and email logic can be integrated as needed based on your business rules.
- The repository currently includes the core payment gateway flow and can be extended to store registration records and send custom emails.

## Example Use Cases

- Event registration with ticket fee collection
- Conference or workshop enrollment
- E-commerce checkout with payment collection
- Donation or membership fee processing
- Custom payment-based form submissions

## Contribution

Contributions, improvements, and feature additions are welcome. If you want to extend this project with database persistence, email notifications, or a full registration system, you can build on the existing payment flow.

## License

This project is currently provided for educational and development purposes. Add an appropriate license if you plan to distribute it publicly.
