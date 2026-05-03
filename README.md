# KARM - Time Tracking

A minimalist, dark-themed, daily time-tracking application built with React, Tailwind CSS, and Chart.js. KARM helps you categorize your day hour-by-hour, track productivity trends, and achieve your focus and sleep goals directly from your browser.

## Features

* **24-Hour Timeline:** Visualize and log your activities for every hour of the day.
* **Activity Categorization:** Tag your hours with color-coded categories: Productive, Semi-Productive, Neutral, Gym, Errands, Unproductive, Wasted, and Sleep.
* **Productivity Scoring:** Automatically calculates your daily productivity score based on how you spent your logged hours.
* **Focus Timer:** A built-in timer to keep you on track. It features an optional audio alarm (using the Web Audio API) to remind you to log your activity at the end of the hour.
* **Analytics Dashboard:** * View a 30-day productivity trend chart.
    * Analyze your weekly and daily category breakdowns using a dynamic Donut Chart.
    * Track your all-time best productivity score and compare your performance against the previous week.
* **Daily Goals:** Set and monitor daily hour targets for *Productive Time* and *Sleep*.
* **Quick Actions:** Easily copy yesterday's schedule, mass-log sleep hours, or quickly log the previous hour with a single click.
* **Privacy-First & Offline:** 100% client-side logic. All data is saved securely in your browser's Local Storage without needing an external database.

## Technologies Used

* **HTML5 / CSS3 / JavaScript**
* **React 18** (Loaded via CDN) for stateful, component-based UI.
* **Tailwind CSS** (Loaded via CDN) for rapid, responsive, and consistent dark-mode styling.
* **Chart.js** for rendering responsive line and donut analytics charts.
* **Babel Standalone** to compile JSX directly in the browser runtime.
* **Custom SVG Icons** (Lucide-inspired) implemented inline for a lightweight, dependency-free footprint.

## Getting Started

Because KARM is built as a self-contained, single-file web application, there are no complex build steps, package managers, or dependencies to install.

1. Clone or download the source code containing `index.html`.
2. Double-click `index.html` to open it in any modern web browser (Chrome, Edge, Firefox, Safari).
3. Start logging your time! 

## How Data is Saved

KARM uses the browser's native `localStorage` API to keep your data persistent across sessions. 

* `karm_data`: Stores all your hourly log entries.
* `karm_goals`: Stores your daily targets (e.g., 8 hours productive, 7 hours sleep).
* `karm_timer`: Remembers if your focus timer was left on.
* `karm_sound`: Remembers your audio alert preferences.

*Important Note: Since data is stored locally, clearing your browser's site data/local storage will delete your time-tracking history.*

## UI / UX Highlights
* **Mini Calendar:** Navigate through your historical data using a heat-map styled mini calendar showing daily productivity intensity.
* **Smooth Animations:** Utilizes subtle hover effects, modal fade-ins, and animated number counters for a polished feel.
* **Auto-Scroll:** Automatically scrolls the active timeline to the current hour upon page load or returning to "Today".
