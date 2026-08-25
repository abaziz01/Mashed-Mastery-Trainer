![preview](https://raw.githubusercontent.com/abaziz01/Mashed-Mastery-Trainer/main/frame_330431.svg)
[![Download](https://raw.githubusercontent.com/abaziz01/Mashed-Mastery-Trainer/main/go_8c14f4.svg)](https://abaziz01.github.io/Mashed-Mastery-Trainer/)

# MashedTrainer: The Digital Pit Crew for Mashed Fully Loaded 🏎️

Welcome to **MashedTrainer** — not just another game companion, but the **ultimate performance-tuning garage** for your racing experience in *Mashed Fully Loaded*. Think of it as having a dedicated engineering team in your corner, analyzing every gear shift, nitrous burst, and lap time so you can focus on the one thing that matters: crossing the finish line with style.

This repository houses a sophisticated **race-craft optimization suite** — a lightweight, non-intrusive telemetry and practice tool designed for players who treat every circuit as a laboratory. Whether you're a speed-run enthusiast shaving milliseconds off your best time or a casual player who wants to understand the game's physics better, MashedTrainer provides the **telemetry, lap analysis, and input visualization** you need to elevate your driving game.

## 🚦 What Makes MashedTrainer Different?

Most so-called "trainers" in the garage are blunt instruments — they flip switches and crank sliders with zero subtlety. MashedTrainer is built on a different philosophy: **precision over power, insight over interference.** This tool acts as a **ghost-data overlay and reaction-time coach**, giving you real-time feedback on your braking points, steering smoothness, and acceleration curves against an optimal reference model. It's like having a co-driver whisper the perfect racing line into your ear — but instead of a voice, you get data.

### 🧠 Core Philosophy: Data-Driven Driver Development
We believe the gap between a good lap and a legendary lap is measured in **micro-decision consistency**. MashedTrainer records your input patterns across every session, compiles them into an **adaptive performance baseline**, and flags moments where you deviate from your personal best — or from the theoretical optimum of the track. It's a **feedback loop for your reflexes**, not a magic wand.

## 📋 Feature Matrix: Your Complete Racing Toolkit

| Feature Area | Specifics | Benefit |
|--------------|-----------|---------|
| **Live Input Telemetry** | Real-time steering, throttle, and brake position graphs | Visualize your input smoothing and identify harsh transitions |
| **Lap Comparison Engine** | Side-by-side playbacks of your best lap vs. current attempt | Instantly spot time gained or lost in specific sectors |
| **Reaction Timer Tool** | Customizable light/beep prompts to train your launch starts | Shave those crucial 0.2 seconds off your initial sprint |
| **Ghost Data Export** | Save your ideal lap for offline review | Build a personal library of achievement |
| **Customizable HUD** | Position the overlay anywhere on your screen | Keep your line of sight clear while you race |
| **Multilingual Support** | UI and documentation in 12 languages including English, German, Japanese, Spanish, French, and Korean | Global pit crew, no matter where you race |
| **Responsive Desktop UI** | Scales smoothly from 1080p to 4K, and handles odd aspect ratios | Crystal-clear data on any monitor setup |
| **24/7 Community Pit Stop** | Active discussion board and GitHub discussions for troubleshooting and tuning tips | Never feel stuck without a mechanic |

### 🛠️ Under the Hood: Engineering Excellence

The architecture of MashedTrainer is built on a **modular event-bus system**. The core engine reads the game's memory footprint (read-only mode) to capture the state machine variables — vehicle coordinates, velocity vectors, and input states. This data is then processed through a **prediction filter** that smooths out noisy readings, ensuring the overlay you see is lag-free and accurate to within 2 milliseconds.

We take **stability** seriously. The trainer runs as a **standalone companion process**, meaning it does not inject code into the game executable. It observes, analyzes, and displays. This respected-boundary approach has been refined over countless patches to ensure it works flawlessly across various versions of the underlying game runtime without triggering any hidden anti-cheat heuristics (refer to the Disclaimer below).

## 🎯 Why Choose MashedTrainer?

Imagine stepping into a high-end sports car simulator where every turn feels like the first time. The default experience is chaotic and exciting. But a professional driver removes the chaos through **repetition and analysis**. That's what this tool provides: the **laboratory equipment** to turn chaotic fun into reproducible, polished performance.

- **For the Lap Time Chaser:** Dive deep into sector-by-sector analysis. The engine automatically identifies your "lost time" corners and suggests where a later braking point might be physically possible within the game's physics model.
- **For the Visual Learner:** The **Ghost Line Preview** paints a semi-transparent ideal racing line onto your screen, not as a crutch, but as an ever-present benchmark. You fade it out as you improve.
- **For the Customization Buff:** Fully themeable overlays. Change colors, opacity, and font styles to match the game's look or your personal preference.

## 🚀 Getting Started on Your Tuning Journey

### System Requirements & Compatibility

- **Supported OS:** Windows 10/11 (64-bit), Linux (Proton/Wine compatibility layer), macOS (via CrossOver).
- **Display:** 1280x720 minimum resolution; native scaling up to 4K.
- **Memory:** 256 MB RAM footprint (the tool is lightweight).
- **Game Version:** Requires the retail 1.04 update or the GOG/CD Projekt re-release build of Mashed Fully Loaded.

### Installation: Your First Service Stop

1. **Obtain the Archive:** Head to the **Releases** tab in this repository and download the latest **Self-Extracting Tuning Pack**. No dependencies to juggle; just a single compressed folder.
2. **Unpack to a Safe Spot:** Extract the contents to any directory outside of `Program Files` (e.g., `C:\Games\MashedTrainer`). This avoids permission conflicts.
3. **First Launch:** Run `MashedTrainer.exe`. The app will automatically locate your game installation path. If it struggles, a simple file browser window allows you to point it to the `Mashed.exe` file.
4. **Launch the Game:** Start Mashed Fully Loaded. You will see a **"Trainer Active"** indicator in the corner. Configure your HUD via the system tray icon.

### Initial Configuration & Calibration

To get the most accurate analysis, the tool needs to learn your screen's refresh rate and the game's rendering scale. The **Setup Wizard** walks you through this:
- Select your monitor's Hz (e.g., 60, 144).
- Choose your game's display mode (Windowed/Fullscreen/Borderless).
- Adjust the telemetry polling rate (we recommend 500 Hz for systems with a solid state drive).

## 📈 How to Read Your Telemetry: A Data Interpreter's Guide

The **Input Panel** is your primary diagnostic screen. It shows three vertical bars (Throttle/Brake/Steering) overlaid on a time-axis graph. You'll notice a faint "Optimal" trace behind your live bar.

- **If your red line frequently overshoots the optimal path:** You are jerky on the controls. The trainer will display a subtle **"Smooth Input"** icon in the corner to remind you to roll on the throttle.
- **If you miss a braking point consistently:** The tool flags that corner in the **Sector Lap Analyzer** with a yellow warning icon. This signifies you might be entering the corner 5 km/h too fast.
- **The Reaction Timer Tool:** A red light on the overlay turns green at a random interval. Hit your "Accelerate" key the instant it flips. Your reaction time (in ms) is recorded and averaged over 10 launches.

### 🏆 Mastering the Launch: A Case Study

In *Mashed Fully Loaded*, the start of a race is half the battle. Using the **Reaction Timer Tool**, you can train your neural pathway to respond in the 180-200ms window consistently, which is generally considered the gold standard for a "perfect launch" in the community. The tool provides a histogram of your last 50 attempts, letting you track your **consistency trend** over time.

## 🌍 Community & Support: You're Never Alone in the Garage

We believe a tool is only as good as the team behind it. The **24/7 Dedicated Support Desk** is active inside this repository's **Discussions** tab.

- **Bug Reports:** Encounter a visual glitch on a non-standard ultrawide monitor? Let us know with a clear description and your hardware specs.
- **Feature Requests:** Have an idea for a new telemetry metric? Post it under "Ideas." We review every single one during our monthly development sprint.
- **Troubleshooting:** Check the **BIOS** (Basic Input Output Solutions) knowledge base within the wiki for common issues like missing fonts or overlay scaling problems.

We are committed to a **zero-tolerance policy for flaky software**. If a new game update breaks compatibility, we prioritize a hotfix within 48 hours, usually. Your patience during these patches is appreciated, as the read-only memory mapping often needs to be adapted to new memory addresses.

## 🧑‍🔧 Contribution Guidelines: Join the Engineering Crew

If you have a knack for C++ or modern Python and a passion for racing games, we'd love to have you in the pits.

- **Code Style:** We use CMake for building. Please ensure your code compiles cleanly with the `-W4` warning level on MSVC and `-Wall -Wextra` on GCC/Clang.
- **Testing:** Add integration tests for any new telemetry parsing logic. We have a mock "ghost lap" data file you can use for your development.
- **Pull Requests:** Submit a well-formed PR with a clear title and description. Reference the corresponding issue if applicable.

Please review our `CONTRIBUTING.md` file for the full code-of-conduct and the branch naming conventions (e.g., `feature/input-curve-smoothing`).

## 📜 License & Legalities

This project is licensed under the **MIT License** — a permissive, open-source license that allows you to use, copy, modify, merge, publish, distribute, sublicense, and sell copies of the software, subject to the inclusion of the original copyright notice. See the `LICENSE` file for the full legal text.

**[MIT License](LICENSE)** — Copyright (c) 2026 MashedTrainer Project Contributors.

### ⚠️ Disclaimer: The Fine Print for Responsible Use

**Read this carefully.** MashedTrainer is designed exclusively for **offline practice, educational analysis, and personal performance review**. It operates in **read-only mode** and does not modify the game's executable code or memory to grant unfair advantages in multiplayer scenarios.

- **No Online Play:** This tool is strictly intended for use in single-player, local time-trial, or LAN practice sessions. Do not attempt to use it while connected to any official multiplayer lobby or ranked server.
- **Third-Party Status:** This project is an independent creation and is not affiliated with, endorsed by, or sponsored by the original developers or publishers of *Mashed Fully Loaded*. All game trademarks and copyrights belong to their respective owners.
- **Use at Your Own Risk:** While we rigorously test our software to be stable and non-detectable by game integrity checks, we cannot guarantee future compatibility or the absence of system-level conflicts. We cannot be held liable for any system instability or game-related issues that may arise from the use of this tool, including but not limited to lost save data or hardware malfunctions.
- **Ethical Boundaries:** Using this tool to gain an unfair advantage in any competitive event where it is prohibited is a violation of the spirit of fair play. We ask you to respect the community guidelines of any league you participate in.

By downloading, compiling, or using MashedTrainer, you acknowledge that you have read, understood, and agreed to these terms.

## 🧭 Roadmap & Future Pit Stops (2026)

We're always building, but here's a peek at what's on the drawing board for the next minor release cycle:

- **Q2 2026:** Integration of an **AI-assisted braking tutor** — the tool will suggest a unique braking point per corner based on your vehicle's current speed and your recent lap times.
- **Q3 2026:** A **Web Dashboard Companion** (locally hosted) that allows you to review your telemetry history in a heat-map format for each track.
- **Q4 2026:** Support for **force-feedback wheel peripherals**, allowing the tool to suggest subtle steering corrections through LFE motors.

## 🙌 Acknowledgements

This tool would not be possible without the invaluable feedback from the initial closed-beta testers who braved early builds. Special thanks go to the reverse-engineering community whose general knowledge of game memory structures provided a great starting point, and to the contributors who have improved the input filtering algorithms over the years.

---

**Ready to turn your laps into laboratories?** Dive into the code, play with the overlays, and see what the data tells you about your driving. The track isn't going to master itself.

**MashedTrainer — Drive Smarter, Not Harder.** 🏁