# MenyAI

## Description

MenyAI is an **Adult literacy learning platform** focused on the Rwandan Population in Kinyarwanda language with optional AI assistance to improve.  
The mobile app (built with **React Native (Expo)** and **TypeScript**) guides learners through structured levels, lessons, and practice activities.  
It is designed for adults  with simple interfaces, clear progress tracking, and room for AI-powered personalization in future iterations.


## GitHub repository

> Replace the placeholder URL below with your actual repository link.

- GitHub: [MenyAI repository](https://github.com/your-username/menyai)

## Platform overview

MenyAI aims to:

- Help learners **read and understand Kinyarwanda** through structured, level-based content.
- Provide **short, focused lessons** with images, audio, video, words, and simple interactions.
- Track **learner progress** across levels and lessons.
- Offer an **AI assistant** (future-ready) for guidance, explanations, and adaptive practice.

Core concepts:

- **Levels** – Progressive difficulty tiers (e.g., beginner, intermediate).
- **Lessons** – Individual learning units with text, images, and activities.
- **Practice** – Matching exercises and other activities to reinforce learning.
- **Progress tracking** – Simple visual indicators (streaks, completion).

## Screens

- **Login** – Phone + PIN, “Injira”
- **Register** – Create a new account (phone + profile details)
- **Forgot PIN** – Help users recover or reset their PIN
- **Home** – Greeting, “Amasomo” / “Amasomo yose”
- **Lessons** – Level picker, lesson cards (completed / download)
- **Yiga (Learn/[level])** – Lesson list per level
- **Lesson Detail** – View lesson content before practice
- **Practice (Iyitoze)** – Match word to image
- **Progress** – Progress bar and streak
- **Activities** – Placeholder for extra activities
- **Account** – Profile overview and navigation to settings
- **Profile** – Edit basic user information
- **Settings** – App preferences (future: language, notifications, etc.)
- **Help / About** – FAQ, app information, and support details
- **AI Assistant** – Screen reserved for AI-powered tutoring features

## Designs

Design assets and references:

- **UI Design HTML mockup**: `menyai-ui-design.html` in the project root  
  (Open in a browser to preview visual layouts and flows.)
- **Architecture / concept document**: `mobile/AI_Powered_Literacy_Platform_Rwanda.pdf`
- **Figma mockups** (if available):  
  > Add your Figma link here, for example:  
  > `https://www.figma.com/file/xxxxxxxx/MenyAI-Designs`  
- **Circuit / system diagram**


<img width="782" height="2584" alt="circuit diagram" src="https://github.com/user-attachments/assets/4a279c27-dc58-4ed8-8c52-e45247f40227" />


- - **Screenshots of app interfaces**:  
  > Place screenshots under a folder like `docs/screenshots/` and reference them here:
  > - `docs/screenshots/login.png`
  > - `docs/screenshots/home.png`
  > - `docs/screenshots/practice.png`

## Environment & setup

### Prerequisites

- **Node.js** (LTS recommended, e.g. 18+)
- **pnpm** package manager  
  ```bash
  npm install -g pnpm
  ```
- **Expo tooling**  
  You can use the Expo CLI or run via `pnpm` scripts.
- **Mobile device or emulator**:
  - Android device with Expo Go app installed, or
  - iOS device with Expo Go, or
  - Android/iOS emulator/simulator.

### Install dependencies

From the **repo root**:

```bash
pnpm install
```

This will install dependencies for the workspaces (including `mobile/`).

Alternatively, from the **mobile app folder**:

```bash
cd mobile
pnpm install
```

### Run the app

From the **repo root**:

```bash
pnpm start
```

Or from **`mobile/`**:

```bash
cd mobile
npm install -g pnpm
pnpm install
pnpm start
```

Then press **a** (Android) or **i** (iOS), or scan the QR code with Expo Go.

## Project structure

```text
mobile/
├── app/              # Expo Router (tabs + stack)
├── components/ui/    # Button, Card, Input
├── data/mock.ts      # Mock data – replace with Firebase when ready
├── lib/firebase.ts   # Firebase config (add keys)
├── theme.ts
└── package.json
```

Other notable files:

- `menyai-ui-design.html` – static HTML representation of UI design
- `mobile/AI_Powered_Literacy_Platform_Rwanda.pdf` – conceptual / architecture document

## Commands

From the project root:

- `pnpm start` or `pnpm mobile` – Start Expo from root
- `pnpm typecheck` – Run TypeScript checks (in `mobile/`)
- `pnpm format.fix` – Run Prettier formatting

You can also run equivalent commands inside `mobile/` if preferred.

## Mock data

All content currently comes from **`mobile/data/mock.ts`**:

- Lessons, levels, progress, and user details are hard-coded.
- This makes the app easy to run locally without any backend.

When you connect a real backend, you can replace these mocks with data fetched from your API or Firebase.

## Firebase & backend roadmap

Firebase is planned as the primary backend for:

- **Authentication** (phone + PIN methods)
- **Firestore/Realtime Database** for lessons, levels, and user progress
- **Storage** for media assets (images, audio)

Steps to enable Firebase:

1. Create a project at [Firebase Console](https://console.firebase.google.com).
2. Add Android/iOS apps and copy the config.
3. Edit **`mobile/lib/firebase.ts`**: uncomment the code and set the `firebaseConfig`.
4. Gradually replace usage of `mobile/data/mock.ts` with live Firestore/REST calls.

## Deployment plan

### Short term (development & testing)

- Run the app with **Expo Go** using `pnpm start`.
- Test on:
  - Real Android/iOS devices (recommended), or
  - Emulators/simulators on your development machine.
- Iterate on UI, UX, and content using the mock data layer.

## Video Demo
this is the link to access the demo : https://github.com/Ms-Lina/menyaa/blob/main/Video%20Demo
