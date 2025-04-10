**FrameFocus** helps automate the task of trimming visual clutter from your videos by intelligently detecting the subject and cropping everything else. Whether you're repurposing content for TikTok, YouTube Shorts, or Instagram Reels, FrameFocus saves time and improves framing without requiring manual work.

Built for content creators, developers, and editors who need quick results with precision.

---

## ✨ Features

- Automatically detects the area of interest in videos
- Supports popular aspect ratios: vertical (9:16), landscape (16:9), and square (1:1)
- Works with single videos or entire folders
- Audio control: keep, silence, or replace soundtracks
- Optimized for backgrounds in solid black or white
- Relies on FFmpeg for sharp and efficient cropping

---

## ⚙️ Installation

To get started, clone the repository and set up the environment:

```bash
git clone https://github.com/yourusername/framefocus.git
cd framefocus
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

Make sure FFmpeg is installed and available in your system path.

---

## 🚀 Usage

### Command Line Interface

```bash
# Crop a single video
python framefocus-cli.py --video_path /path/to/video.mp4

# Crop all MP4 videos in a folder
python framefocus-cli.py --video_dir /path/to/folder

# Crop with a specific output file name
python framefocus-cli.py --video_path /path/to/video.mp4 --out /path/to/output.mp4

# Replace audio with a new track
python framefocus-cli.py --video_path /path/to/video.mp4 --audio-track /path/to/audio.mp3 --audio-volume 0.4

# Remove original audio
python framefocus-cli.py --video_path /path/to/video.mp4 --silence-audio

# Replace original audio and silence it simultaneously
python framefocus-cli.py --video_path /path/to/video.mp4 --silence-audio --audio-track /path/to/audio.mp3 --audio-volume 0.5
```

### Python Usage

```python
import framefocus

framefocus.process_video("/path/to/video.mp4", "/path/to/output.mp4")
```

---

## 🧠 How It Works

1. **Sample Analysis** – Selects multiple frames from the video to understand layout.
2. **Background Isolation** – Identifies plain-colored backgrounds to separate content.
3. **Subject Focus** – Pinpoints the portion of the video with the most visual information.
4. **Aspect Ratio Mapping** – Adjusts the crop zone to fit a standard output size.
5. **Final Processing** – Uses FFmpeg to generate the cropped video with audio options.

---

## 📋 Requirements

- Python 3.9 or newer
- OpenCV
- NumPy
- FFmpeg (install via `brew install ffmpeg` on macOS or your platform's package manager)

---

## 💡 Notes

FrameFocus performs best with videos that have clear separation between content and background. Results may vary with highly dynamic or complex footage. For consistent results, use videos with plain borders or obvious framing.

---

## 🙌 Acknowledgments

Developed and maintained by [Your Name]. Inspired by the everyday need for smarter, faster video editing solutions.

---

## 📄 License

**MIT License**  
You are free to use, modify, and distribute this software as long as the original license is included with any substantial portions of the code.

