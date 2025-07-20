# ComaTool (YouTube-to-Twitch Chat Bridge) 🎮📺

A Python-based bot that listens to a **YouTube livestream chat** and forwards any messages that start with a `!` command (like `!bsr`) into a **Twitch channel's chat**.

---

## 🌟 Features
- Reads messages from a specified YouTube livestream
- Sends matching messages to your Twitch channel chat
- Easy to customize and extend
- Ideal for streamers who want cross-platform chat interaction

> ✅ Originally developed for Beat Saber song requests (`!bsr`) but can be used for any command system!

---

### 🔧 Installation

Go to releases and download the .exe file.

---

### 🔴 YouTube Setup

You only need:

- `YOUTUBE_VIDEO_ID` – the ID of your livestream

#### How to find it:

1. Go to your YouTube livestream page.
2. Copy the part after `v=` all the way to the first `&` after it in the URL.
     Example: https://www.youtube.com/watch?v=   -> x7X9w_GIm1s <-   &t=1s&ab_channel=Fireship
