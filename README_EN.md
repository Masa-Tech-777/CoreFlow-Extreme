# CoreFlow Extreme

[日本語版 README](README.md)

CoreFlow Extreme lets you adjust CPU performance on Windows 11 (x64) for the way you use your PC. For example, you can prioritize performance while plugged in and set a lower maximum frequency on battery power.

## Features

- Set the maximum CPU frequency (MHz), minimum performance target, and boost mode independently for AC and battery power.
- Apply changes to a copy of the selected Windows power plan, preserving the original plan’s CPU settings.
- Confirm the changes within 15 seconds to keep them. If the timer expires, the app restores the previous state.
- Use the included Monitor to check the observed clock speed, CPU usage, and current control status. Temperature readings require a compatible module.

## Getting started

1. Extract the entire distribution ZIP. If an older version is running, use **Exit and Restore** to close it first.
2. Run `CoreFlow_Extreme.exe` and approve the Windows administrator prompt. Keep the `LiveMonitor` folder next to the executable.
3. Choose a power plan, review the AC and battery settings, and click **Apply Settings**. Start with small changes to the maximum frequency so you can see their effect.
4. Choose the option to keep the settings if they work for you. To exit the app and return to a regular power plan, right-click its notification area icon and choose **Exit and Restore**. Closing the window with **×** keeps the app and its controls running in the notification area.

## Understanding clock readings

The maximum frequency is a limit requested through Windows. The app converts the minimum frequency you enter to a Windows minimum processor performance percentage. Actual clock speeds and the effects of your settings depend on your CPU, workload, and the PC manufacturer’s controls. Monitor displays clock speed estimates from Windows over a sampling interval. See `User_Guide_EN.txt` in the distribution ZIP for details.

## Trial and support

You can try the app for 60 minutes of total use before registering. For support or a replacement license key, contact masatech.dev.apps@gmail.com.

Developed by MasaTech / Itachi, Spica, and Mahiru  
[MasaTech on BOOTH](https://masatech.booth.pm/)
