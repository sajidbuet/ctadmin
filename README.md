# CTAdmin – Class Test Administration Tool
![logo](https://github.com/sajidbuet/ctadmin/blob/main/docs/favicon.png?raw=true)
A lightweight, browser-based tool for BUET EEE instructors to:
- **Generate seat plans** for different sections & seating patterns  
- **Run synced timers** with visual pie-chart display  
- **Audio cues** at start, 5 min remaining, and end (with customizable sound files)  
- **Mute / fullscreen / light & dark mode toggle**  
- **Dynamic scale slider** to adjust timer size in “large” mode  

---

## 🚀 Features

- **Seat-plan Generator**  
  - Choose section (A, B, C, A1, …), seating pattern (row/column, serpentine, random), start side & row  
  - Auto-renders a responsive table with chairs, blank columns & walkway  

- **Stopwatch-style Timer**  
  - User-set duration (minutes), Start/Pause/Reset controls  
  - Pie-chart SVG visualization with smooth countdown  
  - **Audio cues** (pre-loaded) at:  
    1. **Start** – `gong-start.mp3`  
    2. **5 min remaining** – `5min-bell.mp3` → `last-five-minutes.mp3`  
    3. **Finish** – `end-bell.mp3` → `please-stop-writing.mp3`  
  - **Mute** toggle to silence all cues  
  - **Fullscreen** toggle for distraction-free display  
  - **Theme** switcher (light ↔ dark)  
  - **Scale slider** (1× – 2.5×) visible only in “large” timer mode  

- **Responsive & Accessible**  
  - Mobile-friendly layout  
  - Semantic HTML & keyboard-accessible controls  
  - CSS custom properties for easy theming  

---

## 📦 Installation

Simply clone this repo (or copy the `CTadmin` folder) into your web host:

```bash
git clone https://github.com/<your-org>/ctadmin.git
cd ctadmin
```

## 🚀 Additional Feature Ideas

- [ ] **Accessibility Mode**: Provide high-contrast theme, larger controls, and ARIA labels for screen readers.
- [ ] **PDF Export**: Add a “Download Seat Plan” button to export the generated plan as a PDF.
- [ ] **Preset Templates**: Allow saving and loading of common timer durations or seat-plan configurations.
- [ ] **Live Sync**: Use WebSockets so remote proctors can see timer state & receive alerts in real time.


## 🛠️ Immediately Implementable Critical Features
- [X] **Pre count down** (add 3, 2, 1 countdown) - ✅ DONE
- [X] **Audio Volume Slider**  - ✅ DONE
  Provide a slider to adjust cue volume directly in the UI, rather than relying solely on system settings.
- [X] **Minimal Mode Toggle**   - ✅ DONE
  Offer a condensed UI toggle that hides all non-essential controls (only timer and seat-plan remain) for distraction-free exam environments.
- [X] **Maximize Timer Button**   - ✅ DONE 
  Pressing it would hide the seat plan, condense the controls and maximize the size of the timer (1.7x), full screen the window,  the maximize button is located beside the close button. once maximized, it would toggle the button to restore mode (restore previous values of expand/condense, full screen status, timer size, and seat plan visibility).
- [X] **Persistent Timer**  - ✅ DONE 
  Once timer starts, the end time will be saved in settings. On browser refresh or load, settings will be checked if the timer was running/paused. If timer was running, the end time and remaining time will be adjusted automatically. If timer was running it will continue to run.
- [ ] **Persistent Settings**  
  Store user preferences (theme, volume level, section, start-side, start-row, pattern, pre-countdown, mute, last-used duration, section choice) in `localStorage` so settings survive page reloads.
- [ ] **Auto–Save & Restore**  
  Automatically save the current timer state (running/paused, remaining time) and seat-plan configuration so accidental navigations don’t reset progress.
- [ ] **Flexible Class Mode**: Provide settings for setting the number of rows and columns of the classroom.
- [ ] **Keyboard Shortcuts**  
  Implement shortcuts for key actions (e.g. “S” to Start/Pause, “R” to Reset, “M” to Mute/Unmute, arrow keys to adjust time).
- [ ] **Print-Friendly Seat Plan**  
  Add a “Print View” style that strips off controls and backgrounds, ensuring the seat-plan table prints neatly on paper. 
- [ ] **Download Seat Plan**  
  One click download the seatplan as a PNG
