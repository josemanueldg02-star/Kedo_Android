# Kedo — Android App

Native Android client for the [Kedo Backend](https://github.com/josemanueldg02-star/Kedo_Backend) 
REST API. Allows users to discover and manage geolocation-based community events, 
with a dynamic UI that adapts based on the authenticated user's role.

Built as the capstone project for a Higher Degree in Multiplatform Application 
Development (DAM).

[![Kotlin](https://img.shields.io/badge/Kotlin-latest-7F52FF)](https://kotlinlang.org/)
[![Android](https://img.shields.io/badge/Android-native-3DDC84)](https://developer.android.com/)
[![MVVM](https://img.shields.io/badge/Architecture-MVVM-blue)]()
[![Material Design](https://img.shields.io/badge/UI-Material%20Design-757575)](https://m3.material.io/)

---

## Features

- **JWT authentication** — secure login with token stored and sent on 
every API request
- **Role-based UI** — the interface adapts dynamically depending on 
whether the user is an admin or a standard user
- **Geolocation-based event discovery** — community events filtered and 
displayed based on the user's location
- **Real-time data sync** — asynchronous REST API consumption for 
persistent, up-to-date data

---

## Tech Stack

- **Language:** Kotlin
- **Architecture:** MVVM (Model-View-ViewModel)
- **UI:** Native Android components with Material Design
- **Networking:** HTTP/JSON requests to the Kedo REST API
- **Build:** Gradle

---

## Technical Highlights

- **MVVM architecture.** ViewModels expose UI state via LiveData/StateFlow, 
keeping business logic out of Activities and Fragments and making the app 
easier to test and maintain.
- **Role-driven view layer.** The JWT payload contains the user role, which 
the app reads on login to render admin or standard user screens without 
additional API calls.
- **Network-aware data layer.** API calls are handled asynchronously, with 
error states surfaced to the UI cleanly through the ViewModel layer.

---

## Running Locally

**Prerequisites:** Android Studio, and 
[Kedo_Backend](https://github.com/josemanueldg02-star/Kedo_Backend) 
running locally.

```bash
git clone https://github.com/josemanueldg02-star/Kedo_Android.git
```

1. Open the project in **Android Studio**
2. Sync Gradle (`File → Sync Project with Gradle Files`)
3. Update the API base URL to your machine's local IP address 
(e.g. `http://192.168.X.X:8080`) — `localhost` resolves to the 
device itself, not your computer
4. Run on emulator or physical device

---

## Author

**José Manuel Domínguez García** · [@josemanueldg02-star](https://github.com/josemanueldg02-star)
