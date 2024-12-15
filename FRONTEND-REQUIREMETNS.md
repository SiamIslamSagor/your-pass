# Client-Side Requirements for YOURPASS

This document outlines the detailed requirements for the **client-side** of YOURPASS, including the routes, sections, functionality, buttons, UI/UX guidelines, and content placement for each part of the application.

---

## Routes and Pages

### 1. Home Page (`/`)

- **Purpose**: Provide an overview of the application and a gateway for new and existing users.
- **Sections**:
  1. **Hero Section**:
     - A concise tagline explaining YOURPASS (e.g., "Secure. Simple. Your Password Manager.").
     - Call-to-Action (CTA) buttons:
       - **"Get Started"** (Navigates to the Sign-Up page).
       - **"Login"** (Navigates to the Login page).
  2. **Feature Highlights**:
     - List core features of YOURPASS (e.g., "Encrypted Vault," "Password Generator," "Secret Notes").
     - Visual icons to accompany features for clarity.
  3. **Footer Section**:
     - Links to About, Privacy Policy, and Contact pages.

### 2. Sign-Up Page (`/signup`)

- **Purpose**: Allow new users to create an account.
- **Sections**:
  1. **Form Section**:
     - Input fields: Full Name, Email, Password, Confirm Password.
     - Dropdown for selecting security questions (for account recovery).
     - Button: **"Create Account"** (Validates and stores user credentials).
  2. **Navigation Links**:
     - **"Already have an account? Login"** (Navigates to Login page).

### 3. Login Page (`/login`)

- **Purpose**: Authenticate existing users.
- **Sections**:
  1. **Form Section**:
     - Input fields: Email, Password.
     - Button: **"Login"** (Authenticates user and redirects to Dashboard).
     - Link: **"Forgot Password?"** (Navigates to Forgot Password page).

### 4. Dashboard (`/dashboard`)

- **Purpose**: Provide users access to their password vault and features.
- **Sections**:
  1. **Top Navigation Bar**:
     - Branding ("YOURPASS" logo).
     - Search bar for filtering passwords by title or category.
     - Profile dropdown (Logout, Settings).
  2. **Password Vault**:
     - Display a list of saved passwords in a card-based layout.
     - Each card contains:
       - Password title (e.g., "Google Account").
       - Category (e.g., "Social").
       - Buttons:
         - **"View"** (Decrypt and show password).
         - **"Edit"** (Open password edit form).
         - **"Delete"** (Prompt confirmation modal to delete the entry).
  3. **Quick Actions Panel**:
     - Button: **"Add Password"** (Navigates to Add Password page).
     - Button: **"Generate Password"** (Opens Password Generator modal).
     - Button: **"View Secret Notes"** (Navigates to Secret Notes page).

### 5. Add Password Page (`/add-password`)

- **Purpose**: Allow users to add a new password.
- **Sections**:
  1. **Form Section**:
     - Input fields: Title, Username, Password, URL, Description.
     - Dropdown for selecting category.
     - Button: **"Save Password"** (Validates and adds password to the vault).
     - Button: **"Cancel"** (Navigates back to Dashboard).

### 6. Secret Notes Page (`/secret-notes`)

- **Purpose**: Allow users to view, add, or share secure notes.
- **Sections**:
  1. **Notes List**:
     - Display a list of saved notes in a card-based layout.
     - Each card contains:
       - Note title.
       - Buttons:
         - **"View"** (Decrypt and show note details).
         - **"Edit"** (Open note edit form).
         - **"Delete"** (Prompt confirmation modal to delete the note).
     - Button: **"Add Note"** (Navigates to Add Note page).

### 7. Forgot Password Page (`/forgot-password`)

- **Purpose**: Allow users to recover access to their accounts.
- **Sections**:
  1. **Form Section**:
     - Input fields: Email, Security Question Answer.
     - Button: **"Reset Password"** (Sends email with reset link or OTP).

---

## Button Behavior and Navigation

### General Button Guidelines

- **Primary Buttons**: Use for critical actions (e.g., "Save," "Login").
  - Color: Blue with hover effects for clarity.
- **Secondary Buttons**: Use for non-critical actions (e.g., "Cancel").
  - Color: Gray with subtle hover effects.

### Button-Specific Actions

1. **Get Started**: Redirects to Sign-Up page.
2. **Login**: Authenticates and navigates to Dashboard on success.
3. **Add Password**: Opens Add Password form or modal.
4. **Generate Password**: Opens modal to generate a password.
5. **Save Password**: Saves the new password to the database.
6. **View/Edit/Delete**: Performs respective actions for passwords or notes.
7. **Reset Password**: Sends password recovery instructions.

---

## UI/UX Guidelines

### General Design Principles

1. **Consistency**:
   - Use a consistent color palette (Blue for primary actions, Gray for secondary actions).
   - Maintain uniform spacing and padding across components.
2. **Responsiveness**:
   - Ensure all pages are optimized for mobile and desktop views.
   - Use flexbox and grid systems for layout.
3. **Accessibility**:
   - Add ARIA labels for all buttons and forms.
   - Ensure proper contrast ratios for text and background colors.

### Specific Page Design Tips

- **Home Page**:
  - Use large, bold headings and high-quality illustrations/icons.
  - Keep CTAs prominent and above the fold.
- **Dashboard**:
  - Use collapsible side menus for better navigation on smaller screens.
  - Include tooltips for icons and buttons.
- **Forms (Sign-Up, Add Password, etc.)**:
  - Use clear placeholder text and labels.
  - Highlight validation errors with red text and icons.

---

This detailed breakdown provides all necessary information to develop the client-side of YOURPASS efficiently. Let me know if you need additional clarification or enhancements!

### Password Checking Feature

1.  **Feature Overview**:

    - Allow users to test their password's strength and check if it has been compromised in known data breaches.
    - Provide suggestions for improving weak passwords.

2.  **Implementation Approach**:

    - Use a third-party API like **Have I Been Pwned** to check if the password appears in known breaches.
    - Calculate password strength locally using metrics like length, complexity (symbols, numbers, etc.), and dictionary checks.

Let me know if you’re ready to explore this feature in detail.

### Simple and Easy-to-Develop Features

Here are some user-demanded features that are simple to implement:

1.  **Password Usage Counter**:

    - Display how many times a password has been accessed.
    - Helps users identify frequently used passwords for prioritizing updates.

2.  **In-App Notifications**:

    - Inform users about expired passwords, account recovery reminders, or app updates.
    - Easy to implement using a simple notification system.

3.  **Custom Tags for Passwords**:

    - Users can add tags (e.g., "banking," "social media") for easier filtering.
    - Tags improve organization and searchability.

4.  **Quick Copy**:

    - Add a "Copy" button next to passwords or usernames for quick copying to the clipboard.
    - Indicate success with a toast notification (e.g., "Copied to clipboard!").

5.  **Recently Viewed Passwords**:

    - Show a list of recently accessed passwords for convenience.

6.  **Color-Coded Categories**:

    - Assign colors to categories (e.g., blue for work, green for personal).
    - Enhance the visual experience and make categories stand out.
