# ConnectPro

A full-stack professional networking platform built with React, Redux Toolkit, and Firebase, enabling users to authenticate, create posts, and interact with a real-time social feed.

![HomeGif](https://github.com/MDbrosev/LinkedIn/blob/master/src/images/LinkedIn.gif)

## Overview

ConnectPro simulates a modern professional networking experience, allowing users to build a profile, share updates, and view a dynamic feed powered by cloud-based data synchronization.
This project demonstrates real-world frontend architecture patterns, including centralized state management, authentication flows, and real-time data handling.

## Features
```text
🔐 Authentication
Firebase Authentication (email/password)
Persistent user sessions via onAuthStateChanged

🧠 State Management
Centralized state using Redux Toolkit
Auth and user state managed globally

📰 Real-Time Feed
Posts stored in Firebase Firestore
Live updates using onSnapshot
Animated UI updates with react-flip-move

✍️ Post Creation
Users can create and submit posts
Immediate feed updates after submission

🎨 Modern UI
Material UI components
Responsive layout with modular components
Clean separation of concerns (Header, Feed, Sidebar, Widgets)
```

## Tech Stack
Frontend
```text
React (Functional Components + Hooks)
Redux Toolkit
Material UI
```
Backend / Services
```text
Firebase Authentication
Firebase Firestore (real-time database)
```
Other
```text
React Flip Move (animations)
```

## Architecture

The project follows a feature-based structure to promote scalability and maintainability:
```text
src/
├── app/              # Redux store configuration
├── features/
│   ├── auth/         # Authentication logic and components
│   └── posts/        # Feed and post management
├── components/       # UI components (Header, Sidebar, Widgets)
├── firebase.js       # Firebase configuration
└── App.js            # Root application logic
```

## Key Design Decisions
```text
Redux Toolkit used for predictable global state management
Firebase chosen for rapid backend integration and real-time capabilities
Feature-based folder structure for scalability and separation of concerns
Real-time listeners (onSnapshot) to simulate production-grade feed updates
```

## Getting Started

### Prerequisites
```text
Node.js (v16+ recommended)
Firebase project (Auth + Firestore enabled)
```

### Installation

```text
git clone https://github.com/yosephhasson/ConnectPro.git
cd ConnectPro
npm install
```

### Environment Setup

Create a Firebase project and update your configuration in:
```text
// src/firebase.js
```

Add your Firebase config:
```javascript
const firebaseConfig = {
  apiKey: "YOUR_API_KEY",
  authDomain: "YOUR_DOMAIN",
  projectId: "YOUR_PROJECT_ID",
  storageBucket: "YOUR_BUCKET",
  messagingSenderId: "YOUR_SENDER_ID",
  appId: "YOUR_APP_ID"
};
```

### Run the App
```bash
npm start
```

### How It Works
```text
Users authenticate via Firebase Auth
Auth state is stored globally using Redux
Posts are stored in Firestore
The feed listens for real-time updates using onSnapshot
UI updates dynamically when new posts are added
```

### Future Improvements
```text
Add comments and reactions system
Implement user connections / networking graph
Introduce backend API layer (Node.js or .NET)
Add notifications system
Improve error handling and logging
Upgrade to latest React / build tooling
```

### Disclaimer
```text
This project is intended for demonstration and portfolio purposes. It simulates core features of a professional networking platform and is not affiliated with LinkedIn.
```

