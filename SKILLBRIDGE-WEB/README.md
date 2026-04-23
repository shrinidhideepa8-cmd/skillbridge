# SkillBridge – Freelancer Platform

> A full-stack freelancer marketplace I designed and built, connecting skilled professionals with clients.

🔗 **Live Demo:** [skillbridge-web.netlify.app](https://skillbridge-web.netlify.app)

---

## 💡 About This Project

I built SkillBridge to solve a real problem — skilled freelancers in India struggle to find clients, and companies struggle to find verified talent. This platform bridges that gap.

I designed the full feature set, set up the Firebase backend, and deployed it live.

---

## ✨ Features

- 👤 Freelancer profile creation — skills, bio, portfolio, availability
- 💼 Job posting system for clients
- 🔍 Search & filter freelancers by category and skill
- 💬 Real-time messaging between clients and freelancers
- ⭐ Review and rating system
- 📋 Proposal submission workflow
- 🔐 User authentication (Sign up as client or freelancer)

---

## 🛠 Tech Stack

| Technology | Purpose |
|---|---|
| React 18 | Frontend UI |
| Firebase Auth | User authentication |
| Firebase Firestore | Real-time database |
| Netlify | Deployment & hosting |
| JavaScript (ES6+) | App logic |
| CSS3 | Styling |

---

## 🚀 Getting Started

1. Clone the repo
2. Open `index.html` in your browser — works instantly, no build step needed
3. To connect your own Firebase: see setup below

---

## 🔧 Firebase Setup

1. Create a project at [console.firebase.google.com](https://console.firebase.google.com)
2. Enable **Email/Password Authentication**
3. Create a **Firestore Database** in test mode
4. Copy your config into `index.html`:

```js
const FIREBASE_CONFIG = {
  apiKey: "YOUR_API_KEY",
  authDomain: "YOUR_PROJECT.firebaseapp.com",
  projectId: "YOUR_PROJECT_ID",
  ...
};
```

---

## 📁 Firestore Data Structure

```
/users/{userId}         → profile info
/freelancers/{id}       → freelancer listings
/jobs/{jobId}           → client job postings
/messages/{chatId}      → real-time chat
/reviews/{freelancerId} → ratings & reviews
```

---

## 🎯 What I Learned

- Integrating Firebase Auth and Firestore into a React app
- Building real-time features with Firestore listeners
- Deploying a production web app on Netlify
- Designing a multi-role platform (client vs freelancer)

---

## 👤 Author

**Shrinidhi S.K**
[LinkedIn](www.linkedin.com/in/shrinidhi-s-k-760b6a323?utmsource =shareutmcampaign = shareviautmcontent = prof
ileutmmedium = iosapp) · [GitHub](https://github.com/shrinidhideepa8-cmd)
