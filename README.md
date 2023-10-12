# 2764 to 27hc641 Read/Write adapter

Adapter to program 27hc64 for using in old computer (as 2364), with a programmer supporting only 2764

In my EMP-20 the 27hc641 programming alghoritm is buggy ( not write 0xFF but this eprom is a three state eprom and need to program 0xFF)

My workarround is to make this adapter for programming 27hc641 as a normal 2764, tested and working in T48 programmer.

In 27hc64 pin 20 (G) is used for Output enable (0v), Program enable (12.5v) and idle (5v)

In 2764, there are 2 dedicated pins, pin 22 for output enable and 27 for program enable.

My project, use a CD4051 analog mux/demux to merge 2764 pin from programmer and adapt it for 27hc641 single control pin.

I have used two 2n7000 to make a level shifter for adapt ttl signal from programmer to cmos signal of CD4051

Power supply is from 18 to 19V

HOWTO

WARNING! WARNING! WARNING! 

Change default programming voltage to 12.5 or you damage device!!! See photo of settings!

In your eprom programmer, select 2732 generic eprom, make setting as "T48 Settings.png"

Power on device, from 18 to 19V (2x9v battery is good)

In xgecu, load bin and click on write image , program your 27hc641, enjoy!

 
