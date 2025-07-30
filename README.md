# SmartMarket Tobie Admin – Firebase Backend

## 📦 Overview

This project contains the backend for the **SmartMarket Tobie Admin** dashboard. It’s built using **Firebase Functions** with **TypeScript**, and supports automated data scraping and processing for various product categories like **electronics** and **grocery**.

The backend logic includes:
- Headless web scraping via **Puppeteer**
- HTML parsing with **Cheerio** and **jsdom**
- Email notification support using **Nodemailer**
- Cloud Functions for Firebase to handle and deploy logic serverlessly
- Category-specific deployment scripts

## 🧰 Technologies Used

- **Firebase Functions**
- **TypeScript**
- **Puppeteer / Puppeteer Extra (Stealth Plugin)**
- **Cheerio / jsdom**
- **Nodemailer**
- **Firestore (NoSQL database)**
- **Node.js 14**

## 📁 Project Structure

functions/
│
├── src/ # Source code for cloud functions
├── scripts/ # Utility and deployment scripts
├── deploy-*.bat # Scripts for category-specific deployment
├── package.json # NPM dependencies and scripts
├── tsconfig.json # TypeScript configuration
│
├── firebase.json # Firebase project settings
├── firestore.rules # Firestore security rules
├── firestore.indexes.json # Firestore index definitions
└── .firebaserc # Firebase project identifier


## 🚀 Getting Started

### 1. Clone the repository
```bash
git clone https://github.com/your-username/smartmarket-tobie-admin.git
cd smartmarket-tobie-admin/functions

### 2. Install dependencies
npm install

###3. Set up Firebase CLI
Make sure Firebase CLI is installed and you're logged in:

npm install -g firebase-tools
firebase login

### 4. Deploy to Firebase
firebase deploy --only functions

Or for category-specific deployment:
./deploy-grocery.bat
./deploy-electronics.bat
