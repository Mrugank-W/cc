# 🎥 Video Transcriber

**Video Transcriber** is a cloud-based application hosted on **Amazon EC2** that allows users to upload video files and receive automatic transcriptions using **AWS Transcribe**. It integrates multiple AWS services to provide a fully automated, scalable transcription pipeline.

---

## 🌐 Overview

- Upload video via a simple web interface
- Video gets stored in an **Amazon S3** bucket
- AWS **Transcribe** is triggered upon upload
- Transcription results are returned and displayed on the web page
- IAM Roles are used for secure communication between services

---

## ⚙️ Technologies Used

| Component      | Technology         |
|----------------|--------------------|
| Frontend       | HTML hosted on EC2 |
| Storage        | Amazon S3          |
| Transcription  | AWS Transcribe     |
| Backend Logic  | AWS-native trigger (no Lambda) |
| Permissions    | IAM Roles          |

---

## 🔐 IAM Roles

- **EC2 Instance Role**: Can access S3 and Transcribe for fetching results
- **S3 Bucket Permissions**: Allow uploads and read access
- **Transcribe Access Role**: Grants access to transcribe videos uploaded to S3

---

## 🚀 How to Run

1. Launch an EC2 instance and serve the HTML frontend.
2. Access the web page using your EC2's public IP.
3. Upload a video file.
4. The video is stored in an S3 bucket.
5. AWS Transcribe processes the video and generates a transcription.
6. The transcription result is returned to the EC2 frontend and displayed.

---

## 🌩️ Why Use the Cloud?

Deploying this project on AWS brings several advantages:

- **Scalability**: Easily handles increasing workloads without changing infrastructure.
- **High Availability**: Services like EC2, S3, and Transcribe are designed for durability and uptime.
- **Cost Efficiency**: Pay-as-you-go pricing ensures you only pay for what you use.
- **Security**: Fine-grained access control through IAM roles keeps your data and services protected.
- **Automation**: S3 event notifications and AWS Transcribe integration enable a seamless, automated transcription workflow


## Architechture
.![Screenshot 2025-04-24 200018](https://github.com/user-attachments/assets/c8bd688a-a248-43b4-8ec4-c0f9da5f7261)
