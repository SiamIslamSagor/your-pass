# YOURPASS - Password Manager Web Application

A **user-friendly, privacy-focused password manager** to securely manage all your passwords in one place. Built using the **MERN stack**, YOURPASS ensures simplicity, flexibility, and modern security standards for everyday users.

---

## Table of Contents

- [Project Overview](#project-overview)
- [Requirements](#requirements)
  - [Core Requirements](#core-requirements)
  - [Technical Requirements](#technical-requirements)
- [Features](#features)
  - [Core Features](#core-features)
  - [Advanced Features](#advanced-features)
- [Tech Stack](#tech-stack)

---

## Project Overview

YOURPASS is designed to provide a lightweight and secure password management solution for individual users who want better control of their credentials without relying on large corporations. It emphasizes **ease of use**, **security**, and **flexibility** while being simple enough to develop and maintain as a solo developer.

---

## Requirements

### Core Requirements

1. **User Authentication**

   - Email and password-based login.
   - Password hashing using **bcrypt**.
   - Token-based authentication with **JWT** for secure session management.

2. **Password Vault**

   - Encrypted storage of user passwords (using **AES-256**).
   - CRUD operations (Create, Read, Update, Delete) for passwords.
   - Categories for easy organization (e.g., Work, Social, Personal).
   - Titles and descriptions for each password entry to enhance searchability and context.

3. **Password Generator**

   - Generate strong passwords with customizable options (length, symbols, numbers, etc.).

4. **Responsive Design**

   - Mobile-first UI, adaptable to various screen sizes.

5. **Data Validation**

   - Ensure all user inputs are properly validated on both client and server sides.

6. **Forgot Password Recovery**
   - Allow users to recover accounts via security questions or email-based verification.

### Technical Requirements

1. **Frontend**: Built with **React**, styled using **Tailwind CSS**.
2. **Backend**: API built with **Node.js** and **Express.js**.
3. **Database**: Password data stored securely in **MongoDB**.
4. **Encryption**: Encrypt passwords before storing in the database using **Crypto module**.
5. **Hosting**: Deployed on **Render** or **Vercel** for the frontend and **Railway** for the backend.

---

## Features

### Core Features

1. **Secure Password Vault**

   - Fully encrypted password storage.
   - Simple and intuitive interface for managing credentials.

2. **Password Generator**

   - Easy-to-use tool to create strong, random passwords.
   - Options for customizing length, inclusion of symbols, numbers, etc.

3. **Categorization**

   - Group passwords into custom categories (e.g., Work, Personal, Banking).

4. **Master Password and Access Options**

   - Single master password for unlocking the vault.
   - Option to set a 4-digit PIN or unlock using a pattern for quicker access.
   - The master password is not stored anywhere (zero-knowledge encryption).

5. **Search Functionality**

   - Quick search to find saved credentials by title, description, or category.

6. **Dark Mode**

   - User toggle for light and dark themes.

7. **Auto Lock**

   - Application auto-locks after a set period of inactivity, requiring reauthentication.

8. **Secret Notes**

   - Add and store secure notes alongside passwords.
   - Shareable notes with expiration settings for temporary sharing of sensitive information.

9. **Access History**
   - Display a history of recent access times for transparency and detecting unauthorized usage.

### Advanced Features

1. **Login Activity Log**

   - Show recent login history for user accounts to detect unauthorized access.

2. **Customizable UI**

   - Users can customize themes or layouts for a personal touch.

3. **Password Strength Analysis**

   - Display password strength scores and suggest improvements (e.g., "Weak," "Strong," "Very Strong").

4. **Favorite Passwords**

   - Allow users to mark frequently used passwords as favorites for quick access.

5. **Password Expiry Notifications**
   - Notify users when a password is too old and suggest updating it for better security.

---

## Tech Stack

- **Frontend**: React, Tailwind CSS
- **Backend**: Node.js, Express.js
- **Database**: MongoDB
- **Encryption**: Crypto module (AES-256 for password encryption)
- **Authentication**: JWT and bcrypt
- **Deployment**: Render, Vercel, or Railway
