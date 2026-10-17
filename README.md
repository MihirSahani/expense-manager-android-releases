# Finance Manager

An expense manager for Android that builds your transaction history from bank SMS and helps you stay within a budget. Your financial data is stored only on your phone.

[Download the latest release](../../releases/latest) · [Report an issue](../../issues)

---

## Overview

Finance Manager reads the transaction SMS your bank sends you, records each debit and credit against the right account, and files it under the category you last used for that payee. Budgets, bills, loans and savings goals are built on top of that history, so most of your records stay up to date without manual entry.

The app requires a subscription and a Google sign-in. These are used only to manage the subscription. Transactions, balances and SMS never leave the device.

## Features

- **Automatic tracking from bank SMS.** New messages are processed as they arrive, and existing ones are imported during setup. Duplicates and multi-part messages are handled.
- **Budgets by cycle.** Set a budget per category, using calendar months or a cycle that starts on your salary date.
- **Analysis.** Spending is grouped into necessities, discretionary spending and investments, with a daily spending heatmap for the current cycle.
- **Accounts and cards.** Track multiple bank accounts and credit cards with automatically updated balances. Link debit cards to the account they draw from.
- **Bills.** Track recurring payments that repeat every 1, 3, 6 or 12 months. The app sets money aside for each bill until it's due, matches the payment when it arrives, and suggests bills from your payment history.
- **Loans.** Record money you have lent or borrowed. A loan can be repaid in installments, using an interest rate and term, a fixed EMI, or amounts you enter for each month. Each installment is tracked as it is paid.
- **Savings funds.** Track progress towards savings goals.
- **Hide amounts.** Mask all figures on screen with one setting.
- **Daily summary.** An optional notification with the day's spending, at a time you choose.
- **In-app updates.** New versions are offered from within the app.

## Pricing

| Plan | Price |
|---|---|
| Monthly | ₹30 per month |
| Yearly | ₹300 per year |

- Payment is by UPI AutoPay through Razorpay. You approve the mandate once in your UPI app, and it renews automatically.
- You can cancel AutoPay at any time from the Subscribe screen. Time you have already paid for remains available.
- There is no free trial.
- **Referrals.** Share your referral code from the Subscribe screen. When a friend who entered your code makes their first payment, you and your friend each receive 30 extra days.

## Privacy

| Data | Where it goes |
|---|---|
| Transactions, balances, accounts, budgets, bills, loans, funds and bank SMS | Stays on your phone. It isn't uploaded anywhere, and it's excluded from Android cloud backup. |
| Google account email and account ID | Sent to the Finance Manager subscription service at sign-in, to identify your subscription. |
| Device identifier (Android ID) | Sent to the subscription service at sign-in, to record which devices use your account. |
| Payment details (UPI ID, phone number) | Entered on Razorpay's page and processed by Razorpay. The subscription service receives only the payment reference, plan and amount. |
| Update check | The app asks GitHub for the latest release on this page. GitHub can see your IP address, as with any website request. |

The app contains no advertising, analytics or crash-reporting libraries. Messages from senders that aren't known banks are ignored and never stored.

## Permissions

| Permission | Purpose | If denied |
|---|---|---|
| Read SMS (`READ_SMS`) | Imports existing bank transaction messages during setup. | The app can't be set up. SMS access is required. |
| Receive SMS (`RECEIVE_SMS`) | Records new bank messages as they arrive. | The app can't be set up. SMS access is required. |
| Notifications (`POST_NOTIFICATIONS`) | The optional daily summary and the notification to reopen the app after an update. | No notifications. Everything else works. |
| Internet (`INTERNET`) | Sign-in, the subscription, and checking for and downloading updates. | Granted automatically by Android. |
| Install apps (`REQUEST_INSTALL_PACKAGES`) | Passes a downloaded update to Android's installer. You confirm each install. | You can still update by downloading the APK from this page. |

The app doesn't request access to contacts, location, camera, microphone, storage, phone or call logs.

## Data storage

**On your phone**, in the app's private storage, which is deleted when you uninstall the app:

| Data | Source |
|---|---|
| Your name | Taken from your Google account during setup, and used only for greetings. |
| Accounts, transactions and the text of each bank SMS | Bank SMS, your confirmations, and manual entries. |
| Categories, budgets, bills, loans and savings funds | Entered by you. |
| Payee-to-category and card-to-account preferences | Learned from your choices. |
| Settings, sign-in session and subscription licence | Your choices, and the subscription service. |

If you move to a new phone with Android's device-to-device transfer, the app's data is copied directly between the devices.

**On the subscription service:**

| Data | Purpose |
|---|---|
| Email address and Google account ID | Identify your account. |
| Android IDs of devices you have signed in on | Account security and abuse prevention. |
| Subscription dates, and Razorpay subscription and payment references with amounts and refunds | Grant access and keep payment records. |
| Your referral code, and the code you entered | Apply referral rewards. |
| A history of changes to your access | Support and dispute resolution. |

Sign-in sessions expire after 90 days. Your account data is kept until you ask for it to be deleted (see [Support](#support)). If you delete your account, any active subscription is cancelled, and the unused part of your latest payment is refunded. Payment records are kept without your name, as tax law requires.

## Supported banks

Transaction SMS are recognised from these banks:

Allahabad Bank, American Express, Andhra Bank, Axis Bank, Bank of Baroda, Bank of India, Bank of Maharashtra, Canara Bank, Central Bank of India, Citi, Federal Bank, HDFC Bank, HSBC, ICICI Bank, IDBI Bank, IDFC First Bank, India Post, Indian Bank, Indian Overseas Bank, IndusInd Bank, Kotak Mahindra Bank, Oriental Bank of Commerce, Paytm Payments Bank, Punjab National Bank, RBL Bank, SBI, SBI Card, Standard Chartered, UCO Bank, Union Bank of India and Yes Bank.

If your bank isn't listed, or a message wasn't recognised, please [open an issue](../../issues).

## Installation

**Requirements:** Android 10 or later.

1. Download the latest `.apk` file from [Releases](../../releases/latest).
2. Open the file. If Android asks, allow installs from your browser or file manager.
3. Open Finance Manager, grant SMS access, and sign in with Google.
4. Review the accounts and payees the app found in your SMS, then subscribe to start using the app.

## Updates

- When a new version is available, the app shows its release notes and offers to install it. Your data is kept.
- After the update installs, tap the notification to reopen the app.
- To check manually, go to **Settings > App Version**.
- Every release is signed with the same key, so Android only installs updates that come from this project.

## Support

Use [GitHub Issues](../../issues) for:

- **Bug reports and feature requests.**
- **Unrecognised SMS.** Paste the message with account numbers, amounts and reference numbers removed.
- **Data requests.** Ask for a copy of your subscription data, or for your account to be deleted. Don't post your email address. The maintainer will follow up to verify your request.

## Source code

The source code isn't public. You can check the privacy claims on this page yourself:

- **Permissions.** Go to **Settings > Apps > Finance Manager > Permissions** to see exactly what Android has granted.
- **Network use.** Inspect or restrict the app's traffic with a firewall such as [NetGuard](https://netguard.me/). It connects only to the subscription service, Razorpay (while you subscribe), Google (for sign-in) and GitHub (for updates).
