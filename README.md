# 🧊 Deep Learning Fridge Scanner App

A deep learning-powered web application that scans images of your fridge to automatically detect food ingredients. It uses a fine-tuned **YOLOv11** model to identify items and helps manage your inventory.

This project is fully containerized using **Docker Compose** for simple, repeatable deployment across any environment.

## 🚀 Technologies Used

| Service | Technology | Purpose |
| :--- | :--- | :--- |
| **Backend API** | Python (FastAPI) | Handles image uploads, runs the YOLOv11 model for object detection, and provides the API interface. |
| **Computer Vision** | Ultralytics YOLOv11 | The core object detection model for identifying food items. |
| **Frontend UI** | React / TypeScript / Vite | The user interface for uploading images and displaying results. |
| **Web Server** | NGINX | Serves the static React build files within the frontend container. |
| **Containerization** | Docker Compose | Defines and runs the multi-container application stack (frontend and backend) with a single command.  |

---

## ⚙️ Prerequisites

To run this application, you only need to have **Docker** and **Docker Compose** installed on your system.

* [Install Docker Engine & Docker Compose](https://docs.docker.com/get-docker/)



## 🏁 Getting Started (Docker version)

### 1. Clone the Repository

Open a terminal and clone the project files:

```bash
git clone https://github.com/BaptisteR23/DL-Fridge-Scanner.git
cd DL-Fridge-Scanner
```

### 2. Build and Run the Stack

Run the following command from the root directory (where the `docker-compose.yml` file is located).

```bash
docker compose up --build -d
```

### 3. Access the Application

Once the command finishes, your application is ready:

| Service | Address (Host Machine) | Purpose |
| :--- | :--- | :--- |
| **Application UI** | **http://localhost:3000** | Access the main web interface here. |
| **Backend API Docs** | `http://localhost:8000/docs` | Test the FastAPI endpoints directly. |

Navigate your browser to **http://localhost:3000** to begin scanning your fridge images.

## ⚖️ Licensing

This project is licensed under the **MIT License**. See the `LICENSE` file for details.