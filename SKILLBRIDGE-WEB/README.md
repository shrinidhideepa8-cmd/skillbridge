# SkillBridge – Freelancer Platform

A full-featured freelancer marketplace web app built with React + Firebase.

---

## Features
- Freelancer profile creation with skills, bio, portfolio, availability
- Service listings and job posting system
- Browse & filter freelancers by category/skill
- Real-time messaging between clients and freelancers
- Review and rating system
- Proposal submission workflow
- User authentication (Sign up as client or freelancer)

---

## Quick Start (Local)

1. Open `index.html` directly in your browser — it runs without any server.
2. All features work with the built-in sample data.

---

## Connect Firebase (for real users & real-time data)

### Step 1 – Create a Firebase project
1. Go to https://console.firebase.google.com
2. Click **Add project** → name it (e.g. `skillbridge-app`)
3. Disable Google Analytics if you don't need it → **Create project**

### Step 2 – Enable Authentication
1. In Firebase Console → **Build → Authentication → Get Started**
2. Enable **Email/Password** provider

### Step 3 – Enable Firestore Database
1. **Build → Firestore Database → Create database**
2. Start in **Test mode** (change rules before going live)

### Step 4 – Get your config
1. Go to **Project Settings** (gear icon)
2. Under **Your apps**, click **</>** (Web)
3. Register your app → copy the `firebaseConfig` object

### Step 5 – Paste config into index.html
Find this block near the top of `index.html` and replace with your values:

```js
const FIREBASE_CONFIG = {
  apiKey: "YOUR_API_KEY",
  authDomain: "YOUR_PROJECT.firebaseapp.com",
  projectId: "YOUR_PROJECT_ID",
  storageBucket: "YOUR_PROJECT.appspot.com",
  messagingSenderId: "YOUR_SENDER_ID",
  appId: "YOUR_APP_ID"
};
```

### Step 6 – Add Firebase SDK
Add these lines before the closing `</head>` tag:

```html
<script src="https://www.gstatic.com/firebasejs/10.8.0/firebase-app-compat.js"></script>
<script src="https://www.gstatic.com/firebasejs/10.8.0/firebase-auth-compat.js"></script>
<script src="https://www.gstatic.com/firebasejs/10.8.0/firebase-firestore-compat.js"></script>
```

Then replace the `STORE` simulation with actual Firestore calls.

---

## Deploy to Firebase Hosting (Free)

```bash
# Install Firebase CLI
npm install -g firebase-tools

# Login
firebase login

# Init hosting in your project folder
firebase init hosting

# Deploy
firebase deploy
```

Your app will be live at `https://YOUR_PROJECT.web.app` 🎉

---

## Deploy to Netlify (Easiest Option)

1. Go to https://netlify.com → **Add new site → Deploy manually**
2. Drag and drop the `freelance-platform` folder
3. Your site goes live instantly with a free URL

---

## Firestore Data Structure (for Firebase integration)

```
/users/{userId}
  name, email, role, title, category, skills[], bio, rate, location, portfolio[]

/jobs/{jobId}
  title, category, budget, type, duration, description, skills[], clientId, clientName, posted

/messages/{chatId}/messages/{msgId}
  from, text, timestamp

/reviews/{freelancerId}/items/{reviewId}
  clientName, rating, text, date
```

---

## Customization Tips

- **Brand name**: Search for "SkillBridge" and replace with your app name
- **Categories**: Edit the categories array in each page component
- **Colors**: Change `--brand: #1a56db` in the CSS `:root` to your brand color
- **Currency**: Replace `₹` with your local currency symbol

---

## Tech Stack
- React 18 (via CDN, no build step needed)
- Firebase (Auth + Firestore + Hosting)
- Pure CSS (no Tailwind or component library dependency)
- Google Fonts: DM Sans + DM Serif Display
