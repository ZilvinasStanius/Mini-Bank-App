# Mini Bank App

## Project Overview

This project was one of the first that helped me understand what **Express.js** is and how it works. It was fascinating to learn about **routing**, and I also enjoyed working with the **fs** (filesystem) module.

## Technologies Used

- **Node.js**
- **Express.js**
- **CORS** (To allow frontend-backend communication)
- **body-parser** (For handling incoming request bodies)
- **Filesystem (fs)** (To store user data in JSON format)

## Features

- **Create an account** (Generates a unique ID)
- **Deposit and withdraw funds**
- **View transaction history** (with date and amount)
- **Validate user actions** (e.g., age restriction, balance limits)
- **Simple front-end simulation for interaction**

## Installation & Setup

### 1. Clone this repository:

```sh
git clone https://github.com/ZilvinasStanius/Mini-Bank-App.git
```

### 2. Open Backend and Frontend Separately in VS Code

After cloning, you need to **open the backend and frontend folders separately** in VS Code.

- Open **Mini Bank App B.E/** in a new VS Code window for the backend.
- Open **Mini Bank App F.E/** in another VS Code window for the frontend.

This ensures both parts work properly without conflicts.

### 3. Navigate to the backend folder and install dependencies:

```sh
npm install
```

### 4. Start the backend server:

```sh
npm run dev
```

The backend will run on `http://localhost:7000`

### 5. Open the frontend and start a **Live Server**

Simply open the **Mini Bank App F.E/** folder in VS Code and click **"Go Live"** (if you have the **Live Server extension** installed). It will automatically load the frontend on port `5502`.

If needed, you can also manually configure the port:

```sh
{
  "liveServer.settings.port": 5502
}
```

## How to Use

1. **Create an Account**

   - Enter your **name, last name, and age** (Minimum age: **18**)
   - After account creation, an **ID** is generated.

2. **Manage Your Account**
   - Enter your **ID** to access account management.
   - You can **deposit funds, withdraw funds**, and view your **transaction history**.

## API Endpoints

| Method     | Endpoint               | Description                   |
| ---------- | ---------------------- | ----------------------------- |
| **POST**   | `/saskaita/sukurti`    | Create a new bank account     |
| **GET**    | `/saskaita/:id`        | Retrieve user account details |
| **POST**   | `/saskaita/:id/imoka`  | Deposit money into account    |
| **POST**   | `/saskaita/:id/ismoka` | Withdraw money from account   |
| **DELETE** | `/saskaita/:id/delete` | Delete an account             |

## Authentication & Security

- **Users are identified by their ID**
- **Age restriction (18+)**
- **Deposits and withdrawals validate the balance before proceeding**

## Demo

#### Here’s a small demo showing how Mini Bank system works:

![Demo GIF](/demo.gif)
