# Dell XPS 9700 macOS BigSur - Working Sleep!

Working sleep and other niceties!

Thanks to @thewhoyouare and @OCD0711 and many others, and a whole heap of luck, I've stumbled across a combination of SSDTs that work for my XPS 9700 4K.

I've added some SSDTs to the repo including SSDT-PS2K.aml which toggles the touchpad when you press PrtSc (F10), but retains touchscreen function. This is very useful if you find you get phantom mouse movements with the touchpad while typing.

@thewhoyouare Repo solved my ridiculous power management settings which was chewing through my battery. I've used CPUfriend with a very low TDP-down of 800Mhz now, you can adjust it to your preference.

Now, to sleep! I was getting the Dell logo on wake up and had to reboot with hard power down. Then I found that by turning off the Logo/Early Signs of Life option in the BIOS, I was able to get proper sleep. Only 1-2% battery drain over night, checked with this Terminal command: 

pmset -g log|grep -e " Sleep  " -e " Wake  "

Issues still unresolved:
- Audio through internal speakers not working
- Microphone (internal) not working
- USB working intermittently, especially through the Thunderbolt Dock (Dell TB15).
- Ethernet working through USB-C dongle but not through Thunderbolt Dock
- HDMI out not working (purple haze, or no signal at all) when going through TB->HDMI but works fine USBC-HDMI. The framebuffer connector type has been adjusted but I think it's to do with TB vs USB-C (alt mode) conversions.

Finally, I'm using rEFInd as my initial boot loader to dual boot Windows / Mac so that's what you'll find in the Boot.zip.

Note that I've taken out some kexts while troubleshooting (eg SD card kexts) so you'll have to put them back in if you need them.


---


## Functional status

|Function/hardware|Status|
|-|-|
|Built-in display UHD630 |Yes, full graphics acceleration|
|Output display using Thunderbolt |Yes, 2 4K@60Hz (via DP) + built-in (1920x1200) tested|
|Output audio to monitor via Thunderbolt (DP) |Yes|
|CPU power management|Normal, could use improvement|
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
|SD card slot|Yes|
|Sleep|YES|

|Headphone plug|No|
|Speakers|No|
|Microphone|No|
|Fingerprint recognition module|No|

---


---

![](https://github.com/thewhoareyou/MacOS-XPS-9700-OpenCore/blob/4fd0700f544e05e248bc58044402969be4f4b3e4/BigSur%20Hackintosh.png)
