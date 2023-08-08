# Marlin_for_Sapphire_Pro(Marlin bugfix 2.1.x)
Since Platformio core 6 i run into compiling problems with different Marlin FW for Sapphire printers.
After long tryouts with other Marlin builds for Sapphire Printers with MKS Robin nano V1.2 Board with the TFT35 and UART i made a new build based on Marlin Bugfix 2.1.x.
Even when i finished a compilation things happen like the printers display is not running after an update.

If you meet the same configuration as below it is just plug and play.

Adapted for Sapphire Pro(Plus is also possible with some adjustments)

### Hardware:
- Board MKS Robin nano V1.2
- TFT35 Screen with touch
- Stepper TMC2209 for X,Y,Z and Extruder with additional UART wiring

### Software changes:
- **TMC2209** with UART **(HAS_TMC_UART)** is active
    * UART Pins are defined in pins folder(mks_robin_nano.h)
    * UART debug is active
- SD card **(SDSUPPORT)** is activated
- Homing point is in the middle of the bed
   * Endstops for X, Y and Z are hardware switches(original state)
   * Printer size is set to 225x225x220mm
- Retraction is dissabled. You can activate the function in configuration_avh.h and define(unmask) **"FWRETRACT"**
   * Display retraction settings are activated then
   * Or change values in the configuration_adv.h
- PID tuning **(PIDTEMP)** is active for bed and hotend
   * Display menu active
   * **PIDTEMPBED** Heated bed is active
- **Z_AFTER_HOMING** is set to 10mm
- Mesh bed leveling active
  * Display menu active
  * No probehead acive
- Core XY
  * Stepper directions are set for core xy
- **EEPROM_INIT_NOW** is active for reinitializing the EEPROM after new FW installation(recommended)
- **EEPROM_SETTINGS** is active for permanent value storage(recommended)
- In .../src/core/serial.h i had to define **SERIAL_CATCHALL** by force. Otherwise compiling ends up in errors.
  * Maybe because i could define in configuraation only one Serial port(if i put more than one in there- compiling errors)
    UART is working with one serial defined

## [Go to releases](https://github.com/Discharge87/Marlin_for_Sapphire/releases)


