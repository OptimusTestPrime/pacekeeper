# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.0.1] - 2026-04-02

### Added
- **Screen Wake Lock API:** The app now explicitly requests that the device keep the screen turned on while a match is in progress, preventing auto-dimming during play.
- **Visibility Re-acquisition:** Added logic to automatically re-sync the timer and re-lock the screen if a user switches apps and returns.

### Fixed
- **Background Throttling:** Resolved a critical issue where the countdown would pause or "drift" when the device screen turned off or the browser was minimized.

### Changed
- **Timestamp-Based Logic:** Rebuilt the internal countdown engine to use absolute system time (`Date.now()`) rather than simple interval subtraction. The clock is now bulletproof and remains accurate even if the device sleeps for several minutes.
- **Tick Frequency:** Increased UI update frequency to 500ms for a more responsive visual experience on wake-up.

## [1.0.0] - 2026-03-31

### Added
- **Initial Release:** Launched PaceKeeper (formerly conceptualized as StoneTimer), a free curling game monitor.
- **Dual Display Modes:** Toggle seamlessly between a large digital countdown and a dynamic analog pie-chart dial that scales to your custom time.
- **Match Configuration:** Set custom hours and minutes with responsive, rapid-advance touch controls.
- **End-of-Game Policies:** Built-in display alerts to remind players of club rules when time expires (e.g., "Finish current end, then stop" vs. "Finish current + one additional end").
- **Accessible Alerts:** Choose between an audio buzzer, an accessible "Scrolling Curling Rock" visual animation, or both.
- **Match Controls:** Dedicated Start/Pause button, a quick-reset button to reset the current timer without losing settings, and a Home button to return to the setup screen.
- **Alarm Dismissal:** The active "Done" button mutes the buzzer and hides the visual animation immediately.
- **Help Modal:** In-app instructions and cross-promotional links to the HammerTime and StoneStat apps.
