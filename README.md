# Video Transcoding Tool (Windows)

A lightweight, Python-based GUI application designed for Windows users to transcode video files using FFmpeg,created with the help of AI. Inspired by the functionality of HandBrake, this tool provides an accessible interface for converting video formats, adjusting quality settings, and utilizing hardware acceleration without requiring complex command-line knowledge.

##  Features

- **User-Friendly Interface**: A clean Tkinter-based GUI that simplifies the transcoding process.
- **Format Conversion**: Support for common output formats including MP4, AVI, MKV, MOV, and WebM.
- **Codec Selection**: Choose between various video codecs (H.264, H.265/HEVC, VP9) and audio options.
- **Quality Control**: Adjust compression quality using CRF (Constant Rate Factor) sliders and presets (from `ultrafast` to `veryslow`).
- **Hardware Acceleration**: Support for GPU acceleration (CUDA, NVENC) where available.
- **FFmpeg Integration**: Automatically detects or allows manual selection of the FFmpeg executable path.
- **Progress Tracking**: Real-time status updates and progress indicators during encoding.
- **Configuration Management**: Save your preferred settings as defaults via a JSON config file.

## Requirements

Before running this tool, ensure you have the following installed on your Windows machine:

1.  **Python 3.x** (Recommended version 3.8 or higher)
2.  **FFmpeg.exe**: Download the latest build from [Gyan.dev](https://www.gyan.dev/ffmpeg/builds/) and place it in a known location, or use the built-in browser to select your existing installation.

### Installation Steps

1.  Install Python if not already installed:
    ```bash
    # Using winget (Windows Package Manager)
    winget install Python.Python.3.11
    ```
2.  Add Python to your system PATH (if not done automatically).
3.  Download the `Hand.py` file and save it as `main.py`.

## 📖 Usage

### Running the Application

You can run the application directly using Python:

```bash
python main.py
```

### Workflow

1.  **Select Source**: Click "Browse" to choose your input video file.
2.  **Set Output**: Choose a destination path or let the tool auto-generate one.
3.  **Configure Settings**:
    -   Select your desired output format (e.g., MP4).
    -   Choose Video Codec (e.g., `libx264` for compatibility, `libx265` for smaller file sizes).
    -   Adjust Quality (CRF) and Preset.
    -   Enable Hardware Acceleration if you have an NVIDIA GPU.
4.  **Start Transcoding**: Click the "🚀 START TRANSCODING" button.
5.  **Monitor Progress**: Watch the status label and progress bar as the file processes.

##  Project Structure

```text
P1/Hcopy/
├── Hand.py      # Main application source code
└── README.md    # This documentation file
```

##  Limitations & Notes

-   **Platform**: Currently optimized for Windows environments.
-   **FFmpeg Dependency**: The tool relies on an external `ffmpeg.exe` binary. It does not bundle FFmpeg to keep the application lightweight.
-   **Progress Accuracy**: Progress estimation is based on frame counting in the log stream; it may vary slightly depending on the codec and hardware acceleration used.
-   **Two-Pass Encoding**: Currently simplified for single-pass workflows. Two-pass logic requires additional implementation for accurate bitrate allocation.

##  License

This project is provided as-is for educational and personal use. It is a clone/inspired by existing tools like HandBrake but is not officially affiliated with them.

---
*Built with ❤️ using Python & Tkinter*
