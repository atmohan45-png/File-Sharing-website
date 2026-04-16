# File Sharing Website

## Project Overview

This project is a file sharing web application that allows users to upload, share, and download files securely. The application aims to provide a user-friendly interface for sharing files with friends, family, or colleagues.

## Features
- **User Authentication**: Secure login and registration process using JWT tokens.
- **File Upload**: Users can easily upload files to the server.
- **File Sharing**: Share files via generated links.
- **Download Files**: Users can download files shared with them.
- **Responsive Design**: Works on both desktop and mobile devices.

## Technology Stack
- **Frontend**: HTML, CSS, JavaScript (React)
- **Backend**: Node.js, Express
- **Database**: MongoDB
- **File Storage**: AWS S3 or local storage depending on configuration

## Installation Instructions
1. Clone the repository:
   ```
   git clone https://github.com/atmohan45-png/File-Sharing-website.git
   cd File-Sharing-website
   ```
2. Install dependencies:
   ```
   npm install
   ```
3. Set up environment variables: Create a `.env` file in the root directory and include necessary environment variables such as DB connection string and JWT secret.
4. Run the application:
   ```
   npm start
   ```

## Usage Guidance
1. Open the application in your web browser.
2. Create an account or log in if you already have one.
3. Use the upload feature to add files to your account.
4. Once files are uploaded, use the sharing feature to generate links for your files and share them as needed.
5. Download files shared with you using the provided links.

For more information, feel free to check the wiki or reach out for support.