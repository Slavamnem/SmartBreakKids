# Privacy Policy - SmartBreak Kids

Effective date: 2026-05-06

This Privacy Policy explains what data SmartBreak Kids processes, why it is needed, and how permissions are used.

## 1. Data Controller

Project: SmartBreak Kids  
Contact: use in-app Support form (Profile -> Support)

## 2. Data We Process

### 2.1 Account data (Google Sign-In)
- Display name
- Email address

Purpose:
- authentication in the app;
- showing account information in Profile;
- identifying support requests.

### 2.2 App settings (stored locally on device)
- selected task types;
- selected apps for training popups;
- frequency and active days;
- PIN and app state flags.

Purpose:
- provide app functionality;
- enforce selected training schedule and app lock behavior.

### 2.3 Usage access data (foreground app events)
- current foreground package name (from Usage Access APIs);
- event timing used to determine when to show a task.

Purpose:
- trigger task popup only for apps selected by parent;
- avoid repeated popups according to configured interval.

Important:
- this data is used in-app and is not sold to third parties.

### 2.4 Support and action logs sent to Telegram
When user sends a support message, app sends:
- user display name;
- user email;
- support message text.

When key in-app actions happen, app sends action text only (for example: login, logout, language change, switches, section entry).

Recipient:
- Telegram Bot API (third-party service).

Purpose:
- support handling;
- operational diagnostics and audit of key app actions.

## 3. Permissions and Why They Are Needed

### `android.permission.SYSTEM_ALERT_WINDOW`
Why needed:
- to display training task UI over selected apps.

What would break without it:
- task popup cannot appear on top of other apps.

### `android.permission.PACKAGE_USAGE_STATS`
Why needed:
- to detect foreground app and compare it against parent-selected list.

What would break without it:
- app cannot reliably detect when selected app is opened.

### `android.permission.FOREGROUND_SERVICE`
### `android.permission.FOREGROUND_SERVICE_DATA_SYNC`
Why needed:
- to run app monitoring in a foreground service with persistent notification.

What would break without it:
- background monitoring can be suspended by OS and task triggering becomes unreliable.

### `android.permission.INTERNET`
Why needed:
- Google Sign-In network flow;
- sending support/action messages to Telegram bot endpoints.

What would break without it:
- login and support/action delivery will not work.

## 4. Legal Basis

Processing is based on:
- user consent for optional features requiring special access;
- legitimate interest to provide core parental-control behavior configured by user.

## 5. Data Retention

- Local settings are stored on device until user clears app data or uninstalls app.
- Telegram messages are stored by Telegram according to Telegram policies and by bot recipient chat history.

## 6. Data Sharing

We do not sell personal data.

Data is shared only with:
- Google services for authentication (when user signs in);
- Telegram Bot API for support and action notifications.

## 7. Children and Parents

SmartBreak Kids is intended for parental setup and supervision.  
Parent/guardian is responsible for enabling permissions and configuring blocked apps.

## 8. Security

We use platform APIs and standard HTTPS communication to external services.

Note:
- any secret embedded in client code can be extracted. Production deployment should move bot secrets to a backend.

## 9. User Rights

User can:
- revoke overlay and usage access in Android Settings;
- clear local app data in Android Settings;
- stop using app by uninstalling it;
- contact support to request deletion of support-related records where applicable.

## 10. Policy Updates

We may update this Policy when app functionality or data flows change.  
The latest version is published in this file.

