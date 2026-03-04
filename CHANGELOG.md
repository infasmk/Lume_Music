

## v2.0.9 - 2026-03-04

### 🎨 Premium Drawer Redesign
- **Modern Dark Theme**: Redesigned the app drawer with a premium dark base (`#0A0A0A`) and glassmorphism-style menu cards.
- **New Profile Header**: Added a gradient (blue → purple) profile header with avatar, display name, email, and an **Edit Profile** action.
- **Reusable Menu Cards**: Replaced default list-style drawer items with reusable animated glass cards (rounded corners, soft press/hover feedback).
- **Music Quick Actions**: Added a dedicated **Music** section with **Downloads**, **Equalizer**, **Sleep Timer**, and **Listening History**.
- **Brand Footer**: Added centered branding with app name, version, and "Made with ❤️ by Infaas".

### 🧹 Settings Cleanup
- **Removed Donate Option**: Deleted the **Donate** section from Settings UI.
- **Code Cleanup**: Removed the unused donate settings screen file and related references.

### ✅ Stability
- Preserved existing navigation flow, authentication behavior, and backend logic while updating only UI structure.
- Built a fresh release APK successfully after the update.

## v2.0.8 - 2026-03-04

### 🚀 Admin Broadcast & Notifications
- **Hidden Admin Access**: Added secret admin entry in About page (multi-tap logo + PIN dialog).
- **In-App Admin Broadcast Panel**: Added dedicated admin screen to compose and send broadcast title/message.
- **Direct FCM HTTP v1 Delivery**: Push notifications now send directly from the app using FCM HTTP v1 (no Cloud Functions or Firestore trigger required).
- **Credential Validation Tooling**: Added **Validate FCM Credentials** action in admin panel before sending.
- **Flexible Auth Input**: Supports either OAuth access token or full Service Account JSON for FCM send flow.
- **Permission-Resilient Sending**: Firestore write now occurs only when in-app popup is enabled, so push-only send is not blocked by Firestore rules.

### ✨ UI & UX Improvements
- **Vibrant Blue Theme**: Updated accent palette from yellow to vibrant blue across the app theme system.
- **Admin Panel Responsiveness**: Fixed non-scrollable admin screen by adding full scroll + keyboard-safe bottom insets.
- **Notification Popup Redesign**:
  - Replaced basic alert with a modern glassy gradient card style
  - Added curved outer gradient border
  - Added default **Visit Site** button (`https://lume.webbits.space`)
  - Removed full-screen blur to avoid background over-blurring

### 🎨 Branding & Assets
- **Launcher Icon Update**: Switched app icon source to `assets/icons/final.png` and regenerated platform icons.
- **About Logo Update**: Updated About page logo to use `assets/icons/final.png`.

### 🛠 Stability & Build
- Cleaned analyzer issues on modified files after integration updates.
- Rebuilt release APK successfully with all new features included.

## v1.2.0 - 2026-01-02

### 🚀 Performance & Playback
- **High-Speed Preloading**: Dramatically reduced latency by preloading up to 3 tracks in the queue.
- **Deep Buffering**: Configured aggressive buffering logic to prevent playback interruptions in low-signal areas.
- **Local Stream Caching**: Implemented `LockCachingAudioSource` to save bandwidth and enable offline-ready replays of recently streamed tracks.
- **Equalizer Pro**: Re-engineered the audio pipeline for zero-latency equalizer updates and smoother sound processing.

### ✨ AI & Discovery
- **Smart Recommendations**: A new recommendation engine that learns from your skips and plays.
- **Trending 2.0**: Enhanced trending algorithm with localized chart support and genre-based popularity scoring.
- **Refined Suggestions**: Improved search auto-complete with better relevance and faster response times.

### 🎨 UI & UX Improvements
- **Animated Shimmers**: Replaced static loaders with smooth, modern shimmering effects.
- **Player Redesign**: Micro-animations on play/pause and like buttons, and refined album art scaling.
- **Library Sync**: Faster DB queries for "Liked Songs" and "Recently Played" sections.

---

## v1.1.0 - 2025-12-17

### 🚀 Performance & Connectivity
- **Telegram Integration**: Added official "Join Channel" button in About screen.
- **Login Fix**: Resolved startup hang on Pixel 5a devices (Async Sync).
- **Lag-Free Scroll**: Optimized memory usage for high-quality images.
- **Storage Optimization**: Implemented auto-cleaning cache (Max 200 items).

### ✨ Enhancements
- **Trending**: Smarter algorithm with diverse song suggestions.
- **Equalizer**: Real-time slider updates (Fixed UI lag).
- **UI**: Added Copyright 2025 to About screen.

---

## v1.0.0 - 2025-12-06

### ✨ Features
- **Smart Discovery**:
  - Instant access to "Your Top Mix", "Discover Weekly", and "Release Radar"
  - Quick Access grid for Liked Songs and Recently Played
  - AI-powered "Made For You" mixes based on listening history
- **Universal Search**:
  - Unified search across YouTube Music, Spotify, and JioSaavn
  - Search by Song, Album, Artist, or Playlist
  - Import external playlists via URL
- **Premium Library**:
  - Organized "Liked Songs" with one-tap access
  - Dedicated "Downloads" section for offline playback
  - Local music support
- **Advanced Player**:
  - High-quality streaming (up to 320kbps)
  - Synchronized Lyrics support
  - Sleep Timer (15min to 1 hour)
  - Background playback with notification controls
- **Customization & UI**:
  - Floating iOS-style "Bubble" notifications
  - Modern "Beats Green" dark theme
  - Smooth animations and transitions
  - Data saver options for streaming and downloading

---

