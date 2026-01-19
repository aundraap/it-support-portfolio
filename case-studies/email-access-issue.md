# Case Study: User Unable to Access Google Workspace Business Email

## 🧩 Issue Summary
User was unable to access their Google Workspace business email account while attempting to open a recovery link. All login attempts on the Android tablet redirected to the user’s personal Gmail account, preventing access to the correct inbox.

## 🧭 Environment
- **Device:** Android tablet  
- **Operating System:** Android OS  
- **Platform:** Google Workspace (Business Gmail)  
- **Browser/Apps:** Chrome, Gmail App  
- **Accounts on Device:** Personal Gmail (primary), Google Workspace account (secondary)

## 🔍 Symptoms
- Login attempts repeatedly routed to the personal Gmail account  
- User stuck in a **login loop**  
- Recovery link opened the wrong inbox  
- Removing the personal account did not resolve the issue  
- Unable to authenticate into the Workspace account on the tablet

## 🧠 Root Cause
A conflict between the personal Gmail account and the Google Workspace account caused the device to auto‑route authentication to the wrong account. Cached login tokens and stored Google account data forced the login flow to default to the personal Gmail profile, resulting in a persistent login loop.

## 🛠️ Resolution Steps
1. Verified the issue by having the user attempt login from the tablet.  
2. Instructed the user to log out of the personal Gmail account.  
3. Removed the personal Gmail account from the device to eliminate account priority conflicts.  
4. Attempted login again — issue persisted due to cached authentication data.  
5. Directed the user to switch to a **clean device** with no Google accounts signed in.  
6. User accessed the recovery link from the clean device.  
7. Successfully authenticated into the Google Workspace account.  
8. Confirmed access to the business inbox and ensured the recovery process completed.

## ✔️ Outcome
User successfully regained access to the Google Workspace business email account after signing in from a clean device with no cached Google accounts. The recovery link opened correctly, and the user completed the required action without further login loops.

## 🧾 Notes for Documentation
- Android devices prioritize the primary Google account for authentication flows.  
- Cached cookies and tokens can persist even after account removal.  
- When troubleshooting Google Workspace login issues, always test from a clean browser or device.  
- Recommend separating personal and business accounts on mobile devices to avoid future conflicts.
