# **NK Video Toolbox**

## 📌 Introduction
**NK Video Toolbox** is a video processing tool that supports:
- 🔍 **Retrieving video information** (resolution, duration, file size)
- 📝 **Generating YouTube chapter timestamps** (`timestamps.txt`)
- 🎬 **Merging multiple video files**
- 🏷️ **Automatically naming output files based on the folder name**

This tool works on **macOS** and **Linux**, utilizing `ffmpeg` for video processing.

---

## ⚡ Installation

### 1️⃣ **Install `ffmpeg`** (if not installed)
```bash
brew install ffmpeg  # macOS (Homebrew)
sudo apt install ffmpeg  # Ubuntu / Debian
```

### 2️⃣ **Install NK Video Toolbox using `pipx` (Recommended)**
```bash
pipx install --force git+https://github.com/nkliu1772/NK-Video-Toolbox.git
```

If `pipx` is not installed, run:
```bash
python3 -m pip install --user pipx
python3 -m pipx ensurepath
```

---

## 🚀 Usage

### **1️⃣ Get Video Information**
```bash
nk-video /path/to/video_folder
```
🔹 Displays resolution, duration, and file size.

### **2️⃣ Generate YouTube Chapter Timestamps**
```bash
nk-video-timestamps /path/to/video_folder
```
🔹 Creates `timestamps.txt` and prompts user for confirmation.

### **3️⃣ Merge Videos**
```bash
nk-video-merge /path/to/video_folder
```
🔹 Confirms timestamps before merging videos.

🔹 The default output file name is **the folder name**, but you can specify an output file with `-o`:
```bash
nk-video-merge /path/to/video_folder -o output.mp4
```

---

## 📌 TODO
- [ ] Add `.srt` merge support(auto shift)
- [ ] Add Windows support
- [ ] Improve CLI usability
- [ ] Add GUI for better user experience

## 🛠️ License
This project is licensed under the MIT License.