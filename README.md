# 🚌 TransitDesk

A Node.js REST API for managing bus tickets, passengers, and ticket availability.

Built with Express.js and MongoDB, with automated API testing using Mocha, Chai, and Supertest.

---

## ✨ Features

- 🎫 Book and manage bus tickets
- 🔓 Track open and closed tickets
- 👤 Store passenger details
- 🔄 Update ticket status and passenger information
- 🛠️ Admin API to reset all tickets
- 🗄️ MongoDB Atlas integration
- 🧪 Automated API testing
- ☁️ AWS EC2 deployment

---
## 🚀 Getting Started

Clone the repository, install the dependencies, start the server, and run the test suite:

    git clone https://github.com/PoojaRani24/BusTicketing.git
    cd BusTicketing
    npm install
    npm start
    npm run test

The server runs on port `3000`.

---
## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| Node.js | Backend runtime |
| Express.js | REST API |
| MongoDB Atlas | Database |
| Mocha | Testing framework |
| Chai | Assertions |
| Supertest | API testing |
| AWS EC2 | Deployment |

---

## 🎫 Ticket Lifecycle

A ticket moves between two states:

**OPEN** → Available for booking

**CLOSED** → Assigned to a passenger

The admin reset endpoint can reopen all tickets when required.

---

## 📡 API Endpoints

### Ticket Management

| Method | Endpoint | Description |
|---|---|---|
| `PATCH` | `/tickets/:ticketId/update` | Update ticket status and passenger details |
| `GET` | `/tickets/:ticketId/status` | View ticket status |
| `GET` | `/tickets/open` | View all open tickets |
| `GET` | `/tickets/close` | View all closed tickets |
| `GET` | `/tickets/:ticketId/details` | View passenger details |
| `GET` | `/tickets/:ticketId` | View a ticket by ID |
| `POST` | `/tickets/book` | Create a new ticket |

### Admin

| Method | Endpoint | Description |
|---|---|---|
| `PATCH` | `/admin` | Reset the system and reopen all tickets |

### Development & Testing

| Method | Endpoint | Description |
|---|---|---|
| `DELETE` | `/tickets/id/:ticketId` | Delete a specific ticket |
| `DELETE` | `/tickets/true` | Delete all closed tickets |
| `DELETE` | `/tickets/false` | Delete all open tickets |

---

## 📝 Update Ticket

The update endpoint accepts a list of properties to modify.

Example payload:

`[{"propName":"name","value":"updatedname"},{"propName":"src","value":"newsource"}]`

This can be used to update passenger information, source, destination, and ticket status.

---

## 🔄 How It Works

**Client Request**

↓

**Express.js REST API**

↓

**Ticket Management Logic**

↓

**MongoDB Atlas**

↓

**API Response**

The application handles ticket creation, status management, passenger information, and administrative operations through RESTful endpoints.

---

## 🗄️ Database

The application uses **MongoDB Atlas** for persistent storage.

Ticket records contain information such as:

- Ticket ID
- Passenger name
- Source
- Destination
- Ticket status

---

## 🧪 Testing

The API is tested using:

- **Mocha** — Test runner
- **Chai** — Assertion library
- **Supertest** — HTTP/API testing

The test suite covers ticket creation, updates, status checks, deletion, and other API operations.

---

## ☁️ Deployment

Previously deployed on AWS EC2 and configured to run on port 3000

---

## 🎯 What This Project Demonstrates

- REST API design with Node.js
- Express.js backend development
- MongoDB database integration
- CRUD operations
- Ticket state management
- API testing
- AWS EC2 deployment

---

## 📚 What I Learned

Building BusFlow helped me gain hands-on experience with:

- Designing RESTful APIs
- Structuring a Node.js backend
- Working with MongoDB
- Managing state transitions
- Writing API tests
- Debugging backend services
- Deploying applications on AWS

---

## 👩‍💻 Author

**Pooja Rani**

[GitHub](https://github.com/PoojaRani24)

---

## 📄 License

This project is licensed under the MIT License.
