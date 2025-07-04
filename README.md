# 🌐 SocialEcho

> A modern social networking platform with built-in **AI-driven content moderation** and **context-based authentication** for enhanced security and user experience.

---

## 📚 Table of Contents

- [📌 Project Overview](#-project-overview)
- [🚀 Key Features](#-key-features)
- [🛠️ Technologies Used](#-technologies-used)

## 📌 Project Overview

**SocialEcho** is a full-stack social media application developed using the **MERN stack** (MongoDB, Express.js, React.js, and Node.js). The platform provides essential features of a modern social network, along with:

- 🔐 **Context-aware login authentication**
- 🧠 **Automated content moderation using NLP APIs**
- 🛡️ **Role-based access control** for admins, moderators, and users

### 🔐 Context-Based Authentication

To strengthen account security, the platform tracks the user's **device information**, **IP address**, and **geographic location**. This data is:

- Encrypted using **AES**
- Stored securely in the database
- Used to detect and respond to **suspicious login activity**

When a suspicious login occurs:
- The user is immediately notified via email
- Verification is required to continue access

Users can also **view and manage** their trusted devices through the platform.

### 🧠 Automated Content Moderation

All user-generated content is filtered using **Natural Language Processing (NLP)** APIs to ensure it complies with community guidelines.

Integrated APIs include:

| API                        | Purpose                               |
|----------------------------|----------------------------------------|
| 🧠 **Perspective API**     | Detects spam, toxicity, profanity, etc. |
| 🧠 **TextRazor API**       | Categorizes and analyzes content       |
| 🧠 **Hugging Face API**    | BART-Large MNLI model for classification |

Additionally, a **Flask-based API** replicates Hugging Face behavior using **PyTorch** and BART for zero-shot text classification.

> The system supports dynamic switching between APIs or disabling moderation services as needed—without affecting the core application.

Users may also **report content**, triggering a **manual moderation process** by assigned moderators.

### 👥 User Roles

1. **Admin**  
   - System-wide privileges: manage users, communities, and moderation settings
2. **Moderator**  
   - Community-level permissions: review and manage reported content
3. **General User**  
   - Standard access: create content, interact with others, follow/unfollow

---

## 🚀 Key Features

✅ JWT-based Authentication and Authorization  
✅ Full User Profile Management  
✅ Post Creation, Commenting, and Reactions  
✅ Follow/Unfollow Functionality  
✅ AI-Powered Content Moderation  
✅ Device and Login Context Management  
✅ Admin and Moderator Dashboards  
✅ Email Alerts for Suspicious Logins  
✅ Moderator Auto-Assignment by Email Domain  
✅ Flask API for Custom Text Classification  
✅ Azure Blob Storage for File Uploads

---

## 🛠️ Technologies Used

**Frontend:**
- ⚛️ React.js
- 📦 Redux
- 🎨 Tailwind CSS

**Backend:**
- 🧩 Node.js + Express.js
- 🛢️ MongoDB
- 🔐 Passport.js (JWT)
- 🛡️ Crypto-js
- 📧 Nodemailer

**APIs and Services:**
- 🔍 Perspective API
- 🧠 TextRazor API
- 🤖 Hugging Face Transformers
- 🐍 Flask (BART model with PyTorch)
- ☁️ Azure Blob Storage


### 👑 Admin

- Visit: `http://localhost:3000/admin`
- Use `admin_tool.sh` to set up the first admin
- Admins can:
  - Manage communities
  - Assign moderators
  - Enable/disable moderation APIs
  - Oversee platform activity

### 🛡️ Moderator

- Use an email ending in `@mod.socialecho.com` to register
- Moderators are automatically assigned based on email domain
- From the dashboard, moderators can:
  - Review flagged posts
  - Moderate community discussions

---

### 🙋 General Users

- Can register and log in like standard social platforms
- Can:
  - Create and share posts
  - Like and comment on content
  - Follow/unfollow other users
  - Report content violating guidelines

🔗 **Connect, Share, and Moderate Smarter — with SocialEcho**
