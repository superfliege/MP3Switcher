# 🎵 Audio A/B Switcher

A powerful web-based audio comparison tool that allows seamless switching between two audio versions (A and B) without interruption. Perfect for music producers, sound engineers, and anyone who needs to compare audio mixes while on the go.

Link: https://superfliege.github.io/MP3Switcher/

<img width="836" height="905" alt="image" src="https://github.com/user-attachments/assets/f4631163-b3c0-4c39-9787-e5b410a03a4b" />


## ✨ Features

### Core Functionality
- **Seamless A/B Switching**: Switch between two audio tracks instantly without stopping playback
- **Synchronized Playback**: Both tracks stay perfectly in sync at all times
- **Timeline Control**: Seek to any position with a visual timeline slider
- **Real-time Visualization**: Live audio spectrum analyzer showing the current audio signal

### Audio Processing
- **3-Band Parametric Equalizer**:
  - Band 1: Low Shelf (affects low frequencies)
  - Band 2: Bell/Peaking (focused frequency adjustment)
  - Band 3: High Shelf (affects high frequencies)
- **Interactive EQ Control**: Drag and drop frequency points in a visual X/Y coordinate system
  - X-axis: Frequency (20 Hz - 20 kHz, logarithmic scale)
  - Y-axis: Gain (-12 dB to +12 dB)
- **EQ Curve Visualization**: See the resulting frequency response curve in real-time
- **Toggle EQ On/Off**: Quickly A/B test with and without EQ processing

### File Support
- **MP3** (audio/mpeg)
- **M4A** (audio/m4a, audio/mp4)
- Drag-and-drop or click to upload

### Mobile & PWA
- **Fully Mobile Optimized**: Touch-friendly interface designed for in-car use
- **Progressive Web App**: Install on Android and iOS devices
- **Offline Capable**: Works without internet connection after installation
- **Landscape Mode Support**: Optimized for both portrait and landscape orientations

### Keyboard Shortcuts
- **A**: Switch to track A
- **B**: Switch to track B
- **Space**: Play/Pause

## 🚀 Getting Started

### Installation

1. Clone or download this repository
2. Open `index.html` in a modern web browser
3. That's it! No build process or dependencies required.

### Local Server (Optional)

For testing PWA features locally, serve via HTTP:

```bash
# Using Python 3
python3 -m http.server 8000

# Using Node.js
npx http-server
```

Then visit `http://localhost:8000`

### PWA Installation

**Android (Chrome/Edge):**
1. Open the app in your browser
2. Click the "📱 App installieren" button
3. Follow the installation prompt

**iOS (Safari):**
1. Open the app in Safari
2. Tap the Share button
3. Select "Add to Home Screen"

## 🎛️ Usage Guide

### Loading Audio Files

1. Click on the "Version A" upload box to select your first audio file
2. Click on the "Version B" upload box to select your second audio file
3. Both MP3 and M4A formats are supported

### Playback Control

1. Click **Play** to start synchronized playback of both tracks
2. Use the large **A** or **B** buttons to switch between versions
3. Click **Pause** to stop playback
4. Drag the timeline slider to seek to any position

### Using the Equalizer

1. Toggle the EQ switch (top right of EQ section) to enable/disable
2. **Drag the colored dots** to adjust:
   - **Horizontally**: Change frequency (20 Hz - 20 kHz)
   - **Vertically**: Change gain (-12 dB to +12 dB)
3. Each band is color-coded:
   - 🔴 Red: Low Shelf
   - 🟢 Green: Bell (Peaking)
   - 🔵 Blue: High Shelf
4. Watch the blue curve update to show the combined frequency response

## 🏗️ Technical Details

### Architecture

- **Pure HTML/CSS/JavaScript**: No frameworks or build tools required
- **Web Audio API**: High-performance audio processing with minimal latency
- **Canvas API**: Real-time visualization and interactive EQ interface
- **Service Worker**: Offline functionality and fast loading

### Performance Optimizations

- **Separate Audio Chains**: Independent processing for A and B tracks prevents conflicts
- **Gain Node Switching**: Uses Web Audio gain nodes instead of HTML5 muting for smooth, glitch-free switching
- **Crossfade**: 15ms smooth crossfade when switching between A and B
- **Optimized Sync**: Balanced synchronization threshold (300ms) for mobile performance
- **Hardware Acceleration**: Canvas rendering optimized for 60 FPS

### Browser Compatibility

- Chrome/Edge 90+
- Firefox 88+
- Safari 14.1+
- Mobile browsers with Web Audio API support

## 📱 Mobile Usage

This app is specifically designed for mobile use, including in-car audio comparison:

- **Large Touch Targets**: Oversized A/B buttons for easy tapping while driving
- **No Accidental Zoom**: Viewport locked to prevent zoom gestures
- **Landscape Optimized**: Compact layout when phone is held horizontally
- **Install as App**: Runs fullscreen like a native app

⚠️ **Safety Notice**: Only use this app when safely parked or when you have a passenger operating it. Never use while actively driving.

## 🔧 Development

### Project Structure

```
MP3Switcher/
├── index.html          # Main application
├── manifest.json       # PWA manifest
├── sw.js              # Service worker
└── README.md          # This file
```

### Customization

**Changing EQ Bands:**
Modify the `bands` array in the JavaScript section:
```javascript
let bands = [
    { freq: 100, gain: 0, color: '#f5576c', x: 0, y: 0 },
    { freq: 1000, gain: 0, color: '#38ef7d', x: 0, y: 0 },
    { freq: 10000, gain: 0, color: '#4facfe', x: 0, y: 0 }
];
```

**Changing Colors:**
Update the CSS gradient colors in the `<style>` section.

## 🤝 Contributing

Contributions are welcome! Feel free to:
- Report bugs
- Suggest new features
- Submit pull requests

## 📄 License

This project is open source and available for personal and commercial use.

## 💡 Use Cases

- **Music Production**: Compare different mix versions
- **Mastering**: A/B test mastered vs. unmastered tracks
- **Sound Design**: Compare different audio processing chains
- **Quality Control**: Verify audio encoding quality
- **Education**: Teaching audio engineering concepts
- **Client Presentations**: Real-time mix comparison for clients

## 🙏 Credits

Built with modern web technologies and designed for professional audio comparison workflows.

---

**Enjoy seamless audio comparison! 🎧**
