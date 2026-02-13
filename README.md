# Sharp MZ-80B
My little repository of information about Sharp's MZ-80B all-in-one business computer from 1981.<br>

The MZ-80B is an evolution of the MZ-80K.<br>

WORK IN PROGRESS.<br>

## Videos
- [Part 1: Initial look & disassembly](https://youtu.be/cHQdRs1u79s)
- [Part 2: Keyboard refurbishment starts](https://youtu.be/vS2Di7rVlAI)

## Specs
- Z80 at 4MHz (LH0080A)
- Power: ±5V, +12V
- 32KB RAM, expandable to 64KB
- 2KB ROM (Initial Program Loader, IPL)
- 2KB Character Generator ROM
- 2KB Character RAM
- 8KB Graphics RAM, expandable to 16KB (MZ-80GMK)

## Main ICs
- IC2: Sharp X0240PA (Gate Array 14297)
- IC3: Sharp LH0080A (Z80 CPU)
- IC8: Sharp IX0285PA (IPL Boot ROM, 334-5700)
- IC19: 8253 PIT (Progammable Interval Timer)
- IC24: Sharp LH0081A (Z80 PIO)
- IC25: NEC D8255AC-5 PPI (Programmable Peripheral Interface)
- IC41: Toshiba TMM2016P-1 (2KB S-RAM)
- IC42: Sharp X0241PA (Gate Array 14298)
- IC43: Sharp X0242PA (Gate Array 14299)
- IC44: Sharp IX0286PA (CG-ROM, 334P-5701)
- DRAM: Sharp LH4116-3 (16k x 1-bit)

## [Manuals](/Manuals)
- MZ-80B Service Manual
- MZ-80B Owners Manual

## [ROMs](/ROMs)
- 2KB Initial Program Loader (IPL)
- 2KB Character Generator
- BASIC for EPROM expansion board

## [32KB RAM Expansion](/Sharp_MZ-80B_RAM_III_IV_Expansion)
Internal expansion board to increase the RAM from 16KB to 48KB.  This design is from the Service Manual and so currently uses 4116 RAM chips.<br>

## [8KB Graphics RAM Expansion](/Sharp_MZ-80GMK)
Expansion board that connects to the internal Expansion Port (MZ-80EU) that doubles the graphics video RAM from 8KB to 16KB.  This design is from the Service Manual but uses a 32KB 62256 as these are still available new, rather than an obsolete 8KB 6264 or four 2KB 2016.<br>

WORK IN PROGRESS.<br>

## [DRAM to SRAM](/Sharp_MZ-80B_DRAM-to-SRAM)
Idea to replace the 16 x 4116 DRAMs of the original 32KB RAM plus the additional 16 x 4116 DRAMs of the expansion RAM with two 62256 SRAMs.<br>

WORK IN PROGRESS.<br>

## [Keyboard](/Keyboard)
Schematic and replacement PCB design.<br>

WORK IN PROGRESS.<br>

![Sharp MZ-80B keyboard layout](/Keyboard/sharp-mz-80b-keyboard.jpg)

## [SD Card Interface](https://github.com/yanataka60/MZ-2000_SD)
Design (not mine!) to add SD card interface for the MZ-80B (and others).  It will work in an 80B with or without the Expansion Unit installed, which is neat.
