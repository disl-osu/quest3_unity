
This file shows how to build a Unity app and run it on Meta Quest 3.

## Quick links

- Unity Hub installation: https://docs.unity3d.com/hub/manual/InstallHub.html
- Example Unity tutorial (create a simple cube-manipulation app for Quest):
      - https://www.youtube.com/watch?v=oqQPa--U2Ik&list=PLWa7QG82eDnSmuAsUVYznlvSQgfStyPUF

## Build the APK

- In Unity, set the Player / Product Name (e.g. "testapp").
- Build the project to an Android APK (e.g. myapp.apk).

## Ways to run the simulation on Quest

- Option A — Air Link / streaming (no APK installed; good for fast debugging):
      - Play the scene in Unity on your PC.
      - Windows: run Meta Quest Link on the PC and enable "Link" on the headset.
      - Linux (example): use SteamVR + ALVR on the PC and run the ALVR app on the headset.

- Option B — Install the APK on the Quest (persistent install):
      - Load APK to headset:
            - Open a terminal and run: <pre><code class="language-powershell">adb install myapp.apk</code></pre>
            - Launch on headset:
                  - On the Quest, open Library -> Unknown Sources and start the app named "testapp" (or the product name you set in Unity).

## Tools & setup notes

- Meta Quest Link (official):
      - https://www.meta.com/help/quest/509273027107091/
      - Notes:
            - Use a USB-C 3.0 cable for wired Link.
            - For Air Link (Wi‑Fi), ensure the PC and Quest are on the same local network.

- ADB (Android Debug Bridge) installation reference:
      - https://docs.42gears.com/AstroFarm/InstallADBSetuponWindowsDevices.html#:~:text=1.,required%20when%20configuring%20the%20agent
      - Notes:
            - Use a high-quality USB-C cable when connecting the headset to the PC.
            - Verify connection with: <pre><code class="language-powershell">adb devices</code></pre> 
            - When you connect the Quest 3 to the PC for the first time and run an adb command, the headset will prompt you to allow USB debugging from the computer. Choose "Always allow from this computer" (or similar) on the headset to avoid repeated prompts.

## Troubleshooting hints

- If the headset does not show under adb devices:
      - Reconnect the USB cable and re-enable USB debugging on the headset.
      - Try a different USB port or a known-good cable.
- If streaming (Air Link) stutters:
      - Move PC and headset closer to the Wi‑Fi AP or use a wired connection for the PC.

## References

- Meta Quest Link docs: https://www.meta.com/help/quest/509273027107091/
- ADB install guide: https://docs.42gears.com/AstroFarm/InstallADBSetuponWindowsDevices.html#:~:text=1.,required%20when%20configuring%20the%20agent


