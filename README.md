# TikTok Clone NextJs 13 / (tiktok-clone-nextjs)

### Learn how to build this!

If you'd like a step-by-step guide on how to build this just **CLICK THE IMAGE BELOW**

[![GO TO JOHN WEEKS DEV TUTORIAL VIDEOS](https://github.com/John-Weeks-Dev/ebay-clone/assets/108229029/1d1d9f20-0f5b-4d00-8d5a-9aca0d3e414c)](https://www.youtube.com/watch?v=LtPYuFhYf1w)

Come and check out my YOUTUBE channel for lots more tutorials -> https://www.youtube.com/@johnweeksdev

**LIKE**, **SUBSCRIBE**, and **SMASH THE NOTIFICATION BELL**!!!

## App Setup (localhost)

```
git clone https://github.com/John-Weeks-Dev/tiktok-clone-nextjs.git

cp .env.example .env
```

You'll have to set up an AppWrite account, and then add all of the details into your .env file.

## AppWrite Schema

Database Name: tiktok-clone

Database Collections:

    Profile:
        Document ID: String
        image: String
        bio: String
        user_id: String
        name: String
        
    Profile Indexes: KEY: user_id, TYPE: key, ATTRIBUTE: user_id, ASC/DESC: asc
    
    Profile Settings (Update Permissions):
        Add Role = All guests / Read
        Add Role = All users / Create, Read, Update, Delete

    Post:
        Document ID: String
        user_id: String
        video_url: String
        text: String
        created_at: String
        
    Post Indexes: KEY: user_id, TYPE: key, ATTRIBUTE: user_id, ASC/DESC: asc

    Profile Settings (Update Permissions):
        Add Role = All guests / Read
        Add Role = All users / Create, Read, Update, Delete

    Like:
        Document ID: String
        user_id: String
        post_id: String

    Like Indexes: 
        KEY: user_id, TYPE: key, ATTRIBUTE: user_id, ASC/DESC: asc
        KEY: id, TYPE: unique, ATTRIBUTE: $id, ASC/DESC: asc
        KEY: post_id, TYPE: key, ATTRIBUTE: post_id, ASC/DESC: asc

    Like Settings (Update Permissions):
        Add Role = All guests / Read
        Add Role = All users / Create, Read, Update, Delete

    Comment:
        Document ID: String
        user_id: String
        post_id: String
        text: String
        created_at: String
        
    Comment Indexes: KEY: post_id, TYPE: key, ATTRIBUTE: post_id, ASC/DESC: asc

    Comment Settings (Update Permissions):
        Add Role = All guests / Read
        Add Role = All users / Create, Read, Update, Delete


Once you've connected your application to AppWrite. Run the commands.
    
```
npm i

npm run dev
```

You should be good to go! If you need any more help, take a look at the tutorial video by clicking the image above.
