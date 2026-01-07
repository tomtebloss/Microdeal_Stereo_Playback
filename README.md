<h1 align="center">
Microdeal Stereo Playback
</h1>

<h2 align="center">
Atari ST stereo playback cartridge from Microdeal. Remake from original cartridge.
</h2>

---
 
<img title="Three versions of Stereo Playback Cartridge" style="width:100%" align=center src="Pics/3v_finished_bottom.jpg">

---
 
<img title="Three versions of Stereo Playback Cartridge" style="width:100%" align=center src="Pics/3v_finished_bottom.jpg">

---

## Three versions  

All of the threee versions derive from  the same schematics so the sound produced should is the same. I bought the original cartridge with the intention to revere engineer the scematics. The through hole versions has more or less the same track and component placement as the original. The two smt versions is the same but two different RCA connector was used. All the pcb's have pads for the signals as well if you want to use panel mount rca jacks.

---

## All the components should be faced down when inserting the cartidge in the port. 

I buy SIMM modules from eBay and desolder the chips on it with a hot air station/gun. But you can also buy them individually. That will probably be more expensive. Below you see a picture of a double sided 8Mb, 72 pin SIMM module. 4Mb single sided SIMM can also be found. It can have 2 or 3 chips on each side (I have only seen 2 chip variant). If 3 chips then one chip would be different and that chip is for the parity bit calculation. That is not needed. I used FPM memory here. I have not tried EDO. 

Chips that can be used on this PCB is 1048576-word by 16-bit dynamic random access memories. Speed is usually between 60ns to 80ns. Lower number is faster.

<img title="8Mb SIMM 72 pin" style="width:55%" align=right src="images/SIMM.jpg">

| Manufacturer      | Chip code   |
| :---              | :---        |
| Hitachi           | HM5118160   |
| OKI Semiconductor | MSM5118165  |
| Samsung/SEC       | KM416C1200 and K4F151611 |
| Texas Instruments | TMS418160   |
| NEC               | UPD4218160  |
| HTL               | HT5118160   |
| ACTCTS            | TM5116100   | 
| NPN               | NN5118160   |
| Micron            | MT4C1M16C3DJ|


---

## How to

Start by desoldering all the ram chips on the motherboard. Either by hot air station/gun or with braid/solder pump. Beware of delaminatiton and warping of the motherboard if you heat it to long on the same place. If you don't have any plans for the old ram, just snipp all the legs on the chips with a flush cutter. Then desolder only the pins you need to fit the RAM PCB. Also some decoupling capacitors needs to be desoldered. They are a bit thicker then the plastic on the pin headers. The PSU sits on top of the RAM so hardly any room exist. ***So do _NOT_ use sockets!***

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


