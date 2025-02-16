# RecFix - YouTube Recommendations Manager for Firefox

RecFix is a Firefox extension that helps you take control of your YouTube recommendations. It allows you to analyze your current recommendations, filter out unwanted content, and guide YouTube's algorithm towards content you actually want to see.

## Features

- 📸 Take snapshots of your current YouTube recommendations
- 🔍 Analyze and filter recommendations
- ⭐ Mark videos you want to prioritize
- 🎯 Generate improved recommendation lists
- 💾 Save curated recommendations as playlists
- 🔄 Reset your recommendations feed
- ⚡ Rate limiting (2 fixes per day) to manage API usage
- 🌙 Dark mode support with system preference detection
- 🎨 Modern UI with smooth animations

## Installation

### Loading the Extension in Firefox
1. Download or clone this repository to your local machine
2. Open Firefox and type `about:debugging` in the address bar
3. Click "This Firefox" in the left sidebar
4. Click "Load Temporary Add-on"
5. Navigate to the directory where you downloaded/cloned the extension
6. Select the `manifest.json` file and click "Open"
7. The extension should now appear in your extensions list
8. Click the extensions menu icon in Firefox's toolbar to pin the extension
9. The RecFix icon should now be visible in your toolbar

### Updating the Extension
1. If you make changes to the extension code:
   - Return to `about:debugging`
   - Find RecFix in the list
   - Click "Reload" to update the extension
2. Note: Temporary add-ons in Firefox need to be reloaded after browser restart

### Troubleshooting Installation
- If the extension doesn't load, check for error messages in:
  - The Browser Console (Ctrl+Shift+J or Cmd+Shift+J)
  - The about:debugging page
- Ensure all required files are present in the directory
- Make sure you're selecting the correct manifest.json file
- Restart Firefox if issues persist

### Required Setup
1. Get a YouTube Data API key:
   - Go to the [Google Cloud Console](https://console.cloud.google.com/)
   - Create a new project or select an existing one
   - Enable the YouTube Data API v3
   - Create credentials (API key)
   - Copy your API key
2. Configure the extension:
   - Click the extension's options button (⚙️)
   - Paste your YouTube API key
   - Save the settings

## Usage

### Visual Guide
> 📝 Note: Screenshots and GIFs coming soon! We're working on creating a visual guide to help you navigate the extension more easily.

### Taking a Snapshot
1. Navigate to YouTube
2. Click the RecFix extension icon
3. Click "Scan Recommendations" to capture your current recommendations
4. Watch as the extension analyzes your feed with a smooth loading animation

### Manual Input
1. Open the RecFix popup
2. Switch to the "Manual Input" tab
3. Paste YouTube video URLs (one per line)
4. Click "Process URLs" to analyze them
5. See real-time validation and processing feedback

### Fixing Recommendations
1. Review the captured recommendations in our card-based interface
2. Check the videos you want to prioritize (with visual feedback)
3. Click "Fix My Feed" to generate improved recommendations
4. Watch the progress with our animated loading indicator
5. Optionally, save the curated list as a playlist

## Privacy & Security

### Data Storage & Security
- RecFix operates entirely in your browser and only communicates with YouTube's servers through the official API
- Your data and preferences are stored locally in Firefox's storage and are never sent to third-party servers
- The extension includes a rate limiter (2 fixes per day) to prevent excessive API usage
- API keys are stored securely in Firefox's local storage using encryption
- Regular security audits ensure your data remains protected
- All operations are performed client-side for maximum privacy

### Usage Monitoring
- Real-time tracking of API usage within the extension
- Daily limit notifications to prevent quota exhaustion
- Transparent logging of all API interactions
- Option to clear all stored data at any time

## UI & Features

### Modern Interface
- Uses Tailwind CSS for responsive styling
- Implements Framer Motion for smooth animations
- Responsive design with dark mode support
- Custom components for video cards and buttons
- Loading spinners and status messages
- Tab-based navigation for easy access

### Dark Mode
- Automatic system preference detection
- Carefully designed color palette for reduced eye strain
- Perfect for late-night YouTube sessions
- Smooth transitions between themes

## Advanced Features

### Dark Mode
- Automatic system preference detection
- Smooth transition between light and dark themes
- Carefully designed color palette for reduced eye strain
- Perfect for late-night YouTube sessions
- Consistent styling across all extension interfaces

### Troubleshooting Guide

#### API Key Issues
- "Invalid API Key" Error:
  1. Check if YouTube Data API v3 is enabled in Google Cloud Console
  2. Verify the key has correct API restrictions
  3. Try regenerating the key if issues persist

#### Rate Limiting
- "Daily Limit Reached" Message:
  1. Wait for the daily reset at midnight UTC
  2. Monitor your remaining daily fixes in the extension
  3. Consider upgrading your API quota for more usage

#### Connection Issues
- "No Response from Content Script":
  1. Refresh the YouTube page
  2. Disable and re-enable the extension
  3. Clear browser cache if problem persists

#### Performance Tips
- Keep YouTube tabs focused when scanning
- Close unused YouTube tabs
- Regular cache clearing for optimal performance
- Limit concurrent operations

## Future Improvements

### Planned Features
- 📱 Mobile companion app development
- 🎯 Enhanced recommendation algorithms
- 🔄 Batch processing capabilities
- 📊 Analytics dashboard
- 🌐 Multi-language support
- 🎨 Custom themes

### Under Consideration
- Safari support
- Video platform integrations
- Community features
- AI-powered analysis
- Recommendation sharing

## Privacy & Rate Limiting

- RecFix operates entirely in your browser and only communicates with YouTube's servers through the official API
- Your data and preferences are stored locally and are never sent to third-party servers
- The extension includes a rate limiter (2 fixes per day) to prevent excessive API usage
- API keys are stored securely in Chrome's local storage

### UI Components
- Uses Tailwind CSS for styling
- Implements Framer Motion for animations
- Responsive design with dark mode support
- Custom components for video cards and buttons
- Loading spinners and status messages
- Tab-based navigation

## Development

### Building CSS
```bash
# Install dependencies
npm install

# Build Tailwind CSS
npx tailwindcss -i ./styles.css -o ./output.css
```

### Debugging
- Check the Browser Console (Ctrl+Shift+J or Cmd+Shift+J) for detailed logs
- All logs are prefixed with `[RecFix]`
- Error messages include stack traces
- API responses are logged for troubleshooting

### Contributing
1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## Error Handling

The extension implements comprehensive error handling for:
- API key validation
- Rate limiting
- Network requests
- Content script communication
- YouTube API responses
- User input validation

## License

MIT License - feel free to use this code in your own projects.

## Support

If you encounter any issues or have suggestions for improvements, please open an issue on GitHub.

## Acknowledgments

Built with:
- YouTube Data API v3
- Tailwind CSS
- Framer Motion
- Firefox Extensions API 