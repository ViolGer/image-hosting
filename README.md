# 🖼️ Image Hosting App

A self-hosted image hosting service built with FastAPI, served via Nginx and containerized using Docker.  
Users can upload, view, and manage images through a simple HTML interface or API.

---

## ✨ Features

- Upload images via web interface (upload.html)
- View uploaded images in browser (images.html)
- Static file serving through Nginx
- UUID-based filenames to avoid collisions
- Dockerized + Nginx reverse proxy (production-ready)
- Clean, minimal frontend in static/

---

## 🧠 Tech Stack

- Python 3, FastAPI
- HTML5, JavaScript
- Nginx
- Docker + Docker Compose
- UUID + local file storage

---

## 📁 Project Structure

image-hosting/ ├── app.py                 
# FastAPI application ├── Dockerfile             
# Backend container ├── compose.yml            
# Docker Compose setup ├── nginx.conf            
# Nginx config for serving static + reverse proxy ├── static/          
# Frontend (HTML/CSS/JS) ├── images/              
# Stored uploaded images ├── .gitignore └── requirements.txt

---

## 🚀 Quick Start (with Docker)

Make sure Docker and Docker Compose are installed.

`bash
git clone https://github.com/ViolGer/image-hosting.git
cd image-hosting
docker-compose up --build

App will be available at:
📍 http://localhost (upload page: /upload, gallery: /images)


---

🔧 Local Development

If you want to run it manually (without Docker):

pip install -r requirements.txt
uvicorn app:app --reload


---

🛡 Security Notes

Filenames are randomized with UUIDs

No user auth (MVP version)

You should add cleanup, storage quota, and validation for production use



---

💡 Possible Improvements

Authentication for image uploads

Database support for metadata

Preview thumbnails

Expiring shareable links

Cloud storage (S3)
