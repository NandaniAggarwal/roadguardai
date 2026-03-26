# 🚀 FFmpeg Setup Guide (Windows)

Follow these steps to install and configure FFmpeg for the project.

---

## 📥 Step 1: Install FFmpeg

1. Open **Command Prompt (CMD)**
2. Paste and run:

winget install "FFmpeg (Essentials Build)"


3. Wait for installation to complete.

---

## 🔄 Step 2: Restart CMD

- Close CMD  
- Open it again (important so PATH updates apply)

---

## ✅ Step 3: Verify Installation

Run:

ffmpeg -version


If installed correctly, FFmpeg details will be displayed.

---

## 📍 Step 4: Get FFmpeg Path

Run:
where ffmpeg


- Copy the full path shown  
- Save it somewhere (you’ll need it next)

---

## ⚙️ Step 5: Configure Backend

1. Open:
main/streams.py


2. Find this line (around line 22):

```python
ffmpeg_exe = shutil.which("ffmpeg") or r"C:\Users\DELL.DELL\AppData\Local\Microsoft\WinGet\Packages\Gyan.FFmpeg.Essentials_Microsoft.Winget.Source_8wekyb3d8bbwe\ffmpeg-8.1-essentials_build\bin\ffmpeg.exe"

Replace the path in the or section with your copied path:
ffmpeg_exe = shutil.which("ffmpeg") or r"YOUR_COPIED_PATH_HERE"
