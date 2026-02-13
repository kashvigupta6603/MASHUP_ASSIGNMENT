# 🎧 Mashup Generator & Web Service

A Python-based mashup generator that automatically downloads songs of a singer from YouTube, converts them into audio clips, trims them, merges them into a single mashup, and delivers the result via a web service.

This project was developed as part of an academic assignment to demonstrate command-line automation, multimedia processing, and web service integration.

---

## 🚀 Features

### Program 1 — Command Line Mashup Generator

* Downloads **N songs** of a given singer from YouTube
* Converts videos to audio
* Trims the first **Y seconds** from each audio
* Merges all clips into a single mashup
* Handles invalid inputs and exceptions

### Program 2 — Web Service Mashup Generator

* User-friendly web form interface
* Accepts singer name, number of videos, duration, and email
* Generates mashup automatically
* Sends output as a **ZIP file via email**

---

## 🛠️ Technologies Used

* Python
* Flask (Web Service)
* yt-dlp (YouTube downloading)
* MoviePy (video → audio conversion)
* Pydub (audio trimming & merging)
* FFmpeg (audio processing)
* Yagmail (email delivery)

---

## 📁 Project Structure

```
project/
│
├── mashup.py          # Command-line mashup generator
├── app.py             # Flask web application
├── templates/
│   └── index.html     # Web form interface
└── README.md
```

---

## ⚙️ Installation

### 1️⃣ Install Python Libraries

```bash
pip install yt-dlp moviepy pydub flask yagmail
```

### 2️⃣ Install FFmpeg

**Windows:** download from https://ffmpeg.org and add to PATH
**Mac:**

```bash
brew install ffmpeg
```

**Linux:**

```bash
sudo apt install ffmpeg
```

---

## ▶️ Program 1: Command Line Usage

Run the mashup generator:

```bash
python mashup.py "<SingerName>" <NumberOfVideos> <DurationSeconds> <OutputFile>
```

### Example:

```bash
python mashup.py "Sharry Maan" 20 30 mashup.mp3
```

### Requirements:

* Number of videos must be **greater than 10**
* Duration must be **greater than 20 seconds**

---

## 🌐 Program 2: Web Service Usage

### Start the server:

```bash
python app.py
```

Open in browser:

```
http://127.0.0.1:5000
```

### User inputs:

* Singer name
* Number of videos
* Duration per clip
* Email address

The mashup ZIP file will be sent to the provided email.

---

## 📦 Output

* Combined mashup audio file
* ZIP file (via web service)

---

## ⚠️ Error Handling

The program validates:

* Correct number of parameters
* Invalid numeric inputs
* Duration & video count constraints
* Download/conversion failures

---

## 🎯 Learning Outcomes

This project demonstrates:

* Command-line automation
* Multimedia processing in Python
* API & library integration
* Web service development with Flask
* Email automation
* Exception handling & validation

---

## 📌 Notes

* Internet connection is required for downloading videos.
* Some videos may be skipped if unavailable or restricted.
* FFmpeg must be installed for audio processing.

---

## 👩‍💻 Author

**Kashvi Gupta**
Computer Science Student

---

## ⭐ Acknowledgement

This project was built using open-source Python libraries and tools.
