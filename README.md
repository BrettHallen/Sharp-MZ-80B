# Sharp MZ-80B
My little repository of information about Sharp's MZ-80B all-in-one business computer from 1981.<br>

The MZ-80B is an evolution of the MZ-80K.<br>

WORK IN PROGRESS.<br>

NOTE! Any PCB designs are untested unless stated otherwise.  I have done my best to recreate them based on the schematics in the Service Manual.  (15/Feb/2026)<br>

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

## [Components](/Components)
- IC2: Sharp X0240PA (Gate Array 14297)
- IC3: Sharp LH0080A (Z80 CPU)
- IC8: Sharp IX0285PA (IPL Boot ROM, 334-5700)
- IC19: 8253 PIT (Progammable Interval Timer)
- IC23: NEC D8255AC-5 PPI (Programmable Peripheral Interface)
- IC24: Sharp LH0081A (Z80 PIO)
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

## [32KB RAM Expansion](/Sharp_MZ-80B_RAM_III_IV_Expansion)
Internal expansion board to increase the RAM from 32KB to 64KB.  This design is from the Service Manual and so currently uses 4116 RAM chips.<br>

## [Base 8KB Graphics RAM (MZ-80GM)](/Sharp_MZ-80GM)
Reproduction of the base graphics RAM card (a.k.a. "GRAPHYICS-1") in the Sharp MZ-80B based on the service manual schematics.  I've updated it by replacing the original four 2KB 2016 SRAM chips with a single 32KB 62256.  Overkill, yes, but the 62256 is still available new - it reduces the chip count by four.<br>

![Reproduction MZ-80GM card](/Sharp_MZ-80GM/Sharp_MZ-80GM_3D.png)

## [8KB Graphics RAM Expansion (MZ-80GMK)](/Sharp_MZ-80GMK)
Expansion board (a.k.a. "GRAPHYICS-2") that connects to the internal Expansion Port (MZ-80EU) that doubles the graphics video RAM from 8KB to 16KB.  This design is from the Service Manual but uses a 32KB 62256 as these are still available new, rather than an obsolete 8KB 6264 or four 2KB 2016.<br>

## [DRAM to SRAM](/Sharp_MZ-80B_DRAM-to-SRAM)
Idea to replace the 16 x 4116 DRAMs of the original 32KB RAM plus the additional 16 x 4116 DRAMs of the expansion RAM with two 62256 SRAMs.<br>

## [Keyboard](/Keyboard)
Schematic and replacement PCB design.<br>

![Sharp MZ-80B keyboard layout](/Keyboard/sharp-mz-80b-keyboard.jpg)

## [SD Card Interface](https://github.com/yanataka60/MZ-2000_SD)
Design (not mine!) to add SD card interface for the MZ-80B (and others).  It will work in an 80B with or without the Expansion Unit installed, which is neat.

## [Combo Graphics RAM + SD Interface](/Sharp_MZ-80GMSD)
As my MZ-80B doesn't have an expansion unit I thought about trying to add the 8KB Graphics RAM expansion (MZ-80GMK) aka "GRAPHYCS-2" on the same board as the SD interface above.  The SD board itself is still external, but the connection to the MZ-80B motherboard is included with the graphics RAM expansion.

## Power 
My 80B came from Japan so expects 100VAC and not the 240VAC we use in Australia.

### DC Requirements
| Voltage          | Current | Use                                |
|------------------|---------|------------------------------------|
| +5V regulated    | 2.5A    | motherboard & tape deck            |
| -5V regulated    | 10mA    | DRAM                               |
| +12V regulated   | 1.25A   | monitor & tape deck                |
| +12V unregulated |         | 9.5V-16.5V for tape deck solenoids |

### Connectors
Thanks to [Brad](https://www.youtube.com/@zbradbell) for pointing out the power connectors used are very similar to [JST LV-type](/Datasheets/JST_LV_Connectors.pdf).  Brad did further digging and figured out that they are most likely actually TJC1-type.<br>

| Sharp ID      | JST ID       | Use                                         |
|---------------|--------------|---------------------------------------------|
| QPLGN0303CEZZ | B3P-LV       | 3-pin terminal for tape deck power on PSU   |
| DSOCN0083PAZZ |  3P-LV       | 3-pin socket & wires from tape deck to PSU  |
| QPLGN0103CEZZ | B1P-LV       | 1-pin terminal for monitor power on PSU     |
| DSOCN0083PAZZ | S1P-LV       | 1-pin socket & wire from monitor to PSU     |
| DSOCN0098PAZZ |  4P-LV       | 4-pin socket & wire from PSU to motherboard |
| QPLGN0403CEZZ | B4P-LV       | 4-pin terminal on motherboard               |
| QPLGN0303CEZZ | B3P-LV       | 3-pin terminal for Expansion Unit power     |
|               | SVF-01T-2.36 | Contact type for sockets                    |

- [QPLGN0303CEZZ](/Images/Sharp_MZ-80B_QPLGN0303CEZZ_1.jpg)
- [DSOCN0098PAZZ](/Images/Sharp_MZ-80B_DSOCN0098PAZZ_1.png)


