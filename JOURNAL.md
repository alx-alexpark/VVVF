---
title: "VVVF Inverter"
author: "@alex (p variant)"
description: "Building my own variable voltage variable frequency (vvvf) inverter, just like the ones that power electric trains!"
created_at: "2025-05-24"
---

# May 24th: Did research on how to build a VVVF inverter, and started with basic schematic

Recently, I stumbled upon a [few](https://www.youtube.com/watch?v=2mjUHKlSBy4) [youtube](https://www.youtube.com/watch?v=4SfN0O-F9hM) [videos](https://www.youtube.com/watch?v=mKpIqNNc9Kw) that made me really interested in the sounds that electric trains make. I discovered that many people made their own traction inverters to recreate these sounds, and I figured I wanted to try as well. Originally, I started this project a few months ago, but I hadn't made much progress.

I looked for ways I could aquire the needed 3 phase motor for cheap. Thinking of perhaps buying a cheap washing machine off Facebook marketplace.

Also looked at gate drivers, thought that the TI UCC21520ADW would be a good gate driver IC due to its various protections and being a complete half-bridge driver which makes it a lot simpler for me.

From this, I drew up a quick schematic using the above IC. 

![image](https://github.com/user-attachments/assets/87b510aa-837d-4e5f-a4cc-9f309eb8f0d5)

**Total time spent: 3h**

# May 25th: Decided on a MOSFET, added current monitoring, brake chopper, and Raspberry Pi Pico MCU

So today I decided to use MOSFETS instead of IGBTs because they are a lot simpler. I chose IPDD60R037CM8XTMA1 MOSFETs because they were rated for the high voltage and they had a good exposed thermal pad that I could easily attack to a large heatsink. 

I also added a hall-effect current sensor to one of the phases, and a Raspberry Pi Pico MCU. I drew up a good amount of schematic today.

![image](https://github.com/user-attachments/assets/7840d77f-32a2-4162-8981-cafc1e2ce8c6)

Some parts I selected
![image](https://github.com/user-attachments/assets/2abb6cb0-ef22-4894-8222-acf2e3a6a67d)


**Total time spent: 5h**
