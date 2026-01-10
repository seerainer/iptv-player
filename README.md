# IPTV Player

A modern, responsive web-based IPTV player that supports M3U playlists with HLS streaming capabilities.

## Features

- 📺 **HLS Streaming Support** - Built with HLS.js for adaptive bitrate streaming
- 🌍 **Predefined Playlists** - Quick access to language-specific IPTV channels (English, German, French, Spanish, Italian, Dutch, Portuguese, Turkish, Arabic)
- 📱 **Responsive Design** - Fully optimized for both desktop and mobile devices
- 🌙 **Dark Mode** - Automatic dark theme based on system preferences
- 🔒 **Security** - Implements Content Security Policy (CSP) and Trusted Types
- 🎨 **Channel Logos** - Displays channel logos with fallback support
- 📂 **Group Organization** - Channels organized by group titles from M3U metadata
- 🎯 **Custom Playlists** - Load any M3U playlist URL

## Getting Started

### Prerequisites

- A modern web browser (Chrome, Firefox, Safari, Edge)
- A web server to serve the files (or open directly in browser for local testing)

### Installation

1. Clone or download this repository
2. Open `index.html` in your web browser, or
3. Serve the files using a web server:

```bash
# Using Python 3
python -m http.server 8000

# Using Node.js http-server
npx http-server

# Using PHP
php -S localhost:8000
```

4. Navigate to `http://localhost:8000` in your browser

## Usage

### Using Predefined Playlists

Click on any playlist from the "Playlists" sidebar to instantly load channels in that language.

### Loading Custom Playlists

1. Enter an M3U playlist URL in the input field
2. Click "Load Playlist"
3. Browse the channel list and click any channel to start playback

### Mobile Usage

- On mobile devices, tap the "Channels" button to open the channel drawer
- Select a channel to start playback
- The drawer automatically closes after selecting a channel

## Supported M3U Format

The player parses M3U playlists with the following format:

```
#EXTINF:-1 tvg-logo="logo-url" group-title="Category Name",Channel Name
http://stream-url
```

## Technical Details

### Technologies Used

- **HTML5 Video API** - Native video playback
- **HLS.js** - HTTP Live Streaming support for non-Apple browsers
- **Vanilla JavaScript** - No framework dependencies
- **CSS Grid & Flexbox** - Modern responsive layouts

### Browser Compatibility

- Chrome/Edge 90+
- Firefox 88+
- Safari 14+
- Opera 76+

### Security Features

- Content Security Policy (CSP) headers
- Trusted Types for preventing XSS attacks
- CORS-aware fetch requests

## Project Structure

```
iptv/
├── index.html      # Main HTML structure
├── script.js       # Application logic and playlist parsing
├── style.css       # Styling and responsive design
└── README.md       # This file
```

## Known Limitations

- Some streams may require CORS proxy for cross-origin access
- Channel availability depends on the playlist source
- HLS streams work best on modern browsers with HLS.js support

## Troubleshooting

### Playlist Won't Load

- Ensure the M3U URL is publicly accessible
- Check if the playlist source allows CORS requests
- Try using a CORS proxy service if needed

### Channel Won't Play

- Some streams may be offline or geo-restricted
- Try a different channel from the playlist
- Check browser console for specific error messages

### Mobile Issues

- Ensure autoplay is allowed in your browser settings
- Some mobile browsers may require user interaction before playback

## Contributing

Contributions are welcome! Feel free to:

- Report bugs
- Suggest new features
- Submit pull requests
- Add more predefined playlists

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Playlist sources from [iptv-org](https://github.com/iptv-org/iptv)
- [HLS.js](https://github.com/video-dev/hls.js/) for HLS streaming support

## Disclaimer

This application is a playlist player. Users are responsible for ensuring they have the right to access and view any content they load. The developers are not responsible for the content of external playlists.
