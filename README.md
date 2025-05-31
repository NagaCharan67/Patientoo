# Patientoo - Healthcare Management App

Patientoo is a comprehensive, full-stack healthcare management application designed to streamline the process of booking and managing doctor's appointments. It features separate interfaces for patients and administrators, built with modern web technologies including the MERN stack (MongoDB, Express.js, React, Node.js), Vite, and Tailwind CSS.

Live Link : https://patientoo-heathcare-management-app-0eqb.onrender.com/

## Features

### Patient Features
- **User Authentication:** Secure registration and login functionality.
- **Browse Doctors:** View a list of doctors and filter them by speciality.
- **Doctor Profiles:** Access detailed profiles including qualifications, experience, and fees.
- **Appointment Booking:** Schedule appointments based on real-time available slots.
- **Online Payments:** Securely pay for appointments using Razorpay or Stripe.
- **Appointment Management:** View and manage personal appointments (upcoming, paid, completed, cancelled).
- **Profile Management:** Update personal information and profile picture.

### Admin Features
- **Secure Admin Login:** Dedicated and secure login for administrators.
- **Dashboard:** An overview of total doctors, patients, and appointments.
- **Appointment Management:** View all appointments and their statuses.
- **Doctor Management:** Add new doctors to the platform and view all registered doctors.

## Tech Stack

- **Backend:**
  - Node.js, Express.js
  - MongoDB with Mongoose
  - JSON Web Tokens (JWT) for Authentication
  - Bcrypt for Password Hashing
  - Cloudinary for Image Storage
  - Stripe & Razorpay for Payment Processing
  - Multer for file uploads

- **Frontend (Patient & Admin):**
  - React (with Hooks and Context API)
  - Vite for a fast development experience
  - React Router for client-side routing
  - Tailwind CSS for styling
  - Axios for API requests
  - React Toastify for notifications

## Project Structure

The project is organized into three main directories:
- `frontend/`: Contains the patient-facing React application.
- `backend/`: Contains the Node.js and Express.js server, API logic, and database models.
- `admin/`: Contains the separate React application for the admin panel.

## Getting Started

To get a local copy up and running, follow these simple steps.

### Prerequisites

- Node.js (v16 or higher)
- npm or yarn
- MongoDB (a local instance or a cloud service like MongoDB Atlas)
- A Cloudinary account for image storage.
- A Stripe and/or Razorpay account for payment processing.

### Cloning the Repository

1.  Open your terminal.
2.  Run the following command to clone the repository:
    ```bash
    git clone https://github.com/yourusername/Patientoo-HeathCare_Management_App.git
    ```
3.  Navigate to the project directory:
    ```bash
    cd Patientoo-HeathCare_Management_App
    ```

### Backend Installation

1.  Navigate to the `backend` directory:
    ```bash
    cd backend
    ```
2.  Install the backend dependencies:
    ```bash
    npm install
    ```
3.  Create a `.env` file in the `backend` directory and add the following environment variables:
    ```env
    PORT=4000
    MONGO_URI=your_mongodb_connection_string
    JWT_SECRET=your_jwt_secret_key

    # Cloudinary Credentials
    CLOUDINARY_CLOUD_NAME=your_cloudinary_cloud_name
    CLOUDINARY_API_KEY=your_cloudinary_api_key
    CLOUDINARY_API_SECRET=your_cloudinary_api_secret

    # Admin Credentials
    ADMIN_EMAIL=admin@example.com
    ADMIN_PASSWORD=adminpassword

    # Payment Gateway Credentials
    CURRENCY=INR
    STRIPE_SECRET_KEY=your_stripe_secret_key
    RAZORPAY_KEY_ID=your_razorpay_key_id
    RAZORPAY_KEY_SECRET=your_razorpay_key_secret
    ```

### Frontend (Patient App) Installation

1.  Navigate to the `frontend` directory from the root:
    ```bash
    cd frontend
    ```
2.  Install the frontend dependencies:
    ```bash
    npm install
    ```
3.  Create a `.env` file in the `frontend` directory and add the following:
    ```env
    VITE_BACKEND_URL=http://localhost:4000
    VITE_CURRENCY=INR
    VITE_RAZORPAY_KEY_ID=your_razorpay_key_id
    ```

### Admin Panel Installation

1.  Navigate to the `admin` directory from the root:
    ```bash
    cd admin
    ```
2.  Install the admin panel dependencies:
    ```bash
    npm install
    ```
3.  Create a `.env` file in the `admin` directory and add the following:
    ```env
    VITE_BACKEND_URL=http://localhost:4000
    VITE_CURRENCY=INR
    ```

## Running the Project

To run the application, you need to start the backend, frontend, and admin servers in separate terminal windows.

### Backend

1.  Navigate to the `backend` directory:
    ```bash
    cd backend
    ```
2.  Start the backend server (with nodemon for auto-reloading):
    ```bash
    npm run dev
    ```
    Or for production:
    ```bash
    npm start
    ```
3.  The backend will be running on the port specified in your `.env` file (e.g., `http://localhost:4000`).

### Frontend

1.  Navigate to the `frontend` directory:
    ```bash
    cd frontend
    ```
2.  Start the frontend application:
    ```bash
    npm run dev
    ```
3.  Open your browser and navigate to `http://localhost:5173` (or the port specified by Vite) to see the application.

### Admin Panel

1.  Navigate to the `admin` directory:
    ```bash
    cd admin
    ```
2.  Start the admin application:
    ```bash
    npm run dev
    ```
3.  Open your browser and navigate to the URL provided by Vite (e.g., `http://localhost:5174`).

