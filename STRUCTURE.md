# 📂 MedGuardian Project Structure & Architecture

This document outlines the file structure and architecture of the **MedGuardian** mobile application.

## 🛠️ Technology Stack & Core Summary
* **App Type:** React Native Mobile Application (Cross-platform for Android & iOS)
* **Programming Language:** JavaScript / JSX
* **Data Management:** Local Storage (AsyncStorage / Local database mechanism without external backend)

---

## 📁 Root Directory Files & Folders

* **android/:** Contains the native Android project files and Gradle configurations (`build.gradle`, `settings.gradle`, `gradlew`, `app/`, etc.).
* **ios/:** Contains the native iOS project files, Xcode configurations (`MedGuardian.xcodeproj`), environment configs (`.xcode.env`), and CocoaPods dependencies (`Podfile`).
* **src/:** Main source folder for all React Native code, components, routes, features, hooks, and store.
* **App.jsx:** Main entry point that loads the app.
* **app.json:** Application configuration settings (name, version, etc.).
* **index.js:** Starts and registers the app.
* **babel.config.js:** Configures Babel for JavaScript transpiling.
* **jest.config.js:** Configuration file for unit testing.
* **metro.config.js:** Metro bundler settings for the React Native app.
* **package.json:** Manages dependencies, scripts, and app metadata.
* **tsconfig.json:** TypeScript configuration (if applicable).
* **README.md:** Documentation and instructions about the project.
* **Configuration Files:** `.eslintrc.js`, `.prettierrc.js`, `.gitignore` (for code formatting and git version control).

---

## 🗂️ Inside the `src/` Folder

* **AppLogo.jsx:** A reusable component to show the app's logo.
* **index.js:** Centralized export file for components.
* **routes/ (Navigation):**
  * `AppNavigation.jsx`: Main app navigation structure.
  * `CustomDrawerContent.jsx`: Custom UI for drawer navigation.
  * `DrawerNavigation.jsx`: Drawer navigator setup.
  * `UserDrawerHeader.jsx`: Custom header inside drawer.
  * `index.js`: Central export of navigation configs.
* **features / modules:**
  * `auth/`: Handles authentication (login, signup).
  * `health-vitals/`: Manages health stats like blood pressure and blood sugar.
  * `water-intake/`: Tracks and manages water intake.
* **hooks/:**
  * `useScreenTitle.js`: Custom hook for managing dynamic screen titles.
  * `index.js`: Central export for hooks.
* **store/:**
  * Manages global state (e.g., Zustand) and handles data persistence via local storage, acting as a local database solution without requiring an external backend server.
