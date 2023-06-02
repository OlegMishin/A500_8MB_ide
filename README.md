# A500_8MB_ide
 
 8MB autoconfig FastRAM and IDE interface expansion board mounted into Amiga's CPU socket. 
Inspired by ram68k and ide68k projects: http://www.mklboards.fi/ram68k/ In fact the two boards combined into only one.

Source code based on 68k and A600 "Amiga 600 8 megabytes fastRAM board": http://lvd.nedopc.com/Projects/a600_8mb/index.html
Autoconfig function and Gary IDE registers based on Terriblefire sources (Many thanks to Stephen J. Leary).

Works with A500. Doesn't work with CDTV due to DMAC on board (when I have a chance to test, I will update FW for CDTV).

# CLPD: 
In the design I used Microchip ATF1508 true 5V CPLD in 100 pin TQFP package. The source code is in verilog. Design tool - Quartus 13.0sp1.
The below CPLD can be used in the project:

ATF1508AS/ASV (TQFP-100) or EPM7128STC100/STI100 with speed grade up to 15ns(tested).
Also 25ns should work(not yet tested). 

# RAM: 
The same as in ram68k project: KM416C4104AS-6 or KM416C4104C. Can be salvaged from 72pin SIMM modules.

# PCB: 
Two layers board. CAM file included for production.

# Notes:
- To be able to boot from the IDE without rebooting a patched scsi driver should be integrated into Kickstart. This can be done using Remus software.
- Requires OVR# ant INT2 connections to the expansion slot.
- No CFGIN/CFGOUT implemented as I don't need them.

![3D_render](https://user-images.githubusercontent.com/81614352/137478370-01d7e0f7-530c-4405-b8d8-a8bc4e3bfd53.png)

# Actual PCB
![изображение](https://user-images.githubusercontent.com/81614352/159073952-6bbf11e8-2acb-4636-b400-00bc0ea5ab38.png)


# Installation example
![изображение](https://user-images.githubusercontent.com/81614352/157677474-ae68848f-e7ed-40b6-94e6-58987b2c6a8a.png)

