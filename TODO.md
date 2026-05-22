# TODO

- [ ] Inspect current timer/solve lifecycle in src/App.jsx and confirm how solves are recorded (DNF vs STOPPED) 
- [ ] Implement Page Visibility API handling in src/App.jsx:
  - [ ] When document becomes hidden during RUNNING: invalidate current solve as DNF (penalty -1), stop timers/RAF, transition appState appropriately.
  - [ ] When hidden during INSPECTING/READYING_*: cancel inspection (stop inspection RAF, reset app state so solve can’t resume).
  - [ ] On return to tab: show status/toast text "Solve invalidated because the app lost focus." (simple UI).
- [ ] Ensure logic works for both keyboard and touch flows (no duplicate solve saving).
- [ ] Run local build/test command (npm test/build if available) and do a quick manual verification checklist.

