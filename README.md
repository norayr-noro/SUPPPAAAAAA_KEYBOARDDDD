# SUPPPAAAAAA_KEYBOARDDDD
<img width="667" height="352" alt="Screenshot 2026-06-02 132246" src="https://github.com/user-attachments/assets/b97d5a66-6c25-49ce-a6d4-7b303adf3ba8" />

This project is my version of a custom mechanical keyboard, brimmed up to the max with upgrades (which gives it the name suppaaaaaaa) for comparability to modern proffesional keyboards. It is inspired by the Keychron-V1-Max, but everything is custom, from the plate and case to the pcb and schematic! Before getting into this, I'd also like to say how much diffucult It sounded at first, but I think this is one of the best ways to learn how to design and layout a PCB, CAD and all sorts of stuff from this one project (thats one of the reasons why I wanted to this)!!!

# BOM
Here I'll put down all the components I will likely use in the full project (some of this is subject to change, esp. the switches):
| Item | URL | quantity needed | price total (USD) |
| ---- | ---- | ---------------- | ---------------- |
| cherry-mx style switches | https://tinyurl.com/46ueewwa | 82 | 33.74 | 
| Diodes (1N5817) | https://www.rapidonline.com/st-1n5817-schottky-diode-20v-1a-do41-47-2564 | 82 | 16.16 | 
| 330 ohm resistor  (THT) | https://tinyurl.com/3mh5jma3 | 1 | 2.29 | 
| 4.7K ohm resistor (THT) | https://tinyurl.com/2bpn6xam | 4 | 6.06 |
| 820K ohm resistor (THT) | https://tinyurl.com/4xysbk3m | 1 | 0.02 |
| 2 Mohm resistor (THT) |  https://tinyurl.com/4fxpa99j | 1 | 2.07 | 
| Nice!Nano v2 |  	https://shorturl.at/wlaR4 | 1 | 8.48 | 
| EC11 rotary encoder | https://www.ebay.co.uk/itm/113261494197?var=413549335980 | 1 | 4.94 |
| TPO4056 |  https://www.ebay.co.uk/itm/405070463792?chn=ps&_ul=GB&mkevt=1&mkcid=28&google_free_listing_action=view_item | 1 | 2.42 | 
| LiPo 10000mah 3.7v (battery) | https://tinyurl.com/yc5u3hex | 1 |8.36 | 
| OLED 0.91" | 	https://shorturl.at/Vc0Sg | 1 |5.25 | 
| SS11D10 slide switch | 	https://shorturl.at/1174X | 1 |2.06 |
| USB-A dongle (wireless) |  https://shorturl.at/GAQIp | 1  |  8.07 | 
| SK6812MINI-E (RGB-LED) |  https://tinyurl.com/37m9v9hy | 62 |  4.46 |
| 470 uf capacitor (THT) | https://www.rapidonline.com/panasonic-eca1vm471-470uf-20-35v-85-c-radial-aluminium-electrolytic-11-2172 | 1 |  0.44 |
| MT3608 DC to DC | 	https://tinyurl.com/52ezaaav | 1 |  1.59 |
| kalih hotswap sockets |  	https://tinyurl.com/452x8dtk | 82 |  4.94 |
| (Optional) | URL | quantity | price |
| ----------- | ---- | ------- | ---- | 
| O-rings | 	https://tinyurl.com/y44esxp9 | 82 | 5.38 |
| keycap foam pads | https://tinyurl.com/4kc52tvw | 82 | 9.94 |
| foam gaskets | 	https://tinyurl.com/5hd465du | 82 | 6.48 |
 
 

# 🧠 Design
This project started out by firstly making the schematic, loosely following the design by scotto keebs on [YouTube(https://www.youtube.com/joe_scotto)]

The microcontroller is used to control the entire PCB itself, like the brain of the PCB. For this build I'll be using the Nice!Nano v2, since It would have more gpio pins than the Xiao seeduino using the same nrf52840 chip, and It has the same wifi and bluetooth capabilites. I also added a Gpio extender for the columbs of the switches just because I ran out and chose to stick with the nice nano, and that there would be too many variable changes.

In my design I'll be using a DC-DC converter step-up, to efficently power the SK6212 MINI-E RGB-LEDs which run on 5v instead of the 3v3 which the rest of the board runs. And for the power I'll be using a cheap TP4056 for the usb-c power and a big 10000mah LiPo battery for the long time able to use.
I'll also be using a usb-a dongle for low-latency communication to the laptop/PC 
The extra addons I have added is a rotary encoder knob likely which would be used in noise, a OLED 0.9' screen for cool displays and battery charge, plus the hotswap sockets and the rgb lighting for the premuium look!!!! (and also the optional addons which are not in the total price but may also be added for that nice keyboard feeling)

(schematic and pcb)
<img width="934" height="563" alt="Screenshot 2026-05-20 112616" src="https://github.com/user-attachments/assets/da408af2-d65c-438d-8002-3256981abecb" />
<img width="1002" height="391" alt="PCB_full" src="https://github.com/user-attachments/assets/d9044ae1-3cab-4bf7-9fe1-241ab87349f5" />


KiCad was used to design the schematic and PCB layout
Fusion 360 was used to create the keyboard case and plate.
The case surrounding the pcb is literally a square — Mostly because im not good at all in 3d modeling...(but if you at CAD software its a really easy thing!)

# ⚙️ Firmware
The keyboard is planned to run on [ZMK firmware(https://zmk.dev/docs/features/split-keyboards)], which offers: ZMK was chosen mostly because it's quite flexible, especially for custom keyboard builds.


🚀 Next Steps
The final steps are to fully solder and assemble the PCB, upload the firmware, and wait for the print to finish

# 💭 Final Thoughts
This project was definetly harder than you'd expect it would be but, it was one of the coolest projects I think I have done, and hope to finish this early to actualy see the full thing assembled

Photos of the finished CAD model and the PCB !!!!
<img width="897" height="387" alt="Plate_(final)" src="https://github.com/user-attachments/assets/2211ec76-566b-44f9-8e13-7c17cb729299" />
<img width="962" height="510" alt="PCB_full(diff perc )" src="https://github.com/user-attachments/assets/f909ad8a-5e57-4e89-a59d-475484741fd8" />
<img width="693" height="402" alt="CAD_FULL" src="https://github.com/user-attachments/assets/d31c335f-8f33-4112-ae3f-8ee23001abdc" />
<img width="613" height="335" alt="bottomcase_final" src="https://github.com/user-attachments/assets/26b6467a-4525-40e8-a261-586fd1b69e41" />
<img width="973" height="451" alt="topcase_(final)" src="https://github.com/user-attachments/assets/0aefa14c-f0e0-4796-b907-22c8be022fe1" />






<img width="1152" height="503" alt="PCB_3d(front)" src="https://github.com/user-attachments/assets/a9b6e555-87f9-487a-ac13-d8ccbd27aa54" />
(front and back of PCB)
<img width="995" height="607" alt="PCB_3d(back)" src="https://github.com/user-attachments/assets/7bcee45c-7b9e-4128-998c-8c267db533e5" />



Ill also attach the .step file for the PCB and the .f3d file for the 3d model i have worked on to this repository for future reference...
