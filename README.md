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
 
 Notes on the BOM: Firstly, I would like to say that the keys I chose are quite expensive, and if needed, can easily be replaced by much, much cheaper ones (if you want to, of course  I chose these because their peak and sound reallllly good). Secondly, you can change the lipo too to a bit bigger or smaller type, I chose 10000mAh since it was a nice middle number between huge and smaller similar lipos. Also, the DC-DC converter is there for the RGB LEDs to power them at 5V optimally instead of the half-working 3V3 it would get from the lipo or the MCU. And lastly, the optional section, like the O-rings, the hot-swap sockets, are there if you want to, but the PCB would work fine without them.

# 🧠 Design
This project started out by firstly making the schematic, loosely following the design by Scotto Keebs on [YouTube(https://www.youtube.com/joe_scotto)]

The microcontroller is used to control the entire PCB, like the brain of the PCB. For this build, I'll be using the Nice!Nano v2, since It would have more GPIO pins than the Xiao seeduino using the same nrf52840 chip, and It has the same wifi and Bluetooth capabilities (also really good documentation for custom keyboard firmware). I also added a Gpio extender for the columbs of the switches just because I ran out and chose to stick with the nice nano, and that there would be too many variable changes. (if you want you could change the mcu and extender design to a picoW or something with an nrf52840 chip, and it wouldn't really change a lot)

In my design I'll be using a DC-DC converter step-up, to efficently power the SK6212 MINI-E RGB-LEDs which run on 5v instead of the 3v3 which the rest of the board runs. And for the power I'll be using a cheap TP4056 for the usb-c power and a big 10000mah LiPo battery for the long time able to use.

I'll also be using a USB-A dongle for low-latency communication to the laptop/PC 
The extra addons I have added is a rotary encoder knob, likely which would be used in sound config, an OLED 0.91' screen for cool displays and battery charge, plus the hot-swap sockets and the rgb lighting for that premium look!!!! (and also the optional addons which are not in the total price but may also be added for that nice keyboard feeling yk)

(schematic and PCB)
<img width="934" height="563" alt="Screenshot 2026-05-20 112616" src="https://github.com/user-attachments/assets/da408af2-d65c-438d-8002-3256981abecb" />
<img width="1002" height="391" alt="PCB_full" src="https://github.com/user-attachments/assets/d9044ae1-3cab-4bf7-9fe1-241ab87349f5" />

For the PCB KiCad was used for the schematic and PCB layout and a plugin for the production files
And for the 3d models of the case and plate, Fusion360 was used just because it's one of the free versions of CAD software and imo one of the easier software to learn and use

# ⚙️ Firmware
-(n/a)

# 💭 Final Thoughts
This project was definitely harder than you'd expect it would be, but it was one of the coolest projects I think I have done, and I hope to finish this early to actualy see the full thing assembled

Photos of the finished CAD model and the PCB !!!!
<img width="897" height="387" alt="Plate_(final)" src="https://github.com/user-attachments/assets/2211ec76-566b-44f9-8e13-7c17cb729299" />
<img width="962" height="510" alt="PCB_full(diff perc )" src="https://github.com/user-attachments/assets/f909ad8a-5e57-4e89-a59d-475484741fd8" />
<img width="693" height="402" alt="CAD_FULL" src="https://github.com/user-attachments/assets/d31c335f-8f33-4112-ae3f-8ee23001abdc" />
<img width="613" height="335" alt="bottomcase_final" src="https://github.com/user-attachments/assets/26b6467a-4525-40e8-a261-586fd1b69e41" />
<img width="973" height="451" alt="topcase_(final)" src="https://github.com/user-attachments/assets/0aefa14c-f0e0-4796-b907-22c8be022fe1" />

(with the PCB
<img width="841" height="493" alt="full_parts" src="https://github.com/user-attachments/assets/78e30b8a-213c-4d28-9b38-8cfe783a7795" />
<img width="852" height="437" alt="full_parts2" src="https://github.com/user-attachments/assets/0f373ee9-841e-4611-a977-b6fee50c7400" />
)


(oh and also the assembled full model available in the 3d case + plate folder as *full_asembly.step* )
<img width="634" height="331" alt="full_assembly2" src="https://github.com/user-attachments/assets/d38f0809-e10e-4128-9e7b-bf051ae155c9" />
<img width="774" height="370" alt="full_assembly" src="https://github.com/user-attachments/assets/5c287d9f-c6cc-4c52-a0c8-2feb8248df1b" />


<img width="1152" height="503" alt="PCB_3d(front)" src="https://github.com/user-attachments/assets/a9b6e555-87f9-487a-ac13-d8ccbd27aa54" />
(front and back of PCB)
<img width="995" height="607" alt="PCB_3d(back)" src="https://github.com/user-attachments/assets/7bcee45c-7b9e-4128-998c-8c267db533e5" />



I'll also attach the .step file for the PCB and the .f3d file for the 3d model i have worked on to this repository for future reference...
