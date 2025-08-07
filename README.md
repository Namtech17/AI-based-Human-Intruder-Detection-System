# 🛡️ Human Intrusion Detection System 🔍

A real-time security system that uses **YOLOv8**, **Flask**, **OpenCV**, and **Socket.IO** to detect humans via webcam, raise alerts, send email snapshots, and allow access via QR code on your mobile phone.

---

## 🚀 Demo Preview

### 🔴 Real-Time Detection
![Live Detection Example](snapshot/snapshot_2024-11-30_15_52_13.jpg)

### 📱 QR Code Access from Phone
<img src="https://upload.wikimedia.org/wikipedia/commons/8/8a/Qr-1.png" alt="QR Code Demo" width="200" />

---

## ⚙️ Features

- 🧠 YOLOv8 model for accurate person detection
- 🔴 Real-time video streaming via Flask + Socket.IO
- 🖼️ Snapshot saving when detection happens
- 📧 Email alerts with detection time and image
- 🔊 Sound alert using `pygame`
- 📱 Access via QR Code on your mobile (same Wi-Fi)

---

## 🛠️ Installation

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/Human-intrusion-detection-system.git
cd Human-intrusion-detection-system
```

### 2. Install Dependencies

Create and activate a virtual environment *(optional but recommended)*:

```bash
python -m venv venv
venv\Scripts\activate  # Windows
```

Install required packages:

```bash
pip install -r requirements.txt
```

If you don’t have `requirements.txt`, manually install:

```bash
pip install flask flask_socketio ultralytics opencv-python pygame qrcode python-dotenv
```

---

## ✏️ Configuration - What You MUST Change

1. **Email Credentials**
   - Create a `.env` file:
     ```env
     EMAIL=your_email@gmail.com
     PASSWORD=your_app_password
     TO_EMAIL=recipient_email@gmail.com
     ```
   - Don't forget to allow “less secure apps” or generate an **App Password** in Gmail.

2. **Alert Sound**
   - Replace the sample `static/alert.mp3` with your own audio if needed.

3. **YOLOv8 Weights**
   - Make sure `yolov8n.pt` is present in the project root.
   - Download from: [https://github.com/ultralytics/ultralytics](https://github.com/ultralytics/ultralytics)

---

## 🚦 How to Run

```bash
python app.py
```

- The terminal will show your **local IP** and display a **QR code**.
- Open `http://127.0.0.1:5000` or scan the QR code on your mobile (must be on same Wi-Fi).
- Watch live feed — alerts trigger on human detection.

---

## 📁 Project Structure

```
Human-intrusion-detection-system/
├── app.py
├── yolov8n.pt
├── .env
├── static/
│   └── alert.mp3
├── templates/
│   └── index.html
├── snapshot/
│   └── snapshot_*.jpg
└── README.md
```

---

## 🧪 Example Output

- ✅ Human detected ➝ Green box
- ✅ Email sent ➝ With image + timestamp
- ✅ Sound plays ➝ Alert.mp3
- ✅ Snapshot saved ➝ In `snapshot/` folder

---

## 🧠 Tech Stack

- Python 3.10+
- Flask
- Flask-SocketIO
- YOLOv8 (Ultralytics)
- OpenCV
- Pygame
- QRCode
- HTML/CSS (frontend)

---

## 🤝 Acknowledgments

- [Ultralytics YOLOv8](https://github.com/ultralytics/ultralytics)
- Flask documentation
- OpenCV tutorials

---

## 📌 License

This project is licensed under the [MIT License](LICENSE).

---

## 💡 Want to Contribute?

Pull requests and suggestions are welcome! Let’s build smarter security together.