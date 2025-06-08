# 🎓 AI YouTube Video Finder - Advanced Syllabus Matcher

Transform your syllabus into a personalized video learning experience with this powerful educational tool that automatically finds relevant YouTube videos for your study topics.

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Version](https://img.shields.io/badge/version-1.0.0-green.svg)
![Status](https://img.shields.io/badge/status-active-success.svg)

## ✨ Features

- **🔍 Intelligent Search**: Automatically finds educational videos for each topic in your syllabus
- **🎯 Advanced Filtering**: Filter by duration, upload date, video quality, and more
- **📚 Multiple Topics**: Process entire syllabi with multiple topics at once
- **💾 Save & Export**: Save favorite videos and export results to CSV
- **📊 Smart Analytics**: Track your learning progress with built-in statistics
- **🎨 Beautiful UI**: Modern glass-morphism design with smooth animations
- **📱 Responsive**: Works perfectly on desktop, tablet, and mobile devices
- **🔄 Search History**: Keep track of your previous searches
- **🎪 Demo Mode**: Try the app without API key using demo data

## 🚀 Quick Start

### Option 1: Direct Use (Recommended for Testing)
1. Download or clone this repository
2. Open `index.html` in your web browser
3. Click "Try Demo Mode" to explore the interface
4. For full functionality, set up YouTube API (see below)

### Option 2: With YouTube API
1. Get a YouTube Data API v3 key from [Google Cloud Console](https://console.cloud.google.com/)
2. Open the application and enter your API key
3. Start finding videos for your syllabus!

## 🔧 Installation

```bash
# Clone the repository
git clone https://github.com/yourusername/ai-youtube-video-finder.git

# Navigate to the project directory
cd ai-youtube-video-finder

# Open in your browser
open index.html
```

## 📖 Usage Guide

### 1. **Setting Up API Key**
- Visit [Google Cloud Console](https://console.cloud.google.com/)
- Create a new project or select existing one
- Enable YouTube Data API v3
- Create credentials (API Key)
- Enter the API key in the application

### 2. **Adding Your Syllabus**
```
Introduction to Machine Learning
Neural Networks and Deep Learning
Natural Language Processing
Computer Vision Basics
Reinforcement Learning
```

### 3. **Configuring Filters**
- **Videos per Topic**: Choose how many videos to find for each topic
- **Duration**: Filter by video length (short, medium, long)
- **Upload Date**: Find recent or older content
- **Quality**: HD videos only option
- **Captions**: Closed captioning availability
- **Educational Focus**: Prioritize educational channels

### 4. **Managing Results**
- **Save Videos**: Bookmark videos for later viewing
- **Export Results**: Download CSV file with all video links
- **View Modes**: Switch between grid and list views
- **Search History**: Access previous searches

## ⚠️ Important Limitations

### CORS Issues
Due to browser security restrictions, direct API calls to YouTube may be blocked. Solutions:

1. **Backend Proxy** (Recommended for production):
   ```javascript
   // Create a backend endpoint that proxies YouTube API calls
   app.get('/api/youtube-search', async (req, res) => {
     const response = await fetch(`https://www.googleapis.com/youtube/v3/search?${req.query}`);
     const data = await response.json();
     res.json(data);
   });
   ```

2. **Browser Extensions**: Use CORS-disabling extensions for development

3. **Demo Mode**: Use built-in demo mode for testing interface

## 🛠️ Technical Details

### Built With
- **HTML5**: Semantic markup and structure
- **CSS3**: Advanced styling with glass-morphism effects
- **JavaScript (ES6+)**: Modern vanilla JavaScript
- **Tailwind CSS**: Utility-first CSS framework
- **Font Awesome**: Icon library
- **YouTube Data API v3**: Video search functionality

### Browser Support
- Chrome 90+
- Firefox 88+
- Safari 14+
- Edge 90+

### File Structure
```
ai-youtube-video-finder/
├── index.html              # Main application file
├── README.md              # This file
├── LICENSE               # MIT license
└── screenshots/          # Application screenshots
    ├── main-interface.png
    ├── search-results.png
    └── demo-mode.png
```

## 🔑 API Setup Guide

### Step-by-Step YouTube API Setup

1. **Google Cloud Console Setup**:
   ```bash
   1. Go to https://console.cloud.google.com/
   2. Create new project or select existing
   3. Navigate to "APIs & Services" > "Library"
   4. Search for "YouTube Data API v3"
   5. Click "Enable"
   ```

2. **Create API Key**:
   ```bash
   1. Go to "APIs & Services" > "Credentials"
   2. Click "Create Credentials" > "API Key"
   3. Copy your API key
   4. (Optional) Restrict key for security
   ```

3. **API Quotas**:
   - Free tier: 10,000 units/day
   - Each search costs ~100 units
   - Monitor usage in Cloud Console

## 🎪 Demo Mode Features

When using demo mode, you can:
- ✅ Test the complete user interface
- ✅ Try all filtering options
- ✅ Experience the search workflow
- ✅ Test save/export functionality
- ❌ Cannot play actual videos
- ❌ Limited to sample data

## 🔧 Configuration Options

### Customizing Search Parameters
```javascript
// Modify default search parameters
const DEFAULT_CONFIG = {
  videosPerTopic: 5,
  order: 'relevance',
  type: 'video',
  videoDefinition: 'any',
  videoDuration: 'any'
};
```

### Styling Customization
```css
/* Customize color scheme */
:root {
  --primary-gradient: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  --glass-bg: rgba(255, 255, 255, 0.95);
  --border-radius: 1rem;
}
```

## 📊 Performance Optimization

### Best Practices
- **Batch Processing**: Processes topics sequentially to avoid rate limits
- **Caching**: Implements localStorage for saved videos and history
- **Lazy Loading**: Images load on demand
- **Debounced Input**: Reduces unnecessary API calls

### Rate Limiting
```javascript
// Built-in delays between API calls
await new Promise(resolve => setTimeout(resolve, 200));
```

## 🐛 Troubleshooting

### Common Issues

**"CORS Error"**
```
Solution: Use demo mode or set up backend proxy
Status: Known limitation
```

**"API Quota Exceeded"**
```
Solution: Wait for quota reset or upgrade plan
Check: Google Cloud Console quota usage
```

**"Invalid API Key"**
```
Solution: Verify key is correct and API is enabled
Check: Google Cloud Console credentials
```

**"No Videos Found"**
```
Solution: Try broader search terms or adjust filters
Check: Topic spelling and filter settings
```

## 🤝 Contributing

We welcome contributions! Here's how you can help:

### Development Setup
```bash
# Fork the repository
git clone https://github.com/yourusername/ai-youtube-video-finder.git
cd ai-youtube-video-finder

# Create feature branch
git checkout -b feature/amazing-new-feature

# Make your changes and test
# Commit your changes
git commit -m "Add amazing new feature"

# Push to your fork
git push origin feature/amazing-new-feature

# Create Pull Request
```

### Contribution Guidelines
- Follow existing code style
- Add comments for complex logic
- Test across different browsers
- Update README if needed
- Ensure responsive design

### Priority Features
- [ ] Backend integration template
- [ ] Video playlist creation
- [ ] Progress tracking
- [ ] Advanced analytics
- [ ] Chrome extension version
- [ ] Mobile app version

## 📝 Changelog

### v1.0.0 (Current)
- ✨ Initial release
- ✨ YouTube API integration
- ✨ Advanced filtering system
- ✨ Demo mode implementation
- ✨ Export functionality
- ✨ Search history
- ✨ Responsive design

### Planned Features
- 🔄 Backend proxy template
- 🔄 Video recommendations
- 🔄 Study scheduling
- 🔄 Progress analytics
- 🔄 Social sharing

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

```
MIT License

Copyright (c) 2024 AI YouTube Video Finder

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.
```

## 🙏 Acknowledgments

- **YouTube Data API**: For providing access to video data
- **Tailwind CSS**: For the utility-first CSS framework
- **Font Awesome**: For the beautiful icons
- **Google Fonts**: For the Inter font family
- **Community**: For feedback and suggestions

## 📞 Support

- **Issues**: [GitHub Issues](https://github.com/divyarthjain/Yt-video-finder-according-to-your-syllabus/issues)
- **Discussions**: [GitHub Discussions](https://github.com/divyarthjain/Yt-video-finder-according-to-your-syllabus/discussions)
- **Email**: divyarthj24@gmail.com

## 🌟 Show Your Support

If you find this project helpful, please consider:
- ⭐ Starring the repository
- 🍴 Forking for your own use
- 🐛 Reporting issues
- 💡 Suggesting new features
- 📢 Sharing with others

---

<div align="center">
  <p>Made with ❤️ for students and educators worldwide</p>
  <p>
    <a href="#top">Back to Top</a> •
    <a href="https://github.com/divyarthjain/Yt-video-finder-according-to-your-syllabus">View on GitHub</a> •
    <a href="https://divyarthjain.github.io/Yt-video-finder-according-to-your-syllabus">Live Demo</a>
  </p>
</div>
