# LED_Hoop
Hula hoop with ESP8266, MPU9250, and SK9812 SPI LED strips

This project uses a transparent polypro hoop which is 264cm in radius with an inside diameter of 14.5mm. This gives limited space for components and as such, an ESP-03 is used.

Jason Coon's code works well on ESP based dev boards such as the NodeMCU but the ESP-03 has only 4Mbit flash as opposed to the more common 8Mbit flash on NodeMCU 1.0 etc. 

I also want to incorporate data coming from a MPU-9250 (Sparkfun breakout board version) and hopefully some proof of concept code will be easy to implement.

The other major component is the SK9812 strip, which is SPI controlled and can update at up to several MHz, is often used for light painting which is potentially interesting. This hoop accomodates approx. 264cm of 144 pixels/meter strip (approx 380 RGB individually addressable LED's).

Power is provided by approximately eight 200mAh Li-Ion batteries, in parralel, charged by an suitable external charger. The strips accept the 3.2v - 4.2v output by the Li-Ion batteries directly, however the ESP-03 and the MPU-9250 require small DCDC step down board to regulate the battery output to the lowest voltage that the ESP-03 and MPU-9250 will accept (about 2v).
