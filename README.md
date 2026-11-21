# Soldat Meltfire
 Soldat Meltfire Dashboard

![image](https://github.com/user-attachments/assets/068b62dc-acc1-4e7b-9c84-15c6f08d08de)

---
A design based upon the Soldat Meltfire from RR6/Ferrari 360 or the old style Esprit dashboards. I've left part of the design open for your own gauge (be it AF/Intake temperature/*choose your own adventure*). Let me know if you want something here.

## Layout

- `SoldatMeltfire.qml` - entry file: live data, config load/save, joystick handling, settings menu
- `SoldatMeltfireDisplay.qml` - the dial itself
- `SettingsMenu.qml`, `SettingBox.qml`, `MonoText.qml`, `Theme.qml`, `GridBackground.qml` - settings menu (shared with AgeSolo)
- `SettingsPreview.qml` - standalone menu preview, not loaded by the dash
- `SoldatMeltfire.qml.png` - preview shown in the dash picker

Oil temperature and oil pressure can each be hidden with their Show row in the settings menu.

Settings are saved as JSON in `/opt/IC7/screen_configs/SoldatMeltfire_config.json`. An existing `Meltfire_config.txt` is imported once on first run.

When setting limits, think in units of celcius. I typically make 100C for coolant, and 130 C for oil temp limits. 1 bar = ~14 psi. You'll see the limit marker rotate as you raise the temperature! :) 

---

# Installation notes:

1) Obtain the GARW dash installer here: https://github.com/dustinsterk/GARWDashUploader
2) You will need to unzip this dashboard file, rename the folder to "SoldatMeltfire" (Don't use the quotes), and recompress it. (I know, it's a pain)
3) Upload the dash via the uploader while connected to the GARW Wifi.
4) Follow the rest of the aforementioned instructions.

This dash will require you to update your gear settings (under settings -> gears) for the calculated gear (unless you're very fancy and running a sequential with a canbus output), the following works decently for me currently with a stock C64 transmission:

(1st) 123 (2nd) 83 (3rd) 60 (4th) 47 (5th) 37 (6th) 33
