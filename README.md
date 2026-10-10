---

# 💸 Finances: a private expense manager for Android

## Track your daily spending and stick to a monthly budget, without handing your financial life to anyone.**

Finances reads your bank SMS, turns them into transactions automatically, and shows you where your money goes, all **on your phone**. There's no sign-up, no cloud, no ads and no trackers.

---

## 🔒 Privacy at a glance

| | |
|---|---|
| ✅ **No account or sign-up** | Your name is only used to greet you, and it never leaves the device. |
| ✅ **No cloud sync, no cloud backup** | Your data isn't uploaded anywhere, not even to Google Drive backups. |
| ✅ **No ads, no analytics, no crash reporting** | The app contains no tracking or advertising libraries. |
| ✅ **Personal SMS are ignored** | Only messages from known bank sender IDs are processed. Everything else is skipped and never stored. |
| ✅ **Uninstalling removes everything** | All data lives in the app's private storage on your phone. |
| ℹ️ **One network request: the update check** | When you open the app, it asks GitHub whether a newer version exists. That's all. Details below. |

---

## ✨ What it does

- 📩 **Automatic tracking from bank SMS.** Debits and credits are picked up as they arrive, matched to the right account, and filed under the category you last used for that payee.
- 🗓️ **Budgets that follow your pay cycle.** Use calendar months, or a cycle that starts on your salary date.
- 🏷️ **Categories with budgets.** Set a budget per category and see how much is left this cycle.
- 📊 **Spending insights.** A breakdown of necessities, disposables and investments, plus a daily spending heatmap.
- 🏦 **Multiple accounts.** Balances stay up to date automatically.
- 🏛️ **Loans and 💰 savings funds.** Track money you've lent or borrowed, and progress toward savings goals.
- 🙈 **Hide amounts.** Mask every figure when someone's looking over your shoulder.
- 🔔 **Optional daily summary.** A notification with today's spending, calculated on your device.

---

## 🛡️ Permissions, and why each one is needed

| Permission | Why | If you deny it |
|---|---|---|
| **Read SMS** (`READ_SMS`) | Imports past bank transaction messages when you first set up the app. | No automatic import. You can still add everything by hand. |
| **Receive SMS** (`RECEIVE_SMS`) | Picks up new bank messages as they arrive, so transactions show up on their own. | New transactions aren't added automatically. |
| **Notifications** (`POST_NOTIFICATIONS`) | The optional daily spending summary. | No daily summary. Nothing else changes. |
| **Internet** (`INTERNET`) | **Only** used to check for and download app updates from this GitHub page. | Granted automatically by Android; you can block it with a firewall and the app works fully offline. |
| **Install apps** (`REQUEST_INSTALL_PACKAGES`) | Lets the app hand a downloaded update to Android's installer. You confirm every install yourself. | Android asks the first time. Say no and you can still update by downloading the APK here. |

The app does **not** ask for contacts, location, camera, microphone, storage, phone or call logs.

---

## 📦 What's stored on your phone

Everything below is kept only in the app's private storage. Other apps can't read it, and it's deleted when you uninstall.

| Data | Where it comes from |
|---|---|
| First and last name | You enter it during setup. It's only used for a greeting. |
| Accounts (name, balance, optional account number) | You enter them, or confirm ones detected from SMS. |
| Transactions (amount, date, payee, reference number, last digits of the account or card) | Bank SMS or manual entry. |
| The original text of each **bank** SMS | Kept alongside its transaction so you can see where it came from. Non-bank SMS are never stored. |
| Categories, budgets, loans and savings funds | You enter them. |
| Payee→category and card→account preferences | Remembered from your choices, so future transactions are filed automatically. |
| Settings (cycle type, currency, notification time, and so on) | You choose them. |

**Backups:** the app opts out of Android cloud backup, so your data is **not** uploaded to Google Drive. If you move to a new phone with Android's phone-to-phone transfer (cable or Wi-Fi), the app's data comes along, directly from device to device.

---

## 🌐 What leaves your phone

Only one thing: **the update check.**

When the app opens, it asks GitHub for the latest release on this page. If a newer version exists, it shows you the release notes and asks before downloading. As with visiting any website, GitHub can see your IP address and that a request was made.

**Nothing about you or your finances is ever sent:** no transactions, balances, SMS, names or device identifiers.

---

## 🏦 Supported banks

SMS from these senders are recognised: **SBI, HDFC, ICICI, Axis, Kotak, IDFC First, Canara, Bank of India, UCO, Union Bank, Indian Bank, Central Bank, Standard Chartered, Paytm Payments Bank** and **American Express**.

Messages from any other sender are ignored. Is your bank missing? [Open an issue](../../issues).

---

## 📲 Install

1. Download the latest `finances-vX.Y.Z.apk` from [**Releases**](../../releases/latest).
2. Open it. Android may ask you to allow installs from your browser or file manager. Allow it for this install.
3. Open Finances and follow the setup.

**Requirements:** Android 10 or newer.

## 🔄 Updates

When a new version is out, the app shows a short **"Update to vX.Y.Z"** dialog with the release notes:

- Tap **Update**, then confirm in Android's installer. Your data stays exactly where it is.
- The first time, Android asks you to allow Finances to install apps. This is so it can hand over the update.
- You can also check manually in **Settings → App Version**.

Every release is signed with the same key, so Android only accepts updates that genuinely come from this project.

---

## 🔍 About the source code

The source code is **private for now**. You don't have to take the claims above on trust, though; you can check them yourself:

- **Permissions:** go to **Settings → Apps → Finances → Permissions** to see the exact list Android granted.
- **Network use:** block the app with a firewall such as [NetGuard](https://netguard.me/) or your phone's built-in data controls. Everything except the update check keeps working.

---

## 💬 Feedback

Found a bug, an SMS that wasn't picked up, or have an idea? [Open an issue](../../issues). Please **remove account numbers and amounts** from any SMS you paste.

---
