# TabMixer 🎵

A modern cross-browser extension that gives you granular volume control over individual browser tabs. Built with React and featuring a sleek glassmorphism design.

![TabMixer Extension](https://img.shields.io/badge/Browser%20Extension-Chrome%20%7C%20Firefox-blue)
![Version](https://img.shields.io/badge/version-1.0.0-green)
![License](https://img.shields.io/badge/license-MIT-blue)

## ✨ Features

- **🎛️ Individual Tab Control** - Adjust volume for each tab independently (0-100%)
- **🔇 Smart Mute Toggle** - Instantly mute/unmute any tab with visual feedback
- **🎨 Modern UI** - Beautiful glassmorphism design with smooth animations
- **⚡ Real-time Updates** - Volume changes apply instantly to all audio/video elements
- **🌐 Cross-Browser** - Works seamlessly on Chrome and Firefox
- **🎯 Auto-Detection** - Automatically detects and controls HTML5 media and Web Audio API
- **🔄 Dynamic Loading** - Handles dynamically loaded media content
- **💾 Persistent Settings** - Maintains volume levels across page reloads

## 🚀 Installation

### Chrome
1. Download or clone this repository
2. Open Chrome and navigate to `chrome://extensions/`
3. Enable "Developer mode" in the top right
4. Click "Load unpacked" and select the extension folder
5. The TabMixer icon will appear in your toolbar

### Firefox
1. Download or clone this repository
2. Open Firefox and navigate to `about:debugging`
3. Click "This Firefox" in the sidebar
4. Click "Load Temporary Add-on"
5. Select the `manifest.json` file from the extension folder

## 📁 Project Structure

```
TabMixer-extension/
├── manifest.json          # Extension configuration
├── popup.html            # Main UI (React-powered)
├── content.js            # Content script for audio control
├── background.js         # Service worker for tab management
├── icons/               # Extension icons (16, 32, 48, 128px)
│   ├── icon-16.png
│   ├── icon-32.png
│   ├── icon-48.png
│   └── icon-128.png
└── README.md
```

## 🛠️ How It Works

TabMixer uses a multi-layered approach to provide comprehensive audio control:

### Content Script Layer
- Monitors DOM for audio/video elements using MutationObserver
- Applies volume settings to existing and dynamically loaded media
- Intercepts Web Audio API calls for advanced audio applications

### Background Script Layer
- Manages tab lifecycle and maintains extension state
- Handles communication between popup and content scripts
- Automatically re-injects content scripts on page navigation

### Popup Interface
- Modern React-based UI with real-time tab detection
- Glassmorphism design with smooth animations and hover effects
- Intuitive volume sliders with visual feedback

## 🎨 Design Philosophy

TabMixer embraces modern web design principles:
- **Glassmorphism UI** - Semi-transparent surfaces with backdrop blur
- **Gradient Aesthetics** - Beautiful color gradients for visual appeal
- **Micro-interactions** - Smooth hover effects and transitions
- **Responsive Design** - Consistent experience across different screen sizes
- **Accessibility** - High contrast ratios and keyboard navigation support

## 🔧 Development

### Prerequisites
- Chrome or Firefox browser with developer mode enabled
- Basic knowledge of JavaScript, React, and WebExtensions API

### Local Development
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/TabMixer-extension.git
   cd TabMixer-extension
   ```

2. Make your changes to the source files

3. Reload the extension in your browser:
   - **Chrome**: Go to `chrome://extensions/` and click the refresh icon
   - **Firefox**: Go to `about:debugging` and click "Reload"

### Building Icons
Create icons in the following sizes and place them in the `icons/` folder:
- `icon-16.png` (16x16px) - Toolbar icon
- `icon-32.png` (32x32px) - Extension management
- `icon-48.png` (48x48px) - Extension details
- `icon-128.png` (128x128px) - Chrome Web Store

## 🔒 Permissions

TabMixer requires the following permissions:
- **tabs** - To enumerate and identify browser tabs
- **activeTab** - To interact with the currently active tab
- **scripting** - To inject content scripts for audio control
- **host_permissions: ["<all_urls>"]** - To control audio on all websites

## 🌟 Browser Compatibility

| Browser | Version | Status |
|---------|---------|--------|
| Chrome  | 88+     | ✅ Fully Supported |
| Firefox | 109+    | ✅ Fully Supported |
| Edge    | 88+     | ✅ Should Work* |
| Safari  | N/A     | ❌ Not Supported |

*Edge support is theoretical as it uses Chromium engine, but hasn't been extensively tested.

## 📝 Known Limitations

- Some websites with strict Content Security Policies may prevent audio control
- Embedded content from different domains may not be controllable
- Web Audio API applications with complex routing may have limited control
- Browser-level mute settings take precedence over extension controls

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. **Fork the repository**
2. **Create a feature branch**: `git checkout -b feature/amazing-feature`
3. **Commit your changes**: `git commit -m 'Add amazing feature'`
4. **Push to the branch**: `git push origin feature/amazing-feature`
5. **Open a Pull Request**

### Contribution Guidelines
- Follow the existing code style and conventions
- Test your changes across both Chrome and Firefox
- Update documentation for any new features
- Ensure responsive design principles are maintained

## 🐛 Bug Reports

If you encounter any issues:
1. Check the [Issues](https://github.com/yourusername/TabMixer-extension/issues) page first
2. Create a new issue with:
   - Browser version and operating system
   - Steps to reproduce the problem
   - Expected vs actual behavior
   - Any relevant console errors

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- React team for the excellent UI library
- Chrome and Firefox teams for the WebExtensions API
- The open-source community for inspiration and best practices

## 📊 Roadmap

- [ ] Volume presets and profiles
- [ ] Keyboard shortcuts for quick volume control
- [ ] Audio visualization and spectrum analyzer
- [ ] Custom themes and color schemes
- [ ] Export/import settings functionality
- [ ] Advanced equalizer controls

---

**Made with ❤️ for better audio control**

*Star this repo if TabMixer helps you manage your browser audio!*