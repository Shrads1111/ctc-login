# Setup Guide - CareCompass Application

## Prerequisites

You need to install **Node.js** on your Windows machine. Node.js includes npm (Node Package Manager) which is required to install the project dependencies.

### What is Node.js?
Node.js is a JavaScript runtime that allows you to run JavaScript on your computer (not just in a browser). It's required to run the backend server for this application.

---

## Installation Steps

### Step 1: Install Node.js

1. **Download Node.js:**
   - Go to https://nodejs.org/
   - Download the **LTS (Long Term Support)** version for Windows
   - Choose the Windows Installer (.msi) - 64-bit version is recommended

2. **Install Node.js:**
   - Run the downloaded installer (.msi file)
   - Follow the installation wizard (click "Next" through all steps)
   - Make sure "Add to PATH" is checked (it should be by default)
   - Click "Install" and wait for installation to complete
   - Click "Finish" when done

3. **Verify Installation:**
   - Open PowerShell or Command Prompt
   - Type: `node --version`
   - Press Enter - you should see a version number (e.g., v20.x.x)
   - Type: `npm --version`
   - Press Enter - you should see a version number (e.g., 10.x.x)

   ✅ If both commands show version numbers, Node.js is installed correctly!

---

### Step 2: Navigate to Project Directory

1. Open PowerShell or Command Prompt
2. Navigate to the project folder:
   ```powershell
   cd "C:\Users\SWARALI KANGUDE\Downloads\Coders-ctc-main\Coders-ctc-main"
   ```

---

### Step 3: Install Project Dependencies

Run this command to install all required packages (Express, lowdb, body-parser):

```powershell
npm install
```

This will:
- Read the `package.json` file
- Download and install all dependencies listed
- Create/update the `node_modules` folder
- May take 1-2 minutes depending on your internet speed

✅ You'll see "added X packages" when it's done.

---

### Step 4: Start the Server

Run this command:

```powershell
npm start
```

Or alternatively:

```powershell
node server.js
```

You should see:
```
Server started on http://localhost:3000
```

✅ The server is now running!

---

### Step 5: Open the Application

1. Open your web browser (Chrome, Edge, Firefox, etc.)
2. Go to: `http://localhost:3000`
3. You should see the CareCompass application!

---

## Available Pages

- **Main Page:** `http://localhost:3000/index.html`
- **Caregiver View:** `http://localhost:3000/caregiver.html`
- **Doctor View:** `http://localhost:3000/doctor.html`

---

## Troubleshooting

### Problem: "node is not recognized"
- **Solution:** Node.js is not installed or not in PATH. Reinstall Node.js and make sure to check "Add to PATH" during installation.

### Problem: "npm is not recognized"
- **Solution:** Same as above - reinstall Node.js.

### Problem: Port 3000 is already in use
- **Solution:** Either:
  - Close the other application using port 3000, OR
  - Change the port in `server.js` (line 8) to a different number like `3001`

### Problem: "Cannot find module" errors
- **Solution:** Run `npm install` again in the project directory.

### Problem: Server starts but browser shows "Cannot connect"
- **Solution:** Make sure you're using `http://localhost:3000` (not `https://`)

---

## Stopping the Server

To stop the server:
- Press `Ctrl + C` in the PowerShell/Command Prompt window where the server is running

---

## Quick Start Summary

```powershell
# 1. Navigate to project folder
cd "C:\Users\SWARALI KANGUDE\Downloads\Coders-ctc-main\Coders-ctc-main"

# 2. Install dependencies (only needed once)
npm install

# 3. Start the server
npm start

# 4. Open browser to http://localhost:3000
```

---

## What This Application Does

This is a healthcare application called "CareCompass" that allows:
- Caregivers to log patient information (sleep, behavior, food, medication, etc.)
- Doctors/clinicians to view patient data and add notes
- Patient data management with a simple JSON database
- Sharing patient information via shareable links

The application uses:
- **Backend:** Node.js + Express.js server
- **Database:** lowdb (simple JSON file database)
- **Frontend:** HTML, CSS, JavaScript (runs in browser)

---

Need help? Check that Node.js is installed correctly and all dependencies are installed with `npm install`.
