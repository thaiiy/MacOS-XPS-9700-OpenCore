# Dell XPS 9700 macOS BigSur

This is an EFI made with OpenCore. You can install macOS BigSur on Dell XPS 17 9700 (2020).
I think this EFI should be easy enough to just drag and drop.  You need to set your own serial number/MLB.
Battery life is not great (2-3 hours).  If anyone is able to improve it, please let me know!

<b>OpenCore Version:</b> 0.6.4

<b>macOS Version:</b> BigSur 11.6.1


---


## Functional status

|Function/hardware|Status|
|-|-|
|Built-in display UHD630 |Yes, full graphics acceleration|
|Output display using Thunderbolt |Yes, 2 4K@60Hz (via DP) + built-in (1920x1200) tested|
|Output audio to monitor via Thunderbolt (DP) |Yes|
|CPU power management|Normal work-idle 800MHz, up to turbo frequency)|
|Built-in keyboard|Yes|
|Built-in touchpad/touchpad gestures|Yes|
|Thunderbolt 3|Yes|
|USB 3.x|Yes|
|USB 2.0|Yes|
|Wifi (AX1650S)|Yes|
|Bluetooth|Yes|
|Screen brightness|Yes, can adjust the brightness (shortcut keys are not mapped)|
|Built-in camera|Yes|
|Facetime|Yes|
|iMessage|Yes|
|Sleep|Yes (not fully tested)|
|Hibernation|No (lid close functionality must be disabled in BIOS)|
|Headphone plug|No|
|Speakers|No|
|Microphone|No|
|Fingerprint recognition module|No|
|SD card slot|Not tested|

---


## Note

ALC256.aml SSDT file is included to get Facetime working.  I think if you use any audio codec it will work, especially if you can get the speakers working.

Some models of Dell XPS 17 9700 are equipped with Hynix PC611. They cannot be used on MacOS and will not be able to enter the system/installation interface if they are not shielded. They can be shielded in the BIOS.

---

![](https://github.com/thewhoareyou/MacOS-XPS-9700-OpenCore/blob/4fd0700f544e05e248bc58044402969be4f4b3e4/BigSur%20Hackintosh.png)
