# aws-s3-static-website


# 🌐 Host a Website on Amazon S3

A step-by-step project to host a static website using **Amazon S3** — no servers, no backend, just pure cloud hosting.

---

## 📌 Project Overview

This project walks through hosting a fully functional static website on AWS S3 using the **Static Website Hosting** feature. By the end, the website is live on a public URL powered entirely by Amazon S3.

**Difficulty:** Beginner  
**Cloud Provider:** AWS  
**Service Used:** Amazon S3  
**Project Source:** (http://aws-s3-website-145770591134-ap-south-1-an.s3-website.ap-south-1.amazonaws.com/)

---

## 🗂️ Table of Contents

- [What You'll Learn]
- [Prerequisites]
- [Architecture]
- [Step-by-Step Setup]
  - [Step 1 — Create an S3 Bucket]
  - [Step 2 — Upload Website Files]
  - [Step 3 — Enable Static Website Hosting]
  - [Step 4 — Access Your Live Website]
- [Project Files]
- [Common Errors & Fixes]
- [What's Next]

---

## 🎯 What You'll Learn

- How to create and configure an **Amazon S3 bucket**
- How to upload HTML/CSS files to S3
- How to enable **Static Website Hosting** on S3
- How to get a **live public URL** for your website

---

## ✅ Prerequisites

Before starting, make sure you have:

- [ ] An **AWS Account** (free tier works fine)
- [ ] Basic knowledge of HTML
- [ ] A simple `index.html` file ready to upload

---

## 🏗️ Architecture

```
User (Browser)
      │
      ▼
Amazon S3 Bucket
  ├── Static Website Hosting: Enabled
  ├── index.html  (main page)
      │
      ▼
Public S3 Website URL
"http://aws-s3-website-145770591134-ap-south-1-an.s3-website.ap-south-1.amazonaws.com/"
---

## 🛠️ Step-by-Step Setup

### Step 1 — Create an S3 Bucket

1. Go to **AWS Console** → Search for **S3** → Click **Create bucket**
2. Enter a unique **Bucket name** (example: `my-website-jana-2024`)
3. Choose your **AWS Region** (pick the one closest to you)
4. Under **Block Public Access settings** → **Uncheck** "Block all public access"
5. Acknowledge the warning checkbox
6. Click **Create bucket**

> ⚠️ Bucket names must be globally unique across all of AWS.

---

### Step 2 — Upload Website Files

1. Click on your newly created bucket
2. Click **Upload** → **Add files**
3. Upload your `index.html` and `error.html` files
4. Click **Upload**


### Step 3 — Enable Static Website Hosting

1. Go to your bucket → Click **Properties** tab
2. Scroll down to **Static website hosting** → Click **Edit**
3. Select **Enable**
4. Set **Index document** → `index.html`
5. Click **Save changes**

---

4. Click **Save changes**

> 🔐 This policy allows anyone on the internet to **read** your files. It does not allow editing or deleting.

---

### Step 5 — Access Your Live Website

1. Go to your bucket → **Properties** tab
2. Scroll to **Static website hosting**
3. Copy the **Bucket website endpoint** URL

It will look like:
```
http://aws-s3-website-145770591134-ap-south-1-an.s3-website.ap-south-1.amazonaws.com/
```

4. Open it in your browser — your website is **live!** 🎉

---

## 📁 Project Files

```
├── index.html      # Main homepage

```

---

## ❌ Common Errors & Fixes

| Error | Cause | Fix |
|---|---|---|
| 403 Forbidden | Bucket policy not set | Add the public read bucket policy |
| 404 Not Found | index.html not uploaded or wrong name | Re-upload and check filename spelling |
| AccessDenied on upload | Permissions issue | Check IAM user permissions |
| Bucket name taken | Name not unique | Add numbers or your name to the bucket name |

---

## 🚀 What's Next

Once your site is live, you can level up with:

- 🔒 **Add HTTPS** — Use Amazon CloudFront + ACM Certificate
- 🌍 **Custom Domain** — Connect via Route 53
- ⚡ **Faster Load Times** — Use CloudFront as a CDN in front of S3
- 📊 **Track Visitors** — Enable S3 Server Access Logging

---

## 🙋 Author

**Jana**  

## 📄 License

This project is for learning purposes. Feel free to fork and modify!
