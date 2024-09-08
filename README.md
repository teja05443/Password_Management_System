# Password_Management_System

This project features a bot designed to automate the process of handling password reset requests through a two-stage process: Dispatcher and Performer.

## Overview

The Password Management System bot streamlines password recovery by interacting with Google accounts and managing user credentials. It automates the retrieval and verification of user data, ensuring efficient password resets.

## Components

## UiPath Integration

1. **Download/Clone the Repository:**
   Clone or download the repository containing the `dispatcher` and `performer` UiPath projects.

2. **Upload to UiPath Studio:**
   - Open UiPath Studio.
   - Create a new project or open an existing one.
   - Upload the respective `main.xaml` files for the dispatcher and performer stages into UiPath Studio.

3. **Run the Workflows:**
   - For the dispatcher, upload the `dispatcher_main.xaml` file and run it to start processing emails and user details.
   - For the performer, upload the `performer_main.xaml` file and run it to verify data and send temporary passwords.

### Dispatcher

- **Role**: Gathers credentials for the user's Google account and processes incoming emails.
- **Process**:
  1. Collects credentials from incoming emails.
  2. Reads an Excel document to extract details of users who have forgotten their passwords, including their usernames and employee codes.
  3. Moves processed emails to a "Processed" folder.

### Performer

- **Role**: Verifies user data and sends temporary passwords.
- **Process**:
  1. Checks if all user data from the Excel file is available in the queue.
  2. Validates that all required fields (username, employee code, and email) are correctly filled.
  3. Sends an email with a temporary password to the user if all data is correct.

## Setup

1. **Clone the Repository**

   ```bash
   git clone https://github.com/your-username/Password_Management_System.git
   cd Password_Management_System
