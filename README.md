# PCB-RP2040



We've realized an electronic board based on the RP2040.
This microcontroller has 2 MB of flash memory, providing ample storage space for programs and data. It has 26 digital I/O pins, 3 of which can be used as analog inputs.
The RP20240 is used for the Raspberry Pico board and is programmable in micro-Python or directly with Arduino Ide.
We developed the board on Kicad and had it manufactured on jpclb. It costs around 17 euros per board, and is a 2-layer board measuring 2.7cm x 2 cm. You can find the files on our github.


<h1> Electronic diagram</h1>
We'll now take a closer look at how our electronic board works: 

![Alt text](picture/arduino1?raw=true "PCB in 3D view")

For powering the circuit, we've used a Micro USB type B connector to supply our board with 5V. As the RP2040 uses 3.3V, we've fitted a regulator to convert 5V to +3.3V: 

![Alt text](picture/arduino2?raw=true "PCB in 3D view")

This is where you'll find the 128-megabit flash memory to store the program. The 2-pin connector allows you to force USB boot:

![Alt text](picture/arduino3?raw=true "PCB in 3D view")

The 12Mhz crystal provides the clock for our RP2040 microcontroller:

![Alt text](picture/arduino4?raw=true "PCB in 3D view")


We have added a LED to be programmed on GPIO18 to check that our card is working properly: 
![Alt text](picture/arduino5?raw=true "PCB in 3D view")

Finally, we have the RP2040 microncontroller. It is supplied with 3.3V with decoupling capacitors:
![Alt text](picture/arduino6?raw=true "PCB in 3D view")


<h1>PCB Design</h1>


The board is a 2-layer design. On the top you can see the 3.3V regulator and the Micro-USB type B connector.
In the middle of the board you'll find the flash memory and the RP2040 microcontroller.
At the bottom of the board you'll find the 2-pin USB boot connector and the 12Mhz quartz crystal.
A ground plane has been created on the TOP layer to connect all the GNDs together.

Here are the 3d and top layer views of the PCB:

![Alt text](picture/arduino7?raw=true "PCB in 3D view")

Here is a 3d view of the PCB:

![Alt text](picture/arduino8?raw=true "PCB in 3D view")



