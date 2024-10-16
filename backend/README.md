# Sports Facility Booking System

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Hosted Backend Link](https://gametheory-assignment-1.onrender.com/)
- [Tech Stack](#tech-stack)
- [API Endpoints](#api-endpoints)
- [User Roles](#user-roles)

## Introduction

The Sports Facility Booking System is a web app designed for users to book and manage sports facility reservations. It includes two user roles: regular users and administrators. Built with Express, Mongoose, TypeScript, Node.js, and Zod for validation, the system ensures a reliable and efficient backend. JWT is used for authentication and role-based authorization. Additionally, the project employs ESLint and Prettier to maintain code quality and consistent formatting.

## Features

- **User Registration and Authentication**
- **Role-Based Access Control (User and Admin)**
- **CRUD Operations for Bookings**
- **JWT-Based Authentication**
- **Facility Availability Check**
- **User Profile Management**

## Tech Stack

- **Backend:** Node.js, Express
- **Database:** MongoDB, Mongoose
- **Language:** TypeScript
- **Data Validation:** Zod
- **Authentication:** JWT
- **Linting & Formatting:** ESLint, Prettier

## API Endpoints

Here's a brief overview of the main API endpoints:

- **Auth:**

  - `POST /api/auth/signup` - Register a new user
  - `POST /api/auth/login` - Login a user

- **Facility:**

  - `POST /api/facility` - Create a facility (admin only)
  - `PUT /api/facility/:id` - Update a facility (admin only)
  - `GET /api/facility` - Get all facilities
  - `DELETE /api/facility/:id` - Soft Delete a facility by ID (admin only)

- **Bookings:**
  - `GET /api/check-availability` - Check the availability of time slots for booking on a specific date.
  - `POST /api/bookings` - Create a Booking (User Only)
  - `GET /api/bookings` - Get all Bookings (admin Only)
  - `GET /api/bookings/user` - Get all user specific Bookings (user only)
  - `DELETE /api/bookings/:id` - Cancel a booking by ID (user only)

## User Roles

- **User:**
  - Can create and manage their own bookings
  - Can view available facilities

- **Admin:**
  - Can manage all users and bookings
  - Can add or remove facilities
  - Has access to all user functionalities

