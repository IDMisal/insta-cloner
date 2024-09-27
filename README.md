# Welcome to My Instagram
***
## Demo
You can check out the demo of this Instagram clone [here](https://insta-cloner.vercel.app/).

## Task
Development of an Instagram clone using ReactJS and Firebase that allows users to create accounts, post images, follow other users, and interact with posts through likes and comments. 
The application should feature modern social media functionalities including filters, direct messaging, and a user-friendly design.

## Description
This Instagram clone aims to replicate key features of the popular social media platform, Instagram. The main features include:

- **Login and Signup**: User authentication with Firebase for secure login and signup.
- **Post Creation**: Users can create posts with text, images (with filters), and videos.
- **Follow and Unfollow**: Ability to follow or unfollow users and see posts from followed accounts.
- **Likes, Comments, and Shares**: Users can like, comment, and share posts.
- **Profile Customization**: Edit profiles, change bio, avatar, and social links.
- **Explore**: Discover trending posts, hashtags, and users.

You can check out the demo of this Instagram clone [here](https://insta-cloner.vercel.app/).

## Firebase Configuration  
To connect the application to Firebase, follow these steps:

    - 1. **Create a Firebase project** on [Firebase Console](https://console.firebase.google.com/).
    - 2. **Add a web app** to the Firebase project and obtain your Firebase configuration object.
    - 4. Enable Authentication: Go to Firebase Console, navigate to Authentication, and enable Email/Password sign-in.
    - 4. Set Up Firestore Database: Create necessary collections for users and posts.
    - 5. Set Up Storage: Use Firebase Storage to upload images and media for posts.
    - 6. Replace the placeholder in your project with the actual Firebase configuration in `firebase.js`:

        // firebase.js
        import { initializeApp } from "firebase/app";
        import { getFirestore } from "firebase/firestore";
        import { getAuth } from "firebase/auth";
        import { getStorage } from "firebase/storage";

        const firebaseConfig = {
        apiKey: "YOUR_API_KEY",
        authDomain: "YOUR_PROJECT_ID.firebaseapp.com",
        projectId: "YOUR_PROJECT_ID",
        storageBucket: "YOUR_PROJECT_ID.appspot.com",
        messagingSenderId: "YOUR_MESSAGING_SENDER_ID",
        appId: "YOUR_APP_ID",
        };

        const app = initializeApp(firebaseConfig);
        const firestore = getFirestore(app);
        const auth = getAuth(app);
        const storage = getStorage(app);

        export { firestore, auth, storage };


## Installation

  1. Clone the repository:
        - `cd my_instagram`  
  2. Install dependencies:
        - `npm install`
  3. Start the development server:
        - `npm run dev`

## Usage
1. Login and Signup: Create an account or log in using your credentials.
2. Create Post: Click the "Create Post" button to add a new post with text or media.
3. Interact with Posts: Like, comment, and share posts.
4. Follow and Unfollow: Search for users, follow them, and see their posts in your feed.
5. Profile Customization: Edit your profile from the profile page by updating your bio and avatar.

 * For production, You can check out the demo of this Instagram clone [here](https://insta-cloner.vercel.app/).
 
 # Issues Encountered
While building this Instagram clone, several challenges arose:

1. Firebase Authentication Setup:
    - Initially, there were issues configuring Firebase Authentication due to an incorrect API key and missing project settings.
    - Solution: Verified Firebase setup and regenerated API keys to match the project.

2. Large Bundle Size Warning (Vite):
    - After building the project, a warning appeared about some chunks being larger than 500 kB.
    - Solution: Implemented code splitting with import() to load certain modules dynamically, optimizing the bundle size.

3. Image Upload with Firebase Storage:
    - There were difficulties managing Firebase Storage when uploading images, particularly handling file size and format restrictions.
    - Solution: Implemented validation checks before upload, ensuring files meet the size and format requirements.
4. React Component Re-Rendering Issues:
    - The profile page and post list had unnecessary re-renders, slowing down the app's performance.
    - Solution: Utilized React.memo() and optimized state management to reduce unnecessary re-renders.

5. Chakra UI Learning Curve:
    - Chakra UI provided a powerful, flexible design system, but initially, there was a learning curve in customizing components to fit the Instagram-like design.

### The Core Team


<span><i>Made at <a href='https://qwasar.io'>Qwasar SV -- Software Engineering School</a></i></span>
<span><img alt='Qwasar SV -- Software Engineering School's Logo' src='https://storage.googleapis.com/qwasar-public/qwasar-logo_50x50.png' width='20px' /></span>
