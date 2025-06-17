# Django Bookmarks App

A Django web application that lets users save and share bookmarks with thumbnails, like and follow system.

Written for deep learning purposes. It includes advanced functionality like Google OAuth2 login, bookmarklet support, and HTTPS setup with custom SSL certificates.


## Features

### 🧑‍🤝‍🧑 Social Website with User Accounts

* User **registration, login, logout, password reset**, and password change
* Extended user profiles with editable fields and profile pictures
* Media file upload support for user content
* Authentication built using Django’s built-in system

### 🔐 Google OAuth2 Authentication

* Secure login with **Google accounts** using OAuth 2.0
* Implemented via `python-social-auth`
* Custom authentication pipeline to auto-create user profiles
* Duplicate email check and prevention
* HTTPS support for local development with self-signed certificates

### 📌 Image Bookmarking System

* Users can **bookmark images** from any website
* JavaScript **bookmarklet** to save images directly while browsing the web
* Image thumbnails generated with `easy-thumbnails`

### ⚡ Asynchronous Features & UX Enhancements

* **Infinite scroll** to load more bookmarks without reloading the page
* AJAX-powered **like/unlike** functionality for bookmarks

### 👥 Social Features

* Users can **follow/unfollow** other users
* Personalized **activity feed** showing actions of followed users
* **Like system** for bookmarked images
* Activity tracking using Django signals

### 📈 Performance & Analytics

* Image **view counts stored in Redis**
* Real-time **ranking of popular bookmarks**
* **Django Debug Toolbar** integration for development insights
* Optimized database queries using `select_related`, `prefetch_related`, etc.

## Screenshots

![Screenshot from 2025-06-17 11-52-13](https://github.com/user-attachments/assets/4c549418-d545-4a2e-8b5b-80877f098e20)
![Screenshot from 2025-06-17 11-35-41](https://github.com/user-attachments/assets/e0d752e7-66ca-4c5f-ae72-76d207892ebd)
![Screenshot from 2025-06-17 11-37-46](https://github.com/user-attachments/assets/4bd2dff4-be4d-4062-bb05-1258ff9033c3)
![Screenshot from 2025-06-17 11-38-10](https://github.com/user-attachments/assets/395dda0e-bf35-4b0e-b907-2731d3b8df14)
![Screenshot from 2025-06-17 11-36-03](https://github.com/user-attachments/assets/47c688ae-dc2b-44eb-9da9-3f4548bb461e)
![Screenshot from 2025-06-17 11-36-42](https://github.com/user-attachments/assets/8b19ab82-4ee3-4b1d-924f-8b9510179579)
![Screenshot from 2025-06-17 11-36-20](https://github.com/user-attachments/assets/f12c7d0b-1f28-42a5-9a6a-deba6db98c27)
![Screenshot from 2025-06-17 11-37-20](https://github.com/user-attachments/assets/88229f29-830e-4f10-b863-ffb38a5cfae1)
![Screenshot from 2025-06-17 11-49-30](https://github.com/user-attachments/assets/6b095f90-13dd-428f-b5d9-fc238bb39e03)
![Screenshot from 2025-06-17 11-50-02](https://github.com/user-attachments/assets/aaf5849c-dd28-4518-a4ae-c318c6e22578)
![Screenshot from 2025-06-17 11-50-13](https://github.com/user-attachments/assets/2d425f6e-8bf4-473c-b465-ddaa42339333)
![Screenshot from 2025-06-17 11-35-05](https://github.com/user-attachments/assets/1451f2fa-982e-4cef-9143-6dd7a0ed599b)
![Screenshot from 2025-06-17 11-51-50](https://github.com/user-attachments/assets/6bc0de84-9629-4b73-8b6f-ee64ed2970bb)


## Installation

1. **Clone the repository:**
    ```bash
    git clone https://github.com/Pietruszko/blog-app.git
    cd blog-app
    ```
2. **Create and activate a virtual environment:**
    ```bash
    python3 -m venv venv
    source venv/bin/activate  # Linux/macOS
    venv\Scripts\activate     # Windows
    ```
3. **Install dependencies:**
    ```bash
    pip install -r requirements.txt
    ```
4. **Set up environment variables:**
    - Copy .env.template to .env:
    ```bash
    cp .env.template .env
    ```
    - Fill in your own values (DB config, email credentials, etc.) inside .env.
5. **Apply migrations:**
    ```bash
    python manage.py migrate
    ```
6. **Create a superuser (for the admin panel):**
    ```bash
    python manage.py createsuperuser
    ```
7. **Run the development server:**
    ```bash
    python manage.py runserver
    ```

### Note! To use GoogleOauth2 and Bookmarklet script you would need to run your development server through HTTPS with custom certificates, create an aPI key in your Google Developer Console and use:
  ```bash
  python manage.py runserver_plus --cert-file cert.crt
  ```
