# subathon-timer

# Subathon Timer for Streamlabs OBS

A custom subathon timer that automatically adds time for Twitch bits, subs, and channel points. You can customize fonts, colors, and background transparency via the settings panel.

---

## Features

- Automatically adds time based on bits, subs, and channel points
- Customizable font (paste any Google Fonts link)
- Customizable colors and transparent background option
- Manual time addition and subtraction via text input
- Pause and resume timer
- Notifications for special redemptions (e.g., spin the wheel)
- Designed to be used with Streamlabs OBS Browser Source

---

## Getting Started

### Step 1: Download or clone this repository

Download the `subathon.html` file or clone this repo to your computer.

### Step 2: Open the code in a text editor

Open `subathon.html` in a simple text editor like Notepad (Windows), TextEdit (Mac), or VSCode.

---

## Step 3: Add your Twitch and Streamlabs tokens

To allow the timer to automatically add time when viewers redeem bits, subs, or channel points, you need to add **your own tokens** into the code.

Look near the top of the file for this section:


// ====== CONFIG - tokens and channel ID - CHANGE THESE ONLY ======
const CONFIG = {
  STREAMLABS_TOKEN: "YOUR_STREAMLABS_SOCKET_TOKEN_HERE",
  TWITCH_OAUTH_TOKEN: "YOUR_TWITCH_OAUTH_TOKEN_HERE",
  TWITCH_CHANNEL_ID: "YOUR_TWITCH_CHANNEL_ID_HERE"
};
Replace the placeholder strings with your actual tokens including the quotation marks.

How to get your tokens and channel ID
Streamlabs Socket Token:

Log into your Streamlabs Dashboard. https://streamlabs.com/login?r=https://streamlabs.com/dashboard

Go to Settings → API Settings.

Copy your Socket Token.

Twitch OAuth Token:

Visit Twitch Token Generator. https://twitchtokengenerator.com/

Log in with your Twitch account.

Generate a token with these scopes/permissions:

chat:read

channel:read:redemptions

user:read:subscriptions

Copy the generated token.

Twitch Channel ID:

Visit [Twitch ID Finder.](https://www.streamweasels.com/tools/convert-twitch-username-%20to-user-id/)

Enter your Twitch username.

Copy your numeric channel ID.

Example:
js
Copy
Edit
const CONFIG = {
  STREAMLABS_TOKEN: "abcd1234-your-streamlabs-token-xyz",
  TWITCH_OAUTH_TOKEN: "oauth:abcdef123456-your-twitch-oauth",
  TWITCH_CHANNEL_ID: "123456789"
};
Step 4: Save your changes
Save the file after you paste in your tokens.

Step 5: Add the timer as a Browser Source in Streamlabs OBS
Open Streamlabs OBS.

Add a new Browser Source.

For the URL, either upload your edited subathon.html to a web host or point directly to the local file path.

Set the width and height as desired (e.g., 800x200).

Load the source. The timer will connect automatically and start responding to bits, subs, and channel points.
