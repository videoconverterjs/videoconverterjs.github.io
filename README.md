🎬 Video Converter

A modern, browser-based video converter that converts WEBM files to MP4 format directly in your browser. No uploads, no server processing — all conversion happens locally on your device.

License

✨ Features

🎥 WEBM to MP4 Conversion — Convert videos directly in the browser
🔒 Privacy First — Files never leave your device
🎨 Modern UI — Beautiful gradient design with smooth animations
🌍 Multilingual — Available in Ukrainian and English
⚡ No Installation — Works as a single HTML file
📱 Responsive Design — Works on desktop, tablet, and mobile devices
🎚️ Quality Settings — Choose between High, Medium, and Low quality
📐 Resolution Options — Original, 1080p, 720p, or 480p output
👁️ Live Preview — Watch conversion in real-time
💾 State Persistence — Settings saved between sessions
🎵 Audio Support — Preserves audio tracks in conversion
🚀 No Dependencies — Uses only native browser APIs

🚀 Getting Started

Quick Start

Simply open index.html in your web browser. No build process or server required.

Local Development

Clone the repository:

git clone https://github.com/videoconverterjs/videoconverterjs.github.io.git
cd videoconverterjs.github.io

Open the file in a browser:

# macOS
open index.html

# Linux
xdg-open index.html

# Windows
start index.html

Or serve it with any static server:

📖 Usage

Upload a file — Drag and drop a WEBM file into the drop zone, or click to select one
Configure settings — Choose your desired quality and resolution
Convert — Click the "Convert to MP4" button
Watch progress — See live preview and progress as conversion happens
Download — Save the converted MP4 file to your device

🛠️ How It Works

The application uses native browser APIs to perform video conversion:

Step Technology
Decoding HTML5 <video> element
Frame Capture requestVideoFrameCallback API
Rendering HTML5 <canvas>
Audio Capture Web Audio API
Encoding MediaRecorder API
Stream Combining MediaStream API

The conversion process:

Loads the WEBM file into a video element
Sets up a canvas with the target resolution
Captures audio through the Web Audio API
Draws each video frame to the canvas while playing
Records the canvas stream + audio stream using MediaRecorder
Outputs the final MP4 (or WEBM fallback) file

⚙️ Configuration

Quality Presets

Quality Bitrate Multiplier Use Case
High 3.0x Best quality, larger files
Medium 1.8x Balanced quality and size
Low 0.9x Smaller files, lower quality

Resolution Options

Original — Keeps source resolution
1080p — 1920×1080
720p — 1280×720
480p — 854×480

🌐 Languages

The application supports:

🇺🇦 Ukrainian (Українська)
🇬🇧 English

Language preference is automatically saved and restored.

🐛 Troubleshooting

Output file is empty or has no video

Ensure your input file is a valid WEBM video with a video track
Check the browser console for errors
Try a different quality setting

Conversion is slow

Conversion runs in real-time (1-minute video ≈ 1 minute conversion)
Lower quality and resolution settings will be faster
Close other tabs to free up resources

MP4 is not supported by browser

The app will automatically fall back to WEBM format
The output file will still be playable in most modern players

📁 Project Structure

videoconverterjs.github.io/
├── index.html          # Main application file
├── README.md           # This file
└── LICENSE             # MIT License

🤝 Contributing

Contributions are welcome! Feel free to:

Fork the repository
Create a feature branch (git checkout -b feature/amazing-feature)
Commit your changes (git commit -m 'Add amazing feature')
Push to the branch (git push origin feature/amazing-feature)
Open a Pull Request

📝 License

MIT

🔗 Links

Repository: github.com/videoconverterjs/videoconverterjs.github.io
Live Demo: videoconverterjs.github.io
Issues: Report a bug

💡 Acknowledgments

Built with native web technologies:

MediaRecorder API
Web Audio API
Canvas API
requestVideoFrameCallback


Made with ❤️ for privacy-conscious users who don't want to upload their videos to third-party services.
