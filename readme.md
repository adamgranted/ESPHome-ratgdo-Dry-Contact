# An ESPHome variant for the ratgdo 2.52i

At the time of posting this, the official ESPHome firmware does not support dry contact functionality. Once it does, this config will be deprecated.

This configuration is for a dry contact garage door control using an open reed switch, closed reed switch, and the obstruction sensors. It uses the exact wiring as recommend by the ratgdo project with the exception of the reed switch pinout. The obstruction sensors proved to be tricky, I had to delay the detect timing to smooth out the readings. 

My reed switches are wired in a NC state, essentially the pull up resistors mark the "ON" state in the esp. When the magnet reaches the reed switch, it disconnects the closure from GND letting the pull up resistor mark the pin as high resulting in "closed" or "open" respectively.

Hopefully this helps someone else! 