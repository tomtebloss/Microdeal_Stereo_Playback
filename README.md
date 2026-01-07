<h1 align="center">
Microdeal Stereo Playback
</h1>

<h2 align="center">
Atari ST stereo playback cartridge from Microdeal. Remake from original cartridge.
</h2>

---
 
<img title="Original Stereo Playback Cartridge" style="width:43%" align=top src="Pics/old_case.jpg"><img title="Original Stereo Playback Cartridge - inside" style="width:56%" align=top src="Pics/old_inside.jpg">

---
 
<img title="Three versions of Stereo Playback Cartridge" style="width:100%" align=center src="Pics/3v_finished_bottom.jpg">

---

## Three versions  

All of the threee versions derive from  the same schematics so the sound produced should is the same. I bought the original cartridge with the intention to revere engineer the scematics. The through hole versions has more or less the same track and component placement as the original. The two smt versions is the same but two different RCA connector was used. All the pcb's have pads for the signals as well if you want to use panel mount rca jacks.

---

## Cartridge Orientation
>[!CAUTION]
><font color="red">All the components should be faceing down when inserting the cartidge in the port!</font>  
>
>I can't stress this enough. As the original, the cartridge "seems" to be upside down. I followed the same design. The silkscreen says what is top and bottom as well.



Bill of material (BOM is included in each gerber zip)

