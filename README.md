# New Age, Faster Keyboard - APK Build Package

## Overview
Revolutionary two-button gesture-based keyboard application designed for faster typing on mobile devices.

## Features
- **Two-Button Interface**: Left button for character selection, right button for actions
- **Gesture-Based Navigation**: Hold and swipe vertically to navigate through characters and sets
- **Frequency-Ordered Characters**: Vowels first, then consonants ordered by English language frequency
- **Multiple Character Sets**: Lowercase, uppercase, numbers, and symbols
- **Touch & Mouse Support**: Works on both mobile and desktop devices
- **Visual Feedback**: Smooth animations and status indicators

## APK Build Instructions

### Prerequisites
1. **Node.js** (v14 or higher)
2. **Apache Cordova** (v12 or higher)
3. **Android Studio** with Android SDK
4. **Java Development Kit (JDK)** 8 or higher

### Setup Steps

1. **Install Dependencies**
   ```bash
   npm install -g cordova
   cd faster-keyboard
   npm install
   ```

2. **Add Android Platform**
   ```bash
   cordova platform add android
   ```

3. **Build APK**
   ```bash
   # Debug build
   cordova build android
   
   # Release build (requires signing)
   cordova build android --release
   ```

4. **Run on Device/Emulator**
   ```bash
   cordova run android
   ```

### File Structure
```
faster-keyboard/
├── index.html          # Main application file
├── manifest.json       # Web app manifest
├── package.json        # Node.js dependencies
├── config.xml          # Cordova configuration
├── res/                # Resources directory
│   ├── icon/android/   # App icons (all densities)
│   └── screen/android/ # Splash screens (all orientations)
└── README.md          # This file
```

### Configuration Details
- **App ID**: com.manus.fasterkeyboard
- **Version**: 1.0.0
- **Target SDK**: Android API 33
- **Min SDK**: Android API 22
- **Orientation**: Portrait (recommended)

### Key Features Implementation
- **Character Sets**: Defined in JavaScript with frequency-based ordering
- **Gesture Recognition**: Touch and mouse event handling for swipe detection
- **Visual Feedback**: CSS animations and status indicators
- **Haptic Feedback**: Cordova vibration plugin integration

### Troubleshooting
1. **Build Errors**: Ensure Android SDK path is correctly set
2. **Permission Issues**: Check Android manifest permissions
3. **Icon/Splash Issues**: Verify all resource files are present in res/ directory

### Testing
The application includes comprehensive touch and gesture handling for:
- Character scrolling (hold + vertical swipe)
- Character set switching (right button hold + swipe)
- Single/double tap actions (space, enter, uppercase modes)
- Long press actions (backspace)

### Deployment
- **Debug APK**: Located in `platforms/android/app/build/outputs/apk/debug/`
- **Release APK**: Located in `platforms/android/app/build/outputs/apk/release/`

For production deployment, ensure proper code signing and Google Play Store compliance.

