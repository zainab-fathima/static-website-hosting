# static-website-hosting
Static Task Manager website hosted on AWS S3
## 🌐 Project Name: Task Manager Web App

This project demonstrates how to host a *static website* using *Amazon S3. The hosted website is a simple **task manager* built with HTML, CSS, and JavaScript.

---

## 📁 Project Files

- index.html – Contains the code for the task manager
- screenshots/ – Images of AWS S3 setup and site
- README.md – Project documentation

---

## 💻 Website Features

- Add and display tasks
- Mark tasks as completed (strike-through)
- Delete tasks
- Clean, responsive user interface

---

## 🚀 Hosting Steps on AWS S3

### 1. *Create a Bucket*
- Go to AWS Console → S3 → Create bucket
- Name it uniquely (e.g. zainab-task-manager)
- Uncheck “Block all public access”

### 2. *Enable Static Hosting*
- Open the bucket → Properties
- Enable *Static website hosting*
- Set index document to index.html

### 3. *Upload Files*
- Upload index.html

### 4. *Make Files Public*
- Add this bucket policy:

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "PublicReadGetObject",
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::your-bucket-name/*"
    }
  ]
}
