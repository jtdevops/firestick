# Firestick TV 2nd gen (tank)
## Steps to unbrick/root un-updatable devices

### My experience:
After I had rooted my device a year ago, I had also blocked future updates from happening.
I then went and did a Factory Reset on the device, which did its job, but wasn't able to connect to the Amazon servers to check for updates. The device refused to complete the initial setup process because of this.
This caused my Firestick to be unusable, and essentially bricked as I couldn't get past the update check.

To unbrick/unlock the device I followed these steps: https://forum.xda-developers.com/t/unlock-root-twrp-unbrick-fire-tv-stick-2nd-gen-tank.3907002/

I downloaded the latest prerooted rom and saved it on my USB: https://forum.xda-developers.com/t/fire-tv-stick-2-tank-prerooted-stock-images-5-2-7-3_r1.3912271/
Here is the newest official rom: https://forum.xda-developers.com/t/fire-tv-tank-5-2-8-2-ota-zip.4308269/

To fix this issue, I needed to connect a keyboard/mouse to the Firestick in order to navigate the TWRP interface and flash a new rom images.

I needed to use the following to get access to the TWRP screen after the device was unlocked:
- Firestick OTG cable (similar to: https://www.amazon.ca/Pack-Cable-Fire-Stick-Host/dp/B083KJ1B5H)
- Hub that allows external power - since the USB and mouse need additional power
- USB drive containing the rom image to flash in TWRP
- USB male to male cable
- External power for the Hub and a USB power cable and adapter to connect to the OTG cable

### Cable/hub setup:
- Connect external (USB) power to the hub, then connect the USB and mouse
- Connect external (USB) power to the OTG cable
- Connect the USB male to male cable to the OTG USB A port, and the other end into the laptop's USB port so you can run the scrips linked below

Test to make sure that the device will have enough power by connecting the OTG cable to the Firestick and letting it power up, then remove the USB male from the OTG USB A port and then connect the USB Hub. If there are no power issues then the Firestick will still be powered and working.

Follow the 'Cable/hub setup' step above to get the cables connected and then follow the steps outlined in: https://forum.xda-developers.com/t/unlock-root-twrp-unbrick-fire-tv-stick-2nd-gen-tank.3907002/

Once the device is in TWRP, then you can remove the USB male cable from the OTG USB A port, and then connect the USB Hub.
Now you should be able to use the mouse and USB drive in TWRP to flash your system with a new rom, or other options that TWRP provides.

In TWRP, I went to 'Install' and then selected the rooted rom zip file and went through the process of flashing the Firestick with it.
Once complete, I selected the option to 'Wipe Cache/Dalvik'. I think this part allowed me to complete the Firestick setup process afterwards as it removed the update blocker I had installed.

---

# Install rooted rom
In the Developer Options, enable USB Debug mode
The connect from any computer using ADB or the Android 'Remote ADB Shell' application, and connect to the device via:
```
adb connect <ip>:5555
```
and then confirm that you are connected via:
```
adb devices
```
Make sure that there is only 1 device connected, otherwise disconnect them using:
```
adb disconnect <ip>:5555
```
Then to enter the Recoverty Mode and access TWRP, issue command:
```
adb reboot recovery
```
The Firestick will then restart and take you to the TWRP interface.
Now connect your URB Hub with the mouse and USB drive, to the OTG cable.
Select 'Install' and then try to find the ZIP file containing the rom. I needed to Select Storage and select OTG. Then I was able to find my new rom file.
Once complete, I selected the option to 'Wipe Cache/Dalvik', and then rebooted.
