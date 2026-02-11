# Pro Downloader Suite - Ultra Edition V13.1

**User Manual & Implementation Guide**

Welcome to the **Pro Downloader Suite**, a high-performance, Python-based downloader powered by `yt-dlp` and `FFmpeg`. This manual documents every verified feature and configuration option available in the compiled application. **Fully accessible with screen readers and keyboard navigation.**

---

## Key Features

### Ultra Organizer
The app automatically creates a master folder in your Downloads and organizes files into dedicated subfolders.
- **Location**: `Downloads/Pro Downloader Suite/`
  - `/YouTube` -> YouTube/Shorts
  - `/TikTok` -> TikTok videos
  - `/Instagram` -> Instagram/Reels
  - `/Facebook` -> Facebook videos
  - `/Twitter` -> Twitter/X videos
  - `/Misc` -> Everything else

### Accessibility & Screen Reader Support
- Fully compatible with NVDA and JAWS screen readers
- Features like trimming are opt-in to prevent crashes during navigation
- All controls have accessible names and descriptions

### Keyboard Shortcuts & Navigation
**Main Actions:**
- **Enter** - Start download (when Download button is focused)
- **Esc** - Cancel current download

**Menu Shortcuts (Alt+Letter for File menu, then):**
- **Ctrl+B** - Open Batch Link Manager
- **Ctrl+M** - Open Local Media Converter
- **Alt+S** - Open Settings
- **Ctrl+H** - View History
- **Alt+F4** - Exit application

**Mnemonic Keys (Alt+Letter to activate):**
- **Alt+D** - DOWNLOAD button
- **Alt+C** - CANCEL button
- **Alt+P** - Playlist checkbox
- **Alt+U** - Subtitles checkbox
- **Alt+T** - Enable Trimming checkbox
- **Alt+K** - Skip Sponsors checkbox
- **Alt+E** - Schedule button

### Smart Auth (Browser Cookies)
- **Controlled Access**: By default, "Smart Auth" is **OFF** to ensure maximum privacy and avoid Chrome database lock issues. 
- **When to Use**: Enable this in **Settings** only if you need to download Private, Restricted, or Member-Only content that your browser (Chrome) can access.
- **Privacy First**: The app never stores your passwords. It only "borrows" the login session from your browser temporarily.
- **Troubleshooting**: If you get a "Cookie Database Locked" error, simply close Chrome and try again, or disable Smart Auth in Settings.

---

## Interface Walkthrough

### 1. Dashboard (Main Screen)
- **URL Input**: Paste any video link here.
    - *Auto-Paste*: If you copy a YouTube link to your clipboard while the app is open, it will automatically paste itself into this box.
- **Download Mode**:
    - **Video**: Downloads MP4/MKV. Quality options range from **4K Ultra HD (2160p)** down to **360p**.
    - **Audio**: Extracts audio to MP3. Quality options: **Best**, **192kbps**, **128kbps**, **64kbps**.
- **Checkboxes**:
    - **Playlist**: Check this if the link is a playlist (downloads all videos).
    - **Subtitles**: Embeds/downloads subtitles if available.

### 2. Professional Tools (God Mode)
Located in the "PROFESSIONAL TOOLS" box:
- **Enable Trimming**: Check this box to enable time range trimming (disabled by default for screen reader compatibility).
    - When checked, the app fetches video duration and enables time pickers.
    - **Trim Range**: Download only a specific part of a video/audio.
        - Format: `HH:MM:SS` (e.g., Start: `00:01:30`, End: `00:02:15`).
    - When unchecked, downloads the entire video.
- **Skip Sponsors**: Uses **SponsorBlock** API to automatically remove sponsored segments, intros, and outros from YouTube videos.
- **Speed Limit**: Cap the download speed (500KB/s, 1MB/s, etc.) to save bandwidth for other tasks.

### 3. Scheduler (All Download Types Supported)
- **Location**: Click the `Schedule` button (Alt+E) or bottom right.
- **What You Can Schedule**: Single URLs, Playlists, OR Batch downloads
- **Usage**:
    
    **For Single URL:**
    1. Paste a video link in the URL input.
    2. Set your preferences (quality, subtitles, etc.).
    3. Click `Schedule` button.
    4. Pick a time in 24-hour format (e.g., `14:30` for 2:30 PM).
    5. Click "Schedule" - your exact settings are saved.
    6. Leave the app running. Download starts automatically at that time.
    
    **For Playlists:**
    1. Check the "Playlist" checkbox.
    2. Paste the playlist link.
    3. Set preferences and click `Schedule`.
    4. Pick time → All videos download automatically at that time.
    
    **For Batch Downloads:**
    1. Open **Batch Link Manager** (File > Batch Link Manager) and add multiple URLs.
    2. Click `Schedule`.
    3. Enter time → All URLs download sequentially at that time.

**Time Selection:**
- One time box with hour:minute format (HH:mm)
- Use **Up/Down arrow keys** to change values
- Or **type directly** (e.g., type "23" then Tab, then "45")
- Screen reader announces each change

### 5. Utilities Menu (File Menu)
- **Batch Link Manager**: Paste multiple links (one per line) to queue them up.
- **Local Media Converter**: Convert local files on your PC (e.g., MKV to MP4, WAV to MP3).
- **View History**: Shows a list of past downloads. Double-click to open the file location.
- **Settings**: Configure default behavior (Theme, Voice, Proxy, Mute).

### 6. QR File Beam
- **Trigger**: Happens automatically after a successful download.
- **Function**: A dialog asks "Beam this file to your phone?". If you click **Yes**:
    1. A QR code appears.
    2. Scan it with your phone (must be on the same Wi-Fi).
    3. The file downloads directly to your phone from your PC.

---

## Configuration & Troubleshooting

### Settings
Located in `File > Settings` (or `settings.json`):
- **Theme**: Gold, Midnight, or Pure Dark.
- **Voice Feedback**: Select Neural voices (e.g., `GuyNeural`, `SoniaNeural`). Requires `edge-tts`.
- **Enable Smart Auth**: Toggle on/off. Must be enabled for private videos. (Default: Off).
- **System Proxy**: Use your system's proxy settings.

### Common Issues
- **"QR Error"**: Ensure your phone and PC are on the same Wi-Fi network. Firewalls may block the connection.
- **"Cookie Check Failed"**: If a restricted video fails, close your Chrome browser and try again. The app automatically retries without cookies if Chrome is locked, which works for non-restricted videos.

---

**Generated by Pro Downloader Team**
*Verified against Build V13.1*
