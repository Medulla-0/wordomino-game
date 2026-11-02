# Wordomino

A Turkish word-puzzle game for Android, designed and built by me in Unity 6 and C#. It combines Wordle-style word guessing with block placement on an 8x8 board.

**Status:** Google Play closed testing. Playable APK below.
**Role:** Solo developer (design, gameplay code, UI, release). Built with an AI-assisted workflow; I own the design decisions and can walk through every system.
**Source code:** private. I'm happy to walk through it on a call or screen share.

> Add here: 20-40 second gameplay GIF or video, then 3-4 screenshots.
> `![Gameplay](docs/gameplay.gif)`

---

## What I built

| Area | What's in it |
|---|---|
| **Gameplay** | 8x8 board, hidden Turkish words with Wordle-style feedback, move limit per word, shared cells, stones, hammer / refresh / next-word helpers |
| **Input and UI** | Drag-and-drop letter placement, UI built in code (uGUI, TextMeshPro), code-driven animations |
| **Letter bag** | Weighted by Turkish letter frequency, avoids recent repeats, always keeps a usable letter on the board so the player is never stuck |
| **Difficulty** | Adapts to a player skill profile (speed, solve rate, idle time). Gentler onboarding for new players. I tuned the algorithm using data from closed testing |
| **Save system** | Full board, words, letter queue and difficulty state saved every move and restored exactly. Free resume within 30 minutes, rewarded ad after that |
| **Telemetry** | Custom event pipeline (offline queue, batched upload, retry with backoff) alongside Unity Analytics. Data sharing is opt-in |
| **Ads and compliance** | AdMob rewarded and interstitial ads with frequency caps, Google UMP consent, Android 13+ notification permission, age gate and child mode (non-personalized ads, analytics off) |
| **Release** | IL2CPP, ARM64, R8 shrinking, AAB build for Google Play |

## Tech

Unity 6, C#, 2D URP, uGUI, TextMeshPro, Android (IL2CPP, min API 25), AdMob, Google UMP, Unity Analytics, Git/GitHub.

## Try it

1. Download [`Wordomino-1.0.1.apk`](Wordomino-1.0.1.apk) (about 54 MB). It would be better to also publish it under **Releases**.
2. Allow installs from your browser, then open the file. Android 7.1 or newer is required.
3. Android may show an "unknown app" warning. The app comes from this repo.

Saved games and settings stay on your phone.

## About the author

I'm Mehmet Ataberk Birinci, a game design student in Istanbul. I build games and the backend systems behind them.
[LinkedIn](https://www.linkedin.com/in/mehmet-ataberk-birinci-168946225/) · birinciataberk@gmail.com

## Credits and licenses

- Word list based on Vikisözlük, licensed CC BY-SA 4.0.
- Sounds and graphics are generated in code at runtime.
- Privacy policy: https://labglide.com/wordomino/privacy
- All rights reserved. See `LICENSE`.

---

## Türkçe özet

Wordomino, Unity 6 ile tek başıma tasarlayıp geliştirdiğim bir Android kelime bulmaca oyunudur: Wordle tarzı kelime tahmini ile blok yerleştirmeyi birleştirir. Şu an Google Play kapalı testinde. Kaynak kod gizli, isteyene ekran paylaşımıyla anlatırım. APK yukarıdaki bağlantıda.
