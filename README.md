# Marlin Firmware configured for Sapphire Pro/Plus printers
Sapphire Pro with:
- MKS Robin nano V1 boards
- TMC 2209 stepper drivers with UART(additional wiring needed)
- TFT35 touch Screen
- SD Card

### Marlin bugix 2.1.x Version has a bug if you want to print fast and have ABL activated:
- The stepper starting stuttering when crossing the Meshlines. Also printed blobs are visible at this spots.
- High Jerk is not the solution in this case
- The display menus were lagging at fast movements
#### Version 2.1.2.1 is working fine.

## Status Screen with black background(is set to blue on version 2.1.2.1)

![alt text](https://github.com/Discharge87/Marlin_for_Sapphire/blob/main/Sapphire_status_display.jpg)


### Releases available here:
- [Marlin 2.1.2.1 for Sapphire Pro(latest)](https://github.com/Discharge87/Marlin_for_Sapphire/releases/tag/Version_Sapphire_2.1.2.1)
- [Marlin bugfix 2.1.x for Sapphire Pro](https://github.com/Discharge87/Marlin_for_Sapphire/releases/tag/Version_Sapphire_bugfix_2.1.x)
