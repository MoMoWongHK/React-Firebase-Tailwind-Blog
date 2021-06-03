
# React-Firebase-Tailwind-Blog
A complete website with **SEO friendly ** , **CMS**,  **Serverless** and **One click deployment**.
The website is a public repository by [childnoder.com](https://childnoder.com "childnoder.com"). 
[Contact](mailto:momo@childnoder.com) me for freelance job😊  .

![](https://childnoder.com/icons-192.png)

# Features

- Using [Tailwindcss framework](https://tailwindcss.com/ "Tailwindcss framework") 
--  lighter bundle size.
--  fast FCP (First Contentful Paint).
--  low TBT (Total Blocking Time) .

- Good Internationalization in SEO
-- using [React-I18next](https://react.i18next.com/ "React-I18next")

- Totally Firebase
-- firebase hosting, firebase functions, firebase firestore

- Impletmented Prerendering in cloud functions
-- using [prerender.io](https://prerender.io "prerender.io")

- And more...

# Installation
## Step 1: Git Clone
    git clone https://github.com/MoMoWongHK/React-Firebase-Tailwind-Blog

## Step 2: Install required package
Please execute the following command in your terminal

    //install required package to your main app
	npm install
	
    //install required package to your local server in /server
    cd server
    npm install
	
    //install required package to your firebase cloud functions
	cd ../
    cd functions
    npm install
	
## Step 3: Create new Firebase project and Setup Firebase
### Step 3.1: Download your Firebase Admin SDK Service Account Key
After you create new Firebase project, you have to download your Firebase service AccountKey.json in Firebase Console

[ Firebase Console > Project Setting > Server Account]

> Save the json file to /server/YOUR_SERVICEACCOUNTKEY.json

### Step 3.2: Turn On Google and Email as the Login Provider
[ Firebase Console > Authentication >Sign-in method ]

### Step 3.3: Setup firebase firestore database
[ Firebase Console > Cloud Firestore ]

###  Step 3.4: [OPTIONAL] Upgrade your firebase project plan to Blaze
> :warning: **YOU CANNOT ENJOY YOUR SSR (Server Side Rendering )**: if your plan is Spark.

## Step 4: Import Your Service Account Key in /server/server.js
server.js line 2:

    const serviceAccount = require("./YOUR_SERVICEACCOUNTKEY.json");
	
## Step 5: Change your Firebase Config in /src/Config/firebase.js
you can find your config in your firebase console
[ Firebase Console > Project Setting]

    const firebaseConfig = {
        apiKey: "YOUR_API_KEY",
        authDomain: "YOUR_AUTH_DOMAIN",
        databaseURL: "YOUR_DATABASE_URL",
        projectId: "YOUR_PROJECT_ID",
        storageBucket: "YOUR_STORAGE_BUCKET",
        messagingSenderId: "YOUR_MESSAGING_SENDER_ID",
        appId: "YOUR_APP_ID"
    };

## Step 6: Setup your Admin Role
### Step 6.1: start your web server

    npm run start
	
### Step 6.2: Login using Google Account
go to localhost:3000/en/login and login.

### Step 6.3: Copy your Firebase UID in Firebase Console
[ Firebase Console > Authentication  ]

### Step 6.4: Replace your UID in /server/server.js line 27

### Step 6.5: start your local backedn server

    cd server
    npm run server
	

### Step 6.6: Visit localhost:4000/setAdmin 

### Step 6.7: Logout in your localhost website and login again

# Extra
## Add Algolia Into Your Firebase Project
[-part one- ](https://clipversity.com/article/Add-algolia-into-your-firebase-project-MEHFo0sv-ENT34E79KX/en "part one ")
[-part two-](https://clipversity.com/article/Add-algolia-into-your-firebase-project---2-MFWOcREikfu__vJvb-p/en "part two")
[-part three (backend search)-](https://clipversity.com/article/Add-algolia-into-your-firebase-project-3-backend-search-MFZl67pT53Dx60PBfmO/en "part three (backend search)")
[![algolia firebase](https://firebasestorage.googleapis.com/v0/b/clipversity-firebase.appspot.com/o/ArticleImage%2FAdd-algolia-into-your-firebase-project-MEHFo0sv-ENT34E79KX%2F-MFGxkw5qkxnCQ9pHLaR?alt=media&token=f1867395-5735-4775-a0ea-2483a9d976b6 "algolia firebase")](https://clipversity.com/article/Add-algolia-into-your-firebase-project-MEHFo0sv-ENT34E79KX/en "algolia firebase")
