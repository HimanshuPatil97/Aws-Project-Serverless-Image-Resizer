# Serverless Image Resizer using AWS Lambda and S3

## 📌 Project Overview

This project demonstrates a serverless image processing system using AWS Lambda and Amazon S3.

Whenever an image is uploaded to the source S3 bucket, AWS Lambda is automatically triggered to resize the image and store the resized image in another S3 bucket.

---

## 🧰 AWS Services Used

- AWS Lambda
- Amazon S3
- CloudWatch
- IAM Roles

---

## 🚀 Implementation Steps

### 1. Create S3 Buckets

Created two S3 buckets:
- Source Bucket (Upload Images)
- Destination Bucket (Store Resized Images)

---

### 2. Create Lambda Function

Created a Lambda function using Python runtime.

Function Name:
- image-resizer

---

### 3. Add Pillow Library

Used the Pillow library for image processing and resizing operations through a Lambda Layer.

---

### 4. Implement Lambda Code

The Lambda function:
- Downloads uploaded image from source bucket
- Resizes the image
- Uploads resized image to destination bucket

Example functionality:

```python
image = Image.open(download_path)
image = image.resize((200, 200))
```

---

### 5. Configure IAM Permissions

Attached S3 access permissions to the Lambda execution role.

---

### 6. Configure S3 Trigger

Configured the source S3 bucket to automatically trigger the Lambda function whenever a new image is uploaded.

---

### 7. Test the Project

Uploaded image files to the source bucket.

The Lambda function automatically processed and resized the images.

---

## 🎯 Features

- Serverless Architecture
- Automatic Image Processing
- Event-Driven Workflow
- Scalable Image Resizing
- Fully Automated Processing

---

## 📸 Output

Original images uploaded to the source bucket were automatically resized and stored in the destination bucket.

---

## 🎓 Learning Outcomes

- AWS Lambda automation
- S3 event triggers
- Serverless computing
- Image processing using Pillow
- IAM permission management

---

## ✅ Conclusion

This project successfully implemented a serverless image resizing solution using AWS Lambda and Amazon S3 to automatically process uploaded images efficiently and cost-effectively.