| Quantity | Value          | Package THT      | Package SMT                        | Device/Description                                         |
| :---     | :---           | :---             | :---                               |:---                                                        |
| 2        | 0,1 µF         | C050-024X044     | C0805                              | Capacitor, ceramic (THT: 5mm leg spacing, SMT: 0805)       |
| 4        | 1 µF           | C050-024X044     | C0805                              | Capacitor, ceramic (THT: 2,5mm leg spacing, SMT: 0805)     |
| 2        | 10 µF          | E2.5-5           | SANYO-OSCON_SMD_B6<br>ø5x5.4mm     | Electrolytic Capacitor,<br>(THT: 2,5mm leg spacing, ø5x11mm) (SMT: B6 ø5x5,4mm)   |
| 2        | 47 µF          | E2.5-5           | SANYO-OSCON_SMD_C6<br>ø6.3x5.8mm   | Electrolytic Capacitor,<br>(THT: 2,5mm leg spacing, ø5x11mm) (SMT: B6 ø6,3x5,8mm) |
| 2        | 10 kΩ          | 0207/10          | R0805                              | Resistor, Carbon film (THT: 0,25W 5% tolerance, SMT: 0805) |
| 2        | 100 kΩ         | 0207/10          | R0805                              | Resistor, Carbon film (THT: 0,25W 5% tolerance, SMT: 0805) |
| 1        | 390 Ω          | 0207/10          | R0805                              | Resistor, Carbon film (THT: 0,25W 5% tolerance, SMT: 0805) |
| 2        | 3,9 kΩ         | 0207/10          | R0805                              | Resistor, Carbon film (THT: 0,25W 5% tolerance, SMT: 0805) |
| 2        | 20 kΩ (1%)     | 0207/10          | R0805                              | Resistor, Metal film (THT: 0,6W 1% tolerance, SMT:0805)<br>(All 0805 is 1% so this doesn't matter) |
| 1        | XXX7528        | DIP20            | SOIC127P1032X265-20N<br>SOIC-20    | AD7528, TLC7528 or MX7528. 2 Channel Digital to Analog<br>Converters - DAC CMOS 8-Bit Buffered Multiplying <br>AD7528 (Analog Devices), TLC7528 (Texas Instrument) or<br>MX7528 (Maxim) will also work. Original have AD7528. |
| 2        | BC549B, BC849B | TO-92            | SOT95P237X125-3N (SOT-23)          | Bipolar Transistor. BJT, 30V, 100mA, NPN.<br>(SMT: I have tried with BC848B as well and it works but sounds<br>a bit different. 849 is low noice. Use 849 if you can)
| 1        | Zener diode    | DO-35            | MELF3516 or MELF_DO-213AB<br>SOD80 | Zener Diode 2.7V 500mW (THT: I used BZX55C2V7 in my test built)<br>(SMT: Choose one of the two footprint. 0,5W power dissipation.<br>2,7V. ±5%. I used a BZV55B2V7 for this one.)
| 2        |                | RCJ-041          | RCJ-041 or WBTOR1                  |

---

## Enclosure

There is no enclosure at the moment. I'm not a 3D designer. If anyone makes one, please contact me so I can add it to this repository. There is two hole on the THT pcb as the original. I don't think it will fit in the original case. I haven't tested that to be honest. The two SMT versions have one hole and two notches on the side of the pcb. So it should be easy to make an enclosure for it. But what do I know.

| Solder 1 PCB with chips and capacitors. Take note of the orientation on pin 1 on PCB and chip (pin 1 is marked with circle on PCB. Notch on the left side of chip and text is readable (not upside-down) then pin 1 is located on bottom left side. (I hadn't a photo of PCB without pins soldered in - So disregard that)| <img title="RAM PCB" style="width:54%" src="images/RAM PCB soldered.jpg">   <img title="RAM chips" style="width:45%" src="images/RAM chips.jpg">|
| :--- | :---: |
| Cut pinheaders and place on motherboard. I did lower right side then a few here and there to get it straight. Do ***_NOT_*** solder in. Place PCB on top of unsoldered pins. Solder the RAM PCB first when it's resting on the motherboard pins. Lift RAM PCB and put in a few more of the single pins. Put RAM PCB back and solder those. Keep doing until you have all the pins soldered on the RAM PCB. Then put the RAM PCB back on motherboard. Trim the lenght of pins and solder the pins underneath the motherboard. | <img title="Placement of pins on motherboard" style="width:38%" src="images/no solder holes with ring.jpg">   <img title="Pin placment on RAM PCB" style="width:61%" src="images/RAM PCB placed on pins low angle.jpg"> |
| Looks good. A few steps left now. | <img title="RAM PCB soldered in" style="width:60%" src="images/RAM PCB soldered in angle.jpg">   <img title="RAM PCB soldered in" style="width:38%" src="images/RAM PCB soldered in straight.jpg"> |
| Solder the three resistors if they are missing (68ohm through hole) on R71, R72 and R73 for the CAS1H, CAS1L and RAS1 signals on the motherboard. | <img title="Missing resistors R71, R72 and R73" style="width:100%" src="images/resistors not soldered.jpg"> |
| A9 (or MAD9) needs to be connected from RAM PCB to MMU with a wire. MAD9 is located on [PLCC MMU on pin 64](images/A9%20connected%20on%20PLCC%20pin%2064.jpg) and SMD MMU on pin 66. If the PLCC chip is in socket it is easier to solder to pin 64 underneath the motherboard. | <img title="A9 wire connected" style="width:100%" src="images/A9 connected.jpg"><br><img title="SMD MMU" style="width:57%" src="images/mmu smd.png"> <img title="PLCC MMU" style="width:41%" src="images/mmu plcc.png">|

---

## Useful info

You do not need a hot air station/gun. Chip can be desolder by bending a thick copper wire around all legs and then adding a lot of solder. By dragging the soldering iron across the wire and all the legs on each side, the chip will eventually come loose. It will be messy. Desolder the exess with braid. The SMD RAM chips is soldered on RAM PCB with drag soldering and a knife edge on the soldering iron. If you are more comfortable using other methods, use that! Flux is your friend. Use alot of flux!

---

## Testing

Use [SYSINFO] to test if you have 4Mb.

<img title="Sysinfo v8.37" width="500rem" src="images/sysinfo.png">

---

PCB made by Daniel Guldkrans aka DoG in Eagle January 2024.


