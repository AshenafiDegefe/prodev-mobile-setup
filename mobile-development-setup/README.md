## Project Setup and Environment

This section details the necessary steps and tools required to set up and run this project locally.
### 1. Prerequisites
Make sure you have the following installed on your development machine:
**Node.js:** (LTS recommended)
**npm** or **Yarn** (npm comes bundled with Node.js)
**Expo CLI:** Installed globally or used via npx.
**A Mobile Device or Emulator/Simulator:** To run the application.
### 2. Expo Go Installation
To view and run the application on a physical device, you need the Expo Go app installed.PlatformInstallation SourceNotesAndroidGoogle Play StoreUsed a Samsung Galaxy S23 (Android 14) for testing.iOSApple App StoreTested on an iPhone 14 (iOS 17.2).
### 3. Project Initialization and Run
#### 1. Clone the Repository:
git clone [Your Repository URL]
cd [your-project-name]
#### 2. Install Dependencies:
npm install
 OR
yarn install
#### 3. Start the Development Server:
npx expo start
This command will launch the Metro bundler and display a **QR code** in your terminal.
### 4. Connect with Expo Go:
**Android:** Open the Expo Go app and tap **"Scan QR Code"**.
**iOS:** Use your phone's default **Camera app** to scan the QR code.
The application should build and load automatically within the Expo Go app.

## ⚠️ Challenges and Troubleshooting Log
This section documents any specific challenges encountered during the setup and how they were resolved.
### Challenge 1: Connection Timeout
**Description:** When attempting to scan the QR code, the connection timed out and the app failed to load. The terminal showed the connection mode as LAN.
**Resolution:** The development machine and the mobile device were on different subnets despite being on the same Wi-Fi network. Switched the connection mode from LAN to Tunnel by pressing t in the Metro bundler terminal window. The Tunnel connection worked immediately.
### Challenge 2: SDK Version Mismatch
**Description:** After running npx expo start, the Expo Go app displayed an error stating, "Project uses SDK XX, but the installed Expo Go is for SDK YY."
**Resolution:** Updated the global Expo CLI using npm install -g expo-cli and ensured the expo dependency in package.json was aligned with the latest stable version (e.g., SDK 50). Restarted the server.
### Challenge 3: Watchman Error on macOS
**Description:** On a macOS machine, the server start failed with an error mentioning Watchman.
**Resolution:** Installed/updated Watchman via Homebrew: brew install watchman. Then ran npx expo start again, which resolved the issue.