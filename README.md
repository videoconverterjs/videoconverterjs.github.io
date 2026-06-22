# 🎬 Video Converter

A modern, browser-based video converter that converts WEBM files to MP4 format directly in your browser. No uploads, no server processing — all conversion happens locally on your device.

![License](https://img.shields.io/badge/license-MIT-green.svg)

## 🔗 Links

- **Live Demo:** [videoconverterjs.github.io](https://videoconverterjs.github.io)
- **Repository:** [github.com/videoconverterjs/videoconverterjs.github.io](https://github.com/videoconverterjs/videoconverterjs.github.io)
- **Issues:** [Report a bug](https://github.com/videoconverterjs/videoconverterjs.github.io/issues)

## ✨ Features

- 🎥 **WEBM to MP4 Conversion** — Convert videos directly in the browser
- 🔒 **Privacy First** — Files never leave your device
- 🎨 **Modern UI** — Beautiful gradient design with smooth animations
- 🌍 **Multilingual** — Available in Ukrainian and English
- ⚡ **No Installation** — Works as a single HTML file
- 📱 **Responsive Design** — Works on desktop, tablet, and mobile devices
- 🎚️ **Quality Settings** — Choose between High, Medium, and Low quality
- 📐 **Resolution Options** — Original, 1080p, 720p, or 480p output
- 👁️ **Live Preview** — Watch conversion in real-time
- 💾 **State Persistence** — Settings saved between sessions
- 🎵 **Audio Support** — Preserves audio tracks in conversion
- 🚀 **No Dependencies** — Uses only native browser APIs

## 🚀 Getting Started

### Quick Start

Simply open `index.html` in your web browser. No build process or server required.

### Local Development

Clone the repository:

```bash
git clone https://github.com/videoconverterjs/videoconverterjs.github.io.git
cd videoconverterjs.github.io
```

Open the file in a browser:

```bash
# macOS
open index.html

# Linux
xdg-open index.html

# Windows
start index.html
```

## 📖 Usage

1. **Upload a file** — Drag and drop a WEBM file into the drop zone, or click to select one
2. **Configure settings** — Choose your desired quality and resolution
3. **Convert** — Click the "Convert to MP4" button
4. **Watch progress** — See live preview and progress as conversion happens
5. **Download** — Save the converted MP4 file to your device

## 🛠️ How It Works

The application uses native browser APIs to perform video conversion:

| Step | Technology |
|------|-----------|
| **Decoding** | HTML5 `<video>` element |
| **Frame Capture** | `requestVideoFrameCallback` API |
| **Rendering** | HTML5 `<canvas>` |
| **Audio Capture** | Web Audio API |
| **Encoding** | `MediaRecorder` API |
| **Stream Combining** | `MediaStream` API |

The conversion process:
1. Loads the WEBM file into a video element
2. Sets up a canvas with the target resolution
3. Captures audio through the Web Audio API
4. Draws each video frame to the canvas while playing
5. Records the canvas stream + audio stream using MediaRecorder
6. Outputs the final MP4 (or WEBM fallback) file

## ⚙️ Configuration

### Quality Presets

| Quality | Bitrate Multiplier | Use Case |
|---------|-------------------|----------|
| **High** | 3.0x | Best quality, larger files |
| **Medium** | 1.8x | Balanced quality and size |
| **Low** | 0.9x | Smaller files, lower quality |

### Resolution Options

- **Original** — Keeps source resolution
- **1080p** — 1920×1080
- **720p** — 1280×720
- **480p** — 854×480

## 🌐 Languages

The application supports:
- 🇺🇦 Ukrainian (Українська)
- 🇬🇧 English

Language preference is automatically saved and restored.

## 🐛 Troubleshooting

### Output file is empty or has no video
- Ensure your input file is a valid WEBM video with a video track
- Check the browser console for errors
- Try a different quality setting

### Conversion is slow
- Conversion runs in real-time (1-minute video ≈ 1 minute conversion)
- Lower quality and resolution settings will be faster
- Close other tabs to free up resources

### MP4 is not supported by browser
- The app will automatically fall back to WEBM format
- The output file will still be playable in most modern players

## 📁 Project Structure

```
videoconverterjs.github.io/
├── index.html          # Main application file
├── README.md           # This file
└── LICENSE             # MIT License
```

## 🤝 Contributing

Contributions are welcome! Feel free to:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 License

MIT

## 💡 Acknowledgments

Built with native web technologies:
- [MediaRecorder API](https://developer.mozilla.org/en-US/docs/Web/API/MediaRecorder)
- [Web Audio API](https://developer.mozilla.org/en-US/docs/Web/API/Web_Audio_API)
- [Canvas API](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API)
- [requestVideoFrameCallback](https://developer.mozilla.org/en-US/docs/Web/API/HTMLVideoElement/requestVideoFrameCallback)

---

Made with ❤️ for privacy-conscious users who don't want to upload their videos to third-party services.
