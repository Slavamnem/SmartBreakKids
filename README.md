# SmartBreak Kids

**SmartBreak Kids** is a parental-control Android app that turns screen time into learning time. When a child opens a selected app (game, social media, etc.), a quick educational task pops up — the child must solve it to continue using the app.

---

## Features

- 🔒 **App blocking with tasks** — parent selects which apps trigger a task popup
- 🧠 **Educational tasks** — math, logic, Schulte table, colors, and more
- 👶 **Child age settings** — task difficulty adapts to the child's age
- 📅 **Schedule** — set active days and task frequency
- 📊 **Statistics** — track daily and weekly task results
- 🔐 **PIN protection** — app settings are protected by a PIN code
- 🌍 **Multilingual** — English, Russian, Ukrainian
- 👤 **Google Sign-In** — parent account for setup and management

---

## How It Works

1. Parent installs the app and signs in with Google
2. Parent configures which apps trigger tasks, selects task types, sets frequency and active days
3. Parent enables task blocking and protects settings with a PIN
4. When a child opens a selected app, a task appears on top — the app stays blocked until the task is solved correctly

---

## Permissions

| Permission | Why it is needed |
|---|---|
| `SYSTEM_ALERT_WINDOW` | Display task popup over selected apps |
| `PACKAGE_USAGE_STATS` | Detect which app is in the foreground |
| `FOREGROUND_SERVICE` | Keep monitoring running reliably in the background |
| `INTERNET` | Google Sign-In and support message delivery |

> Usage Access must be granted manually by the parent in Android Settings.

---

## Requirements

- Android 7.0 (API 24) or higher
- Google account for Sign-In

---

## Privacy

SmartBreak Kids does not sell or share personal data.

- All settings are stored locally on the device
- Google account data is used only for authentication
- Support messages (including display name and email) are sent to the developer via Telegram Bot API for support handling

Full Privacy Policy: [PRIVACY_POLICY.md](PRIVACY_POLICY.md)

---

## Package

`com.smartbreakkids.app`

---

## Tech Stack

- Kotlin
- Jetpack Compose
- Foreground Service
- Overlay (SYSTEM_ALERT_WINDOW)
- Usage Stats API
- Google Sign-In
- Cloudflare Workers (support & action log relay)

---

## License

Private project. All rights reserved.

