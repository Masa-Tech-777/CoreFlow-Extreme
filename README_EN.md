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

Set the maximum frequency in 10 MHz steps, or enter 0 MHz to remove the cap. Minimum frequency entries start at 400 MHz and use 10 MHz steps. Choose from seven Windows boost modes (0–6). When the app verifies the CPU maximum in its specification database, that value becomes the input ceiling.

Confirmed settings are saved per original power plan. Selecting a regular plan in Windows pauses Extreme’s control. Apply settings from the app to resume control.

The maximum frequency is a limit requested through Windows. The app converts the minimum frequency you enter to a Windows minimum processor performance percentage. Actual clock speeds and the effects of your settings depend on your CPU, workload, and the PC manufacturer’s controls. Monitor displays clock speed estimates from Windows over a sampling interval. See `User_Guide_EN.txt` in the distribution ZIP for details.

## Using a frequency cap with boost enabled

Suppose your CPU has a rated maximum of 4.9 GHz. On a compatible PC, you can request a 3800 MHz cap and leave boost enabled. Windows and the CPU still respond to the workload. For everyday tasks such as watching videos or editing documents, start with a lower cap and raise it gradually if you notice longer waits. This helps you compare responsiveness and fan noise. You can save separate settings for AC and battery power.

A 3800 MHz cap does not lock the CPU to that speed or guarantee that every instantaneous reading stays below it. Likewise, entering 400 MHz as the minimum does not guarantee that the CPU will reach 400 MHz or stay above it.

## Choosing a boost mode

| Value | Mode | Behavior |
|---|---|---|
| 0 | Disabled | Disables boost. |
| 1 | Enabled | Uses standard Windows boost behavior. |
| 2 | Aggressive | Requests higher performance more readily. |
| 3 | Efficient Enabled | Uses boost with efficiency in mind. |
| 4 | Efficient Aggressive | Requests higher performance more readily while considering efficiency. |
| 5 | Aggressive at Guaranteed | Uses the guaranteed performance level as the reference for aggressive requests. |
| 6 | Efficient Aggressive at Guaranteed | Uses the guaranteed performance level as the reference while considering efficiency. |

The actual response depends on the CPU and firmware. Start by adjusting the cap with your current boost mode so you can see the effect of the cap on its own.

## How input corrections work

When the CPU model matches the built-in database, Extreme displays the rated base and maximum frequencies. An entry above the verified maximum is corrected to that maximum. Blank entries, minimum values below 400 MHz, and maximum values from 1 to 800 MHz are corrected to 1400 MHz. The app also redirects 2500 MHz to 2400 MHz based on earlier testing. If a correction message appears, review the values and select Apply again. When the maximum is nonzero, the minimum must be lower than the maximum.

## Exiting, restoring, and keeping settings

Exit and restore returns Windows to a regular plan and removes Extreme’s dedicated plans. Confirmed settings and license registration are saved. After a normal exit, launching the app again reapplies confirmed settings. After an abnormal exit, recovery takes priority. Full Reset also clears the license registration and saved settings.

## Monitor and diagnostic logs

Select Show Monitor to view CPU activity. If you install HWiNFO separately, register its executable under Help in the main app and open it from Monitor. If you report an issue, include the diagnostic logs from the main app and Monitor, the time it happened, the selected power plan, and whether the PC was plugged in or running on battery.

## Package contents and license registration

The ZIP includes the main app, the `LiveMonitor` folder, Japanese and English user guides, file checksums, and third-party notices and license information. After purchase, open the license registration screen to find your Machine ID and follow the instructions for providing it with your order information. Version 2.7.3 and later uses signed keys beginning with `CFX2-`. Contact support to request a replacement if you have an older key.

## Trial Version and Support

You can use the software in an unregistered state for a cumulative total of 60 minutes. Please purchase a license via BOOTH (https://masatech.booth.pm/).
For support or to request a license reissue for the Astra series, please contact masatech.dev.apps@gmail.com.

Developed by MasaTech / Itachi, Spica, and Mahiru
Blog: [https://masatech.hatenablog.jp/]
[BOOTH – MasaTech](https://masatech.booth.pm/)
