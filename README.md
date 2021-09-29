# Firestick TV 2nd gen (tank)
## Steps to unbrick/root un-updatable devices

My experience:
After I had rooted my device a year ago, I had also blocked future updates from happening.
I then went and did a Factory Reset on the device, which did its job, but wasn't able to connect to the Amazon servers to check for updates. The device refused to complete the initial setup process because of this.
This caused my Firestick to be unusable, and essentially bricked as I couldn't get past the update check.

To unbrick/unlock the device I followed these steps: https://forum.xda-developers.com/t/unlock-root-twrp-unbrick-fire-tv-stick-2nd-gen-tank.3907002/

To fix this issue, I was unable to connect a keyboard/mouse to the Firestick in order to flash a new rom images.

I needed to use the following to get access to the TWRP screen after the device we unlocked:
- Firestick OTG cable (similar to: https://www.amazon.ca/Pack-Cable-Fire-Stick-Host/dp/B083KJ1B5H)
- Hub that allows external power - since the USB and mouse need additional power
- USB drive containing the rom image to flash in TWRP
- USB male to male cable
- External power for the Hub and a USB power cable and adapter to connect to the OTG cable

Cable/hub setup:
- Connect external (USB) power to the hub, then connect the USB and mouse
- Connect external (USB) power to the OTG cable
- Connect the USB male to male cable to the OTG USB A port, and the other end into the laptop's USB port so you can run the scrips linked below

Test to make sure that the device will have enough power by connecting the OTG cable to the Firestick and letting it power up, then remove the USB male from the OTG USB A port and then connect the USB Hub. If there are no power issues then the Firestick will still be powered and working.

Follow the 'Cable/hub setup' step above to get the cables connected and then follow the steps outlined in: https://forum.xda-developers.com/t/unlock-root-twrp-unbrick-fire-tv-stick-2nd-gen-tank.3907002/

Once the device is in TWRP, then you can remove the USB male cable from the OTG USB A port, and then connect the USB Hub.
Now you should be able to use the mouse and USB drive in TWRP to flash your system with a new rom, or other options that TWRP provides.
