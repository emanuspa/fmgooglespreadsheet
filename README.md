Medium link to the article:
https://medium.com/@emaspa/connect-filemaker-to-google-sheets-a-step-by-step-guide-for-real-time-data-sync-df8b051d3b91

# fmgooglespreadsheet
---

🚀 Connect FileMaker to Google Sheets: A Step-by-Step Guide for Real-Time Data Sync
Have you ever dreamed of syncing your FileMaker data with Google Sheets in real time? Maybe to share reports with your team, push form submissions to a cloud spreadsheet, or simply automate your weekly sales exports?
You're in the right place.
 In this article, we'll learn how to integrate FileMaker with the Google Sheets API - even if you're not a Google Cloud expert (yet!).
We'll go step-by-step, and at the end, I'll give you a ready-to-use FileMaker file. You'll just need to plug in a few values like your client ID and refresh token, and you'll be up and running in no time. 🎉
🎯 Real-life use case
Let's say you run a small company and use FileMaker to manage your orders. Every day, your staff needs to update a shared Google Sheet with the latest orders for accounting. Doing it manually is slow and boring.
With this integration, FileMaker can send data directly to your spreadsheet with a click. You can even clear the sheet before writing new values, or retrieve and display data back into FileMaker.
🛠️ What We'll Build
We'll:
Connect FileMaker to the Google Sheets API using OAuth2
Automatically refresh tokens
Read, write, and clear cell ranges using batch API calls
Make it all super user-friendly with a guided dashboard inside the FileMaker file

🧩 What You'll Need
Before we dive in, here's what you'll need to enter into the FileMaker file:
Your Client ID
Your Client Secret
Your Refresh Token
Your Google Sheet ID
Your Sheet Name (or Tab name)

We'll show you how to get all of this step-by-step.

---

🔐 Step 1: Create a Google Cloud Project
Go to console.cloud.google.com
Sign in with your Google account
Click "Select project" > New project
Give it a name like FileMaker Integration
Create it!

🔧 Step 2: Enable the Sheets API
In the left menu, go to API & Services > Library
Search for Google Sheets API
Click it and hit Enable

🗝️ Step 3: Create OAuth Credentials
Go to API & Services > Credentials
Click "+ Create Credentials" > OAuth client ID
If asked, configure the OAuth consent screen
Choose Web application
Add the redirect URI:
 https://developers.google.com/oauthplayground
Save and copy the Client ID and Client Secret

🔁 Step 4: Get the Refresh Token
Open OAuth Playground
Click the ⚙️ icon and check "Use your own credentials"
Paste your Client ID and Secret
In the left panel, select this scope:
 https://www.googleapis.com/auth/spreadsheets
Click Authorize APIs and sign in
Click Exchange authorization code for tokens
Save the Refresh Token somewhere safe

📄 Step 5: Grab Your Sheet Info
Open your Google Sheet
Copy the Spreadsheet ID from the URL
 (it's the long string between /d/ and /edit)
Note the name of the Sheet (tab) you want to use

🧪 Step 6: Open the FileMaker File
Once you download the sample file (link below), open it and go to the Setup screen. Paste in:
Your Client ID
Your Client Secret
Your Refresh Token
Your Spreadsheet ID
Your Sheet Name

Now click one of the buttons and watch the magic happen. ✨
You'll be able to:
Fetch spreadsheet data
Clear cell ranges
Write values from FileMaker to Sheets

Everything happens via secure API calls using native FileMaker scripts and Insert from URL.

---

💡 What You Can Do Next
Once everything works:
Customize the layout for your own data
Schedule automatic updates using FileMaker Server
Share your spreadsheet with your team or clients

🙌 Let's Wrap Up
I hope this guide helped you unlock the power of Google Sheets and FileMaker together. If you've got questions, ideas, or want to share how you're using this integration, I'd love to hear from you, please drop a comment below or share your experience!.
Thanks for reading, and happy building!
