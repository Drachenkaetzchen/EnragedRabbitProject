
# EnragedRabbitProject

Welcome to the Enraged Rabbit Project Github page!

This project aims to bring multimaterial capabilities to 3D printers using a single Direct Drive toolhead. While this project is mainly dedicated to be used on VORON printers, it can also be used (or adapted) on any 3D printer that runs Klipper, and  
potentially RRF.

You like this project? You want to support me and my work, help me bring new cool stuff to the community? Well you can tip me here :
[![paypal](https://www.paypalobjects.com/en_US/FR/i/btn/btn_donateCC_LG.gif)](https://www.paypal.com/donate?business=C9MG5LQSQRKN4&currency_code=EUR)

## Table of Content
- [Changelog](#changelog)
- [Showroom](#showroom)
- [Videos](#videos)
- [Details](#details)
- [BOM](#bom)
- [Acknowledgements](#acknowledgements)
- [FAQ](#faq)
  - [General](#general)
  - [Carrot Patch](#carrot-patch)
  - [Carrot Feeder](#carrot-feeder)
 
## Changelog
- **September 17th 2021 :** The ERCF V1.1 assembly manual, STL files and the STEP file are now released! You'll find the manual in the "Documentation" section now, and the manual will keep growing with setup, tuning and slicer guides. A non-exhaustive patch note can be found in the Carrot_Feeder folder. Finally, note that the new software part of the ERCF V1.1 is not out yet, and the ERCF V1.1 hardware cannot be used with the ERCF V1.0 macros. V1.1 software will be released in a few days. Happy printing and assembly!
- **September 14th 2021 :** Updated the BOM to ERCF V1.1 (release coming soon! tm) and added the new, incoming Toolhead Sensor BOM (bottom tabs)
- **June 4th 2021 :** TopHatLockers and related (servo arm, TopGearHat, macros) have been released to the main branch, from the EarlyDevAccess branch. If you're already running EarlyDevAccess stuff, that won't change anything for you
- **June 2nd 2021 :** Release of Carrot Patch V1.1
   - Increased handles section near the threaded insert for more robustness
   - Removed useless chamfer on feet bottom screw holes and increased hole depth (one can now properly use M3X8 SHCS to secure the Carrot Patch on 2020 extrusions)
   - Fixed several parts lengths//size that impacted the buffer wheel installation. Now the wheel should slightly touch both side walls (to avoid any possible gaps) while being able to turn (but not freely, which is on purpose)
   - Buffer Cross bottom arm is now secured using a M3X20 SHCS screw that comes from the bottom (that is also securing the left feet of the Carrot Patch)
   - Buffer Cross ECAS insert has been tuned, reinforced and a "bridge" shape has been added. Inserting the ECAS will no longer crack the plastic
   - Increased the size of the Buffer Cross "pillar" that sits between the two PTFE paths (some users previously reported fragilities due to the lack of matter for this pillar)
   - Updated the assembly manual, BOM and the CAD accordingly
   - Only parts that did not change are : [a]_Buffer_Wheel, [a]_Latch, [a]_Sliding_Arm, Buffer_Axis, Ptfe_Entry_ECAS and Ptfe_Entry_M10

## Showroom

<img src="Showroom/Benders.png" alt="Benders" width="950"/><img src=Showroom/Bimaterial_logo.png alt="Voron Logo TPU" width="650"/><img src=Showroom/5_colors_test.png alt="5_colors_test" width="300"/><img src=Showroom/9_colors_test.png alt="9_colors_test" width="400"/><img src="Showroom/Gustav_brothers.png" alt="Gustav brothers" width="550"/>

## Videos
Here are videos of the system in action. I need to release more videos...

https://streamable.com/3lo192

https://streamable.com/cjl2iz

## Details

There are 4 components so far : 
 - **The Enraged Rabbit Carrot Feeder (ERCF)**. The Carrot Feeder allows to use a high number of different filaments (tested up to 9 channels so far) and feed them, one at a time, into the printer toolhead. The ERCF gear motion system (i.e. what is used to push and pull the filament) is based on the Voron Design M4 extruder. The ERCF was inspired by the Prusa MMU2 and the Smuff.

  <img src="https://cdn.discordapp.com/attachments/842792223769624605/888344547501940736/20210917_103629.jpg" alt="Carrot Feeder" width="600"/><img src="https://cdn.discordapp.com/attachments/842792223769624605/888344548298874880/20210917_103640.jpg" alt="Carrot Feeder 2" width="600"/>
 
 - **The Enraged Rabbit Carrot Patch (ERCP)**. It is a light spool-holder and buffer combo to help you deal with the filament  
management issue associated with multimaterial systems.
 
 <img src="https://cdn.discordapp.com/attachments/788818216260337664/807282522756350022/image0.jpg" alt="Carrot Patch" width="300"/><img src="https://cdn.discordapp.com/attachments/500407802414628876/806108474668613632/20210202_112459.jpg" alt="Carrot Patch 2" width="300"/>
 - **The Enraged Rabbit King's Seat (ERKS)**. The King’s Seat is a pellet-purge system to remove the need for a wipe-tower and make faster filament purges. This system is designed for Voron V2s only so far.
 - **The filament sensor** : a filament sensor system located below the extruder gears to check proper loading and unloading of filament.
  
Note that this is a work in progress !!
 
Only the King's Seat is yet to be released !
 
## BOM
 The BOM for those components can be found [here](https://docs.google.com/spreadsheets/d/1A_qeNeaVprh_iPbvLcLjvJ2o2NfCzjuJam3K3RkWW0w).
 
## Acknowledgements

Thanks to the VORON Design devs and VORON discord members for the discussions and support, with a special thanks to the #honhonhonbaguette-FR members and @Tircown#8715!!
 
## FAQ
### General
**Q:** In what material should this be printed with?  
**A:** The whole design assumes it's printed in ABS, so printing it in PLA or PETG may result in poor fits or tolerances.


**Q:** What materials can be printed with the Enraged Rabbit?  
**A:** So far, PLA, PETG, ABS and TPU were all tested with success. For TPU, both 95A and 30D (~80A) were tested and could be loaded//unloaded using the Enraged Rabbit Carrot Feeder. While the 95A TPU was also working well with the Carrot Patch spool holder + buffer combo, the 30D TPU is way too soft to make filament "loops". If you plan to use such ultra-soft TPU, make sure the concerned Carrot Patch is located in a "clean" area (to avoid your TPU buffer length to be caught on something) or use another buffer//spool holder.


**Q:** Can I use this system on another printer than a VORON V2?  
**A:** Yep, as long as your printer is running Klipper you should be good to go. Make sure the toolhead you are using have a filament sensor below the extruder gear (VORON AfterBurner, Galileo and LGX on AfterBurner are officialy supported, but plenty other toolheads have been modified to fit such a sensor, look in the usermods folder of this repo).


**Q:** Can I use a dedicated control board?  
**A:** Of course, Klipper allows you to use as many MCUs as you want. In the end you'll need to control 2 stepper motors, 1 5V servo, 1 mechanical switch, 1 IR sensor and 1 filament detector. You can find a dedicated PCB, made by @Tircown, here : https://github.com/Tircown/ERCF-easy-brd.


### Carrot Patch
**Q:** How does this work?  
**A:** The spool holding part is a direct copy of the nominal spool holder on Vorons, i.e. an arm with a 4mm PTFE tube on which the spool rests and turns around. The buffer part of the Carrot Patch, which is inspired from several similar open-source designs, consists of a big wheel located in a filament "cage". Filament from the spool enters the filament cage, makes a few turns around the wheel and then exit the cage through a PTFE tube. When the extruder pull filament during a print, the filament will encircle the buffer wheel, which will simply turn to go along with the extruder pulling. When there is a retract // unload, the filament will be pushed back in the filament cage, making big loops (as much as the cage allows, so roughly 15 cm diameter), storing the filament buffer length in the cage. More filament turns around the wheel implies a longer buffer length. Use 4 turns form a buffer of around 120 cm. 


**Q:** Why not use a spool rewinder instead of a buffer?  
**A:** Usual rewinders are using either a sprint or a counterweight of some sort (nuts, bearing, spool itself...). The result is that it will rewind a certain number of spool turn, not a defined filament length (an almost empty spool will have a very small rewinding capabiliy). Also VORON V1s and V2s are big printers and the reverse bowden is usually quite long (around 80cm), meaning that typical rewinding solutions are not enough anyway. On the other hand, a buffer like the one on the Carrot Patch can handle very long filament buffer length.


**Q:** The buffer wheel recess on the buffer cross has a smaller diamater than the buffer wheel itself, is this normal?  
**A:** Yes. Goal of this recess is just to reduce the total contact surface between the wheel and the buffer cross "wall", while conserving a direct contact with the edge of the wheel.

### Carrot Feeder
**Q:** How many channels can I build on the Carrot Feeder?  
**A:** Only mechanical limitation will come from the length of the 5mm D-cut shaft that holds the Bondtech-type Gears. Typically people are using 6, 9 or 12 channels, but you can go from 2 to whatever in theory.


**Q:** Is there a cutter blade on the Carrot Feeder?  
**A:** No, and there won't be (there is no need for that).


Thanks !!

Ette
