---
title: "Kumo"
github: "https://github.com/Rexaintreal/Kumo"
description: "A smart, expressive quadruped walking robot with ML and TTS, based on Sesame."
created_at: "2026-11-19"
total_time: "2.5h"
---

## November 27, 2026: Finishing the BOM and fixing the power supply

was really busy with practicals finally got time for kumo, The BOM was unfinished last time because the power supply was not sorted T_T so thats what i fixed today in the [BOM](https://github.com/Rexaintreal/Kumo/blob/main/BOM.csv) is done now except the 3D prints whihc will be added later

![Battery listing](https://raw.githubusercontent.com/Rexaintreal/Kumo/main/assets/battery.png)

### Power supply

sooo i picked a 7.4V 1000mAh 2S 145 00 pack with a Charging cable included so no separate charger needed ig its a bit weird as the listing has no reviews and 1000mAh seems too much for 14500 cells so i will check the real specs when i receive it The LM2596 buck stays and will be set to 5.1V with a multimeter before anything gets connected just to be safe :pray

### Connector

intiially i thought of an XH2.54 3 pin pigtail but the battery comes with a 4 pin SM plug so that would not even fit i swapped it for a JST SM 4 pin connector with wire Its only rated for about 1A so the main power path will use the thicker 22AWG silicone wire!

- Final total is about $44.82 or ₹4194

### Not in v1

alsoooo i am skipping the mic and speaker sadly :( for v1 so ML and TTS will come later and 3d printing will be done by a print on demand service in my city so i will get a quote once the CAD is ready!!!

**Total time spent: 0.5h**


## November 19, 2026: Project setup and file structure

Created the file structure and finalized the project scope and features created basic strucutre with all the folders and all made sure it fits well with fabricate sync structure

![Repo setup and project start](https://raw.githubusercontent.com/Rexaintreal/Kumo/main/assets/Journal1.png)

**Total time spent: 0.3h**

## November 20, 2026: Sourcing parts and making the BOM

Spent today picking all the parts for Kumo and putting them in the [BOM](https://github.com/Rexaintreal/Kumo/blob/main/BOM.csv). Its based on Sesame so i started from its parts list and changed stuff to fit my own features like ML and TTS

![Bill of materials](https://raw.githubusercontent.com/Rexaintreal/Kumo/main/assets/BOM.png)

### Brain and display

The brain is an ESP32-S2 Mini. Small with built in wifi and enough pins for all the servos and the screen

![ESP32-S2 Mini](https://raw.githubusercontent.com/Rexaintreal/Kumo/main/assets/esp32s2mini.png)

For the face i went with an OLED so Kumo can show different emotions while walking

![OLED display](https://raw.githubusercontent.com/Rexaintreal/Kumo/main/assets/oled.png)

### Motion and power

Legs run on servo motors, one for each joint

![Motor](https://raw.githubusercontent.com/Rexaintreal/Kumo/main/assets/Motor.png)

Servos pull a lot of current and the ESP32 needs a steady supply so there is a buck converter to bring the battery voltage down. Also added a switch to turn the whole robot on and off

![Buck converter](https://raw.githubusercontent.com/Rexaintreal/Kumo/main/assets/buckConverter.png)

![Switch](https://raw.githubusercontent.com/Rexaintreal/Kumo/main/assets/switch.png)

### Wiring

For connections i got a prototype board, header pins so stuff can be unplugged and terminal wire for the power lines

![Prototype board](https://raw.githubusercontent.com/Rexaintreal/Kumo/main/assets/prototypeBoard.png)

![Header pins](https://raw.githubusercontent.com/Rexaintreal/Kumo/main/assets/headerpins.png)

![Terminal wire](https://raw.githubusercontent.com/Rexaintreal/Kumo/main/assets/terminalWire.png)

Legs move all the time so the wires need to be soft. Silicone wire bends way easier than normal wire and wont snap after a lot of movement

![Silicone wire](https://raw.githubusercontent.com/Rexaintreal/Kumo/main/assets/wiresilicon.png)

### Small hardware

Screws for the body and servo mounts, heat shrink for solder joints and zip ties to keep the cables tidy

![Screws](https://raw.githubusercontent.com/Rexaintreal/Kumo/main/assets/screws.png)

![Heat shrink](https://raw.githubusercontent.com/Rexaintreal/Kumo/main/assets/heatshrink.png)

![Zip ties](https://raw.githubusercontent.com/Rexaintreal/Kumo/main/assets/zipties.png)

### Still unfinished

The BOM is not done yet Still need to fix the power supply and figure out the DC to DC connector setup. Once thats sorted i can start the CAD for the body and legs :3

**Total time spent: 1.7h**
