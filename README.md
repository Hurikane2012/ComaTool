# ComaTool (YouTube-to-Twitch Chat Bridge) 🎮📺

A Python-based bot that listens to a **YouTube livestream chat** and forwards any messages that start with a `!` command (like `!bsr`) into a **Twitch channel's chat**.

---

## ⚠️ Note About Sensitive Info

I want to sincerely apologize that this version of the bot requires you to manually provide sensitive credentials like your Twitch token, client secret, and user ID.

I understand this isn't ideal or secure for a public tool, and I take that seriously.

**The next version is already being planned**, and it will:
- No longer ask for any private credentials
- Be fully integrated as a secure Twitch Extension
- Only require a YouTube video link to work

Thanks for understanding — this first version is open-source so you can fully see what it does, and improvements are coming soon!

---

## 🌟 Features
- Reads messages from a specified YouTube livestream
- Sends matching messages to your Twitch channel chat
- Easy to customize and extend
- Ideal for streamers who want cross-platform chat interaction

> ✅ Originally developed for Beat Saber song requests (`!bsr`) but can be used for any command system!

---

## 🚀 Getting Started

### Requirements
- Python 3.11 or later (tested on Python 3.13)
- [PyCharm](https://www.jetbrains.com/pycharm/download) (recommended for setup and running)

> **Note:** This project was developed entirely in **PyCharm**, and we recommend using it for the best compatibility and ease of use.

---

### 🔧 Installation

1. Go to releases and download both .py files.
2. Ge [PyCharm](https://www.jetbrains.com/pycharm/download) if you haven't already.
3. In a new PyCharm project, import the two .py files.

---

## 🔑 Setup: Getting Required Keys

Before you can run the bot, you need to gather a few credentials from **Twitch** and **YouTube**.

---

### 🟣 Twitch Setup

You'll need the following:

- `TWITCH_TOKEN` – OAuth token for your bot
- `TWITCH_CLIENT_ID` – App Client ID from Twitch Dev Console
- `TWITCH_CLIENT_SECRET` – App Client Secret from Twitch Dev Console
- `TWITCH_USER_ID` – Your numeric Twitch User ID
- `TWITCH_CHANNEL` – Your Twitch channel name (lowercase)

#### Step-by-step:

1. **Create a Twitch Developer Application:**
   - Go to: [Twitch Console Apps](https://dev.twitch.tv/console/apps)
   - Click **"Register Your Application"**
   - Fill in:
     - **Name:** Anything (e.g. `yt-to-twitch-bot`)
     - **OAuth Redirect URLs:** `http://localhost`
     - **Category:** Chat Bot
   - Click **"Create"**

2. **Copy your Client ID and Client Secret**
   - These go into `TWITCH_CLIENT_ID` and `TWITCH_CLIENT_SECRET`

3. **Generate your OAuth Token (TWITCH_TOKEN):**
   - Use the following URL to start the manual token flow (replace `YOUR_CLIENT_ID`):
     ```
     https://id.twitch.tv/oauth2/authorize?client_id=YOUR_CLIENT_ID&redirect_uri=http://localhost&response_type=token&scope=chat:read+chat:edit+user:bot+user:write:chat
     ```
   - Log in and **authorize** the app
   - After being redirected, look at the URL bar:
     ```
     http://localhost/#access_token=xxxxxxxxxxxxxx&scope=...
     ```
   - Copy the entire `xxxxxxxxxxxxxx` part (From the `=` to the `&scope`) — that’s your `TWITCH_TOKEN`

4. **Get Your Twitch User ID (TWITCH_USER_ID):**
   - Run the included `user_id_generator.py` script (we provided it for you)
   - It will print your user ID to use in `TWITCH_USER_ID`

5. **Set Your Channel Name (TWITCH_CHANNEL):**
   - Just use your Twitch username in **lowercase** (e.g. `itscomatic`)

---

### 🔴 YouTube Setup

You only need:

- `YOUTUBE_VIDEO_ID` – the ID of your livestream

#### How to find it:

1. Go to your YouTube livestream page.
2. Copy the part after `v=` all the way to the first `&` after it in the URL.
     Example: https://www.youtube.com/watch?v=   -> x7X9w_GIm1s <-   &t=1s&ab_channel=Fireship
