# 🔔 Auto Join Reminder for Microsoft Teams Meetings via Power Automate + Pushbullet

This Power Automate flow automatically sends you a **push notification** when a Microsoft Teams meeting is about to start — including a direct link to join.

Notifications are sent through **Pushbullet** to your device (e.g. phone, tablet, or browser).

---

## 🚀 Features

* ⏱ Detects upcoming Outlook calendar events (default: 3 minutes before start)
* 🔍 Extracts the **Teams meeting URL** from the event description
* 📲 Sends a **Pushbullet notification** with the join link
* 🧠 Fully automated, runs silently in the background

---

## 🛠️ Setup Guide

### 1. Requirements

* Microsoft 365 account with Outlook
* Access to [Power Automate](https://flow.microsoft.com)
* A [Pushbullet account](https://www.pushbullet.com)
* A registered Pushbullet device (e.g. smartphone or Chrome extension)
* Your **Pushbullet API token** and **device ID**

---

### 2. Import the Flow

1. Open [Power Automate](https://make.powerautomate.com)
2. Go to **"My flows" > "Import"**
3. Select the `OpenTeamsMeetingwhenitisabouttostart.zip` file
4. Ensure the following connections are configured:

   * Office 365 Outlook
   * HTTP (for Pushbullet request)

---

### 3. Configure Pushbullet

1. Go to: [Pushbullet Settings](https://www.pushbullet.com/#settings)
2. Copy your **Access Token**
3. Find your **device ID** via the [API Docs](https://docs.pushbullet.com/#devices)
   or directly from [https://api.pushbullet.com/v2/devices](https://api.pushbullet.com/v2/devices)
4. In the flow, locate the `Http` action (Push notification step) and replace:

   * `"Access-Token"` with your token
   * `"device_iden"` with your device ID

---

### 4. Optional Customization

* Want to use Telegram, Discord, or something else? Replace the HTTP step.
* Change the lead time (default is 3 minutes) in the trigger step if needed.

---

## 📁 Files Included

* `OpenTeamsMeetingwhenitisabouttostart.zip` – Ready-to-import Power Automate flow
* `README.md` – Setup and usage instructions

---

## 🔐 Privacy Note

This flow processes your calendar data within Microsoft Power Automate only. Your meeting info is sent solely to your personal Pushbullet account.

---

## 💬 Need Help?

If you need assistance or want to tweak this flow for your setup, feel free to reach out. Let’s automate the boring stuff. 🚀
