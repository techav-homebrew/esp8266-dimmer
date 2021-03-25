# esp8266-dimmer
ESP8266 3-Channel LED dimmer

This is a simple WiFi-enabled 3-channel LED dimmer with 4 user buttons. It is designed to be powered from the same 12 Volt power supply that would be used to power a common RGB LED strip. Higher current draw (e.g. longer LED strips) may require active cooling on the output switching transistors. 

This project has been abandoned and is being published here to release into public domain (CC0). Project is intended as an intellectual excercise only, and its author will accept no liability for any adverse effects of its use. 

## Construction
Output screw terminals and programming header are intended to be mounted on the bottom of the board. All other parts should be mounted on top. 

Board is designed to use virtually any capable TO-252-3 transistor. Pads are included for a 100-Ohm base resistor if a bipolar transistor is used. For a MOSFET, this resistor is not necessary, and a jumper or 0-ohm resistor may be installed instead.

## Programming
No firmware currently exists. Device can be programmed with any ESP8266 toolchain, including the Arduino environment. Programs are loaded via 3.3V UART connected to the programming header. To place the device in programming mode, connect the UART, hold the Down button (button 3, GPIO0), and assert ~Reset by connecting to Signal Ground. 

### Programming Header
1. TxD
2. RxD
3. Signal Ground
4. Signal Ground
5. ~Reset