# Vinyl Record Tracker - Cloud Sync + Hosting

This project now supports:

- Local mode (works offline in browser localStorage)
- Cloud sync mode via Firebase Authentication + Firestore
- Hosting via Firebase Hosting so you can open the same app URL on any device

## 1) Create Firebase project

1. Go to Firebase Console and create a project.
2. Add a Web App in Project Settings.
3. Copy the Web App config values.
4. Enable Authentication -> Sign-in method -> Google.
5. Enable Firestore Database (start in production mode).

## 2) Add Firebase config to the app

Open [index.html](index.html) and fill the `firebaseConfig` object near the top of the JavaScript module.

## 3) Set your Firebase project id

Open [.firebaserc](.firebaserc) and replace:

- `your-firebase-project-id`

with your real project id.

## 4) Deploy security rules + hosting

Install the Firebase CLI if needed:

```bash
npm install -g firebase-tools
```

Login and deploy:

```bash
firebase login
firebase deploy
```

After deploy, Firebase prints a Hosting URL. Open that URL on any device and sign in with the same Google account to access/edit the same records.

## Data model

Each signed-in user stores records in:

- Firestore collection: `collections`
- Document id: Firebase Auth `uid`

Rules in [firestore.rules](firestore.rules) ensure users can only read/write their own document.
