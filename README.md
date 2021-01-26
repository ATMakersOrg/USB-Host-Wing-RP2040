# USB-Host-Wing-RP2040
 Prototype of a USB Host Feather Wing using the RP2040
 
 Based on the excellent Feather board by Limor Fried and quite unlikely to work at the moment.  This is just a starting point to see where this could go.  
 
# Goals
 * Board should run TinyUSB (probably through Arduino when that works) to host USB peripherals.
 * Logic on this board would read the USB and then send messages to the main feather via UART (by default) or I2C or SPI with appropriate solder jumpers set
 * Voltage on the USB Host port should be 5V even when the Feather is being powered by a battery, so an onboard boost converter is needed.
 
# Current Challenges
  * Layout is ineffecient (and there are probably conflicts, etc.
  * Room in the center could be used to expose additional GPIO or Analog pins (which would be handy)
  * It would be nice to have second rows of headers to allow connections from GPIO on this wing to the main feather.
  * Power on the USB-C connector is probably wrong... I need to think through how to handle programming vs hosting w/it.
  * The Boost converter I found (PCA9411) has a BGA package which would be hard to solder (and I know nothing about it) - looking to replace with MCP1642B-50 which is easier to solder & seems like a better fit.
  * The MISO and MOSI lines should not be swapped ( need to redo them)
 
 I welcome all input (including thoughts about killing this idea)!
 Bill
 
![Board File](https://github.com/ATMakersOrg/USB-Host-Wing-RP2040/blob/main/media/BoardTraces.png?raw=true)
![Top](https://github.com/ATMakersOrg/USB-Host-Wing-RP2040/blob/main/media/FrontPCB.png?raw=true)
![Bottom](https://github.com/ATMakersOrg/USB-Host-Wing-RP2040/blob/main/media/BackPCB.png?raw=true)
![Schematic](https://github.com/ATMakersOrg/USB-Host-Wing-RP2040/blob/main/media/Schematic.png?raw=true)
