# Vignette 🌍✈️

> **Visualize Your Travels. Relive Your Memories.**

**Vignette** is a sophisticated mobile travel companion app that transforms your photo library into an interactive travel journal. By leveraging local metadata processing and smart clustering algorithms, it automatically maps your journeys, creates artistic photo mosaics, and provides rich travel statistics—all while maintaining complete user privacy.

*Available on iOS and Android.*

---

## 📱 Project Overview

Vignette was built to solve a common problem: we take thousands of travel photos that get lost in our camera rolls. This app brings them back to life by plotting them on a 3D interactive globe and organizing them into coherent "Journeys" without requiring manual input.

### Key Features

- **Interactive World Map:** A 3D map interface that visualizes every country and city you've visited, with markers for specific memories.
- **Smart Journey Detection:** Algorithms that scan local photo metadata (EXIF) to automatically detect trips based on date, time, and GPS coordinate clustering.
- **Privacy-First Architecture:** All photo processing and map generation happen **on-device**. No personal photos are ever uploaded to a cloud server.
- **Mosaic Generation:** Automatically generates beautiful, shareable photo collages ("Year Wrapped") for your trips.
- **Travel Statistics:** Tracks total distance traveled, countries visited, and creates a "Passport" of your adventures.

---

## 🛠️ Tech Stack

This project was engineered with a focus on performance, smooth animations, and cross-platform compatibility.

- **Framework:** [React Native](https://reactnative.dev/) (Expo)
- **Language:** TypeScript
- **Navigation:** React Navigation (Native Stack & Bottom Tabs)
- **Mapping:** `react-native-maps` with custom tile overlays and Polyline rendering
- **Animations:** `react-native-reanimated` and `lottie-react-native` for high-performance UI interactions (60fps)
- **Local Storage:** `AsyncStorage` & `expo-sqlite` for persisting user journey data locally
- **Native Modules:** `expo-media-library` for accessing and processing device storage and EXIF data
- **Backend (Auth/Sync):** .NET Core (C#) API with PostgreSQL (Dockerized) for user profile management.

---

## 🎨 Design Philosophy

Vignette employs a **Modern, Premium Aesthetic**:

- **Glassmorphism:** Extensive use of blur views and translucent layers for a sleek, depth-filled UI.
- **Dark Mode Optimization:** A rich, deep color palette (`#1A1A1A` base) designed to make photos pop.
- **Fluid Transitions:** Custom shared element transitions when opening albums or expanding maps.
- **Haptic Feedback:** Subtle tactile responses for interactions like zooming into a map region or scrolling through a timeline.

---

## 🚀 Challenges & Solutions

### 1. High-Performance Photo Scanning
**Challenge:** Scanning thousands of local photos for GPS data caused UI freezing on older devices.
**Solution:** Implemented a batched processing system with concurrency limits, processing photos in chunks and yielding to the JS thread to keep the UI responsive.

### 2. Dynamic Map Clustering
**Challenge:** Rendering hundreds of pins on a map cluttered the interface and dropped FPS.
**Solution:** Developed custom clustering logic that groups nearby photos dynamically based on zoom level, only rendering individual pins when the user dives deep into a location.

### 3. Cross-Platform Safe Areas
**Challenge:** Ensuring a unified design across iPhones (with dynamic islands) and various Android notch styles.
**Solution:** Heavily utilized `react-native-safe-area-context` to build a custom adaptive layout engine that perfectly positions navigation elements regardless of the device hardware.

---

## 🔒 Privacy & Security

Vignette is designed with a **"Local-First"** mindset.
- **No Photo Uploads:** Your memories stay on your phone. We only access metadata (Location/Time) to generate the map.
- **Data Control:** Users have full control to export or delete their travel history at any time.

---

## 📧 Contact

**Saad Khattak**
- [GitHub Profile](https://github.com/khattaksaad)
- [LinkedIn](https://linkedin.com/in/khattaksaad)
- Email: [vignette.sp@gmail.com](mailto:vignette.sp@gmail.com)

---

*Note: The source code for Vignette is currently in a private repository as it is a commercial product. This repository serves as a portfolio showcase of the technology and design behind the app.*
