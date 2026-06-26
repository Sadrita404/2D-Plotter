
|Title | 2D Plotter |
|:-- |:--|
|Author | Sadrita Neogi|




## Overview

It's an hobby grade Pen Plotter which can plot upto A1 size pages and will be efficient to use . It is also very reliable to use it uses grbl software.I have made it open source and anyone can recreate this and also customize it as all the step files are provided . This is made up of 2020 Extrusion Rod with Nema 17 stepper Motor..

### Why I chose this project?
I have choosing this project since it's my from a long time. I have think about that. I want to build and pen plotter. Since whenever I seen this kind of plotted video in any social media, it just fascinated me like how it can just recreate the exact same copy that is on the desktop. So I have chosen this project since I have dream about this project and I like the concept, how the project works, how we can control the coordinates and make changes in the design.

### How to use this project
Use case of this project can be many according to the need, but for my I want to create stunning drawings that cannot be achieved by manually if possible, then it would take many hours, but then I can easily recreate this using this slaughter and also I am very fascinated about drawing about the blueprint of any structure, so it would be great. I can make blueprint of any structured using it since it can easily feed big size pages.


  
### Rough Sketch

<img width="4000" height="3000" alt="sketch" src="https://github.com/user-attachments/assets/3ff9f4a0-97d8-4a33-8bcb-374c7489df42" />
<p align="center">
  <img src="https://github.com/user-attachments/assets/3cdb06db-c108-412f-b30e-a9291ced51a7" width="400" alt="6" style="border-radius: 12px;" />
</p>

<div align="center">

|  | CAD WORK |  |  
| :-: | :-: | :-: | 
| <img src="https://github.com/user-attachments/assets/f5c7743b-1f06-4241-a43c-627ae9ecc500" width="250" alt="CAD Work 7" style="border-radius: 12px;" /> | <img src="https://github.com/user-attachments/assets/e98834b3-71f4-40d4-ba0b-56d94ce224ea" width="250" alt="CAD Work 11" style="border-radius: 12px;" /> | <img src="https://github.com/user-attachments/assets/5c28e564-cbb6-448d-a81d-56a01a2b84bd" width="250" alt="CAD Work 18" style="border-radius: 12px;" /> |
| <img src="https://github.com/user-attachments/assets/872a9898-b26c-4b78-a6f7-cdd62827ad8b" width="250" alt="CAD Work 22" style="border-radius: 12px;" /> | <img src="https://github.com/user-attachments/assets/4ec9f484-fb1b-41b3-bdf9-6eb06f371020" width="250" alt="CAD Work 25" style="border-radius: 12px;" /> | <img src="https://github.com/user-attachments/assets/b9170d58-b8fc-46b1-988f-aeb90732ed5d" width="250" alt="CAD Work 29" style="border-radius: 12px;" /> |
| <img src="https://github.com/user-attachments/assets/cf7c77ec-bcb4-4a07-af17-84814ae5d3e6" width="250" alt="CAD Work 32" style="border-radius: 12px;" /> | <img src="https://github.com/user-attachments/assets/d2e4d127-5f1f-48a8-97f4-6bf4affd3580" width="250" alt="CAD Work 34" style="border-radius: 12px;" /> | <img src="https://github.com/user-attachments/assets/8d54e0eb-73f6-4733-8819-c13c0237b8b0" width="250" alt="CAD Work 36" style="border-radius: 12px;" /> |
| <img src="https://github.com/user-attachments/assets/2760f595-ba16-4358-8565-80e33a8aea52" width="250" alt="CAD Work 39" style="border-radius: 12px;" /> | <img src="https://github.com/user-attachments/assets/2c65daa6-3e7f-4e44-9e25-55a56d8310cd" width="250" alt="CAD Work 42" style="border-radius: 12px;" /> | <img src="https://github.com/user-attachments/assets/1f62dfa5-557a-42c9-8a32-50be5da24e73" width="250" alt="CAD Work 47" style="border-radius: 12px;" /> |
| <img src="https://github.com/user-attachments/assets/f719e00a-8817-4589-a976-bd5b86d53faf" width="250" alt="CAD Work 49" style="border-radius: 12px;" /> | <img src="https://github.com/user-attachments/assets/a08bc2e9-9be8-49ee-8b94-c23aa2f8e1c5" width="250" alt="CAD Work 51" style="border-radius: 12px;" /> | <img src="https://github.com/user-attachments/assets/72b73a52-43e4-49f9-92dd-f50b3f03fc05" width="250" alt="CAD Work 52" style="border-radius: 12px;" /> |

</div>

---

## Wiring Diagram 

<p align="center">
  <img width="618" height="407" alt="44" src="https://github.com/user-attachments/assets/db57b136-b41c-432d-b8f7-8cbe54a79360" style="border: 2px solid #ccc; border-radius: 4px; padding: 4px;" />
</p>

## Setup

Once the machine is assembled and wired, firmware needs to be installed so that it can move.

### Flashing GRBL onto the Arduino
GRBL is the firmware which is going to run on the Arduino and interpret the G-code commands. The installation is fairly simple.

1. **Download the Arduino IDE** from their site, a program which allows to flash the Arduino with firmware.
2. **Download GRBL source code** `.zip` file from the GitHub repository: https://github.com/gnea/grbl/releases and unzip the grbl file.  
**Note:** Before we proceed, we need to modify the `config.h` file inside grbl to account for the lack of the Z axis.
3. **Open Arduino IDE and import the grbl file** via: `Sketch` -> `Include Library` -> `Add .ZIP Library...` *(it says .ZIP but the uncompressed file should be chosen)*.
4. **Navigate to the grblUpload sketch** via: `File` -> `Examples` -> `grbl` -> `grblUpload`.
5. **Connect the Arduino to the PC via USB** *(make sure the correct board and port is selected)*.
6. **Flash the sketch** through `Sketch` -> `Upload`.

### For more about the CNC shield - [DOC Link](https://mikroshop.ch/pdf/CNC-Shield-Guide.pdf)
---

### Connecting the Arduino to LaserGRBL
Connecting the Arduino to LaserGRBL (through which I will control the laser) is fairly simple.

1. **Download LaserGRBL** from their website: https://lasergrbl.com and install it.
2. **Connect the Arduino to the computer via USB**.
3. **Choose the correct port** and select **"115200" baud rate**, then click **Connect**.  

If the console shows `Grbl 1.1h`, the chip is connected.

##  Now for sending the G- Code to the Arduino I will use universal Gcode Sender 

**https://github.com/winder/Universal-G-Code-Sender**

- official website - https://winder.github.io/ugs_website/

- It is an open source software, which is used to control CNC machines to send G code to them and to use it


---

  
## Final Look ( Made in Fusion 360 )

<div align="center">

<img width="653" height="508" alt="61" src="https://github.com/user-attachments/assets/ee9a2b04-974a-4702-9400-4b2f7dcb986e" />

<img width="787" height="487" alt="62" src="https://github.com/user-attachments/assets/221eb54b-238e-419e-80ab-219d2eb10462" />

<img width="869" height="450" alt="63" src="https://github.com/user-attachments/assets/9358bbe8-f927-47bd-b198-839bd3665b6d" />

<img width="529" height="517" alt="65" src="https://github.com/user-attachments/assets/2da73543-3982-475f-b194-1d405e3c0c01" />

</div>



<div align="center">
  <h2> Bill of Materials</h2>
</div>

| Name | Purpose | Quantity | Total Cost (USD) | Link | Distributor |
| :--- | :--- | :---: | :---: | :--- | :--- |
| 3.5mm Cylindrical Plastic Spacer | For the Pulley | 1 | 2.76 | [Link](https://onlyscrews.in/products/cylindrical-plastic-spacer-assorted-pack-for-m3-screws) | onlyscrews |
| GT2 Open Loop Timing Belt | For the Pulley | 1 | 4.45 | [Link](https://robu.in/product/5-meter-x-gt2-open-timing-belt-6mm-width/?gad_source=1&gad_campaignid=17416544847&gbraid=0AAAAADvLFWeV6_fecEXW7yD2KwMGyNReC&gclid=Cj0KCQjwo_PRBhDNARIsAEcVALWX-X7-D_kdZfqBS0H3PcbnDxu5TxPluOkUvYZnYQs5FsCJWmV2Wf8aArWPEALw_wcB) | robu |
| Stepper Motor Cable extended | Cable with Connector for NEMA17 Stepper Motor | 3 | 1.40 | [Link](https://robu.in/product/pure-copper-1000-mm-cable-with-connector-for-nema17-stepper-motor/) | robu |
| Extrusion corner bracket | For the Extrusion Rod | 1 | 2.49 | [Link](https://robu.in/product/easymech-cast-corner-bracket-for-20x20-aluminium-profile-silver-4-pcs/?gad_source=1&gad_campaignid=17416544847&gbraid=0AAAAADvLFWeV6_fecEXW7yD2KwMGyNReC&gclid=Cj0KCQjwo_PRBhDNARIsAEcVALV4LRrPM7WoKxLHkLVne42PtrbHs_YY74AkHWUyAiKb2j37QFupw0UaAuZZEALw_wcB) | robu |
| Cable spiral wrap | For the Cable Protection | 3 | 2.75 | [Link](https://robu.in/product/black-insulated-braid-sleeving-tight-pet-wire-cable-protection-expandable-cable-sleeve-wire-gland/?gad_source=1&gad_campaignid=17416544847&gbraid=0AAAAADvLFWeV6_fecEXW7yD2KwMGyNReC&gclid=Cj0KCQjwo_PRBhDNARIsAEcVALW6Kckgv4_RCy8ybwQZHY9RICcNDHibvSeLLwSLn5JaX5Gj5kZvKG8aAs__EALw_wcB) | robu |
| Multistrand wire | For the circuit | 2 | 8.51 | [Link](https://robu.in/product/14awg-multicore-insulated-cable3-cores-silicone/?gad_source=1&gad_campaignid=17427802559&gbraid=0AAAAADvLFWeNFfLjYJ39W-nS_4sWbPF81&gclid=Cj0KCQjwo_PRBhDNARIsAEcVALWHMKavhQ1qHcP6qWESjeKDFIX7pnvpeTL9LZOoMlfDupwrSZbHsYwaAnDeEALw_wcB) | robu |
| M5 Nyloc nuts | For the Frame | 20 | 0.25 | [Link](https://onlyscrews.in/products/m5-nyloc-nuts-mild-steel-with-zinc-plating-dia-5mm?currency=INR&country=IN&variant=50059739463993&stkn=6e84ebfba1b8&gad_source=1&gad_campaignid=23633307277&gbraid=0AAAAA9sP2SSMnVaNCVLCqHI69jE9iy_BO&gclid=Cj0KCQjwo_PRBhDNARIsAEcVALWdsKVdWH_XK2kFfxyFlFbWvU02b3JNGJVffN5sYbhEzycMn1RRN14aAu9HEALw_wcB) | onlyscrews |
| M3 5mm | For the stepper motor | 20 | 0.35 | [Link](https://onlyscrews.in/products/m3-x-5mm-phillips-pan-head-ss-304-screw-dia-3mm-length-5mm) | onlyscrews |
| M5 X 40mm Hex Bolt | For the Frame | 20 | 1.31 | [Link](https://onlyscrews.in/products/m5-x-40mm-hex-bolt-ss304-dia-5mm-length-40mm?currency=INR&country=IN&variant=50078395760953&stkn=6e84ebfba1b8&utm_source=google&utm_medium=cpc&utm_campaign=inderans_campaign_copy&gad_source=1&gad_campaignid=22930701107&gbraid=0AAAAA9sP2SSH1r26WHc6b4kR6oHIPnyZj&gclid=Cj0KCQjwo_PRBhDNARIsAEcVALVO-lVKauidUwBHXRim8nEjOTEB246j9kEfbZuJn508WOhMlg3UoAgaAoGmEALw_wcB) | onlyscrews |
| M5 Bolts | For the frame | 25 | 3.39 | [Link](https://onlyscrews.in/products/m5-phillips-pan-head-ss304-assorted-box?currency=INR&country=IN&variant=50424708858169&stkn=6e84ebfba1b8&utm_source=google&utm_medium=cpc&utm_campaign=inderans_campaign_copy&gad_source=1&gad_campaignid=22930701107&gbraid=0AAAAA9sP2SSH1r26WHc6b4kR6oHIPnyZj&gclid=Cj0KCQjwo_PRBhDNARIsAEcVALXWckbz3mX8A3qACf22M_SuVkp5iQpOOqCkEK5ELHmQAk9AVEqthoEaApGoEALw_wcB) | onlyscrews |
| M5 Sliding Nuts | For the 2020 Extrusion Rod | 20 | 1.91 | [Link](https://onlyscrews.in/products/m4-profile-nuts-mild-steel-with-nickel-plating-for-3030-series-t-nut-hammer-nut-1?currency=INR&country=IN&variant=50662617383225&stkn=6e84ebfba1b8&gad_source=1&gad_campaignid=23633307277&gbraid=0AAAAA9sP2SSMnVaNCVLCqHI69jE9iy_BO&gclid=Cj0KCQjwo_PRBhDNARIsAEcVALWc8-48KAZuBMJriR3emVEtklfOenfcqTM75vcJjYbDCRYzP7gtBcMaAtGPEALw_wcB) | onlyscrews |
| Aluminium Spacer (M5) | For the Pulley | 4 | 4.19 | [Link](https://robu.in/product/lot-aluminium-spacer-5x8mm-7mm-width-silver-4pcs/?gad_source=1&gad_campaignid=17416544847&gbraid=0AAAAADvLFWeV6_fecEXW7yD2KwMGyNReC&gclid=Cj0KCQjwo_PRBhDNARIsAEcVALXjwKWKAPWERNiOz14m6j-zMPEkgBBMNEwkOjFHlQz-XXjXZYS63UUaAuZjEALw_wcB) | robu |
| 10mm Spring (ID 5mm) | For the pen holder | 12 | 0.64 | [Link](https://onlyscrews.in/products/od-5mm-free-length-10mm-wire-dia-0-6mm-compression-spring-stainless-steel-304?currency=INR&country=IN&variant=53625349472569&stkn=6e84ebfba1b8&srsltid=AfmBOoqVrDx-Ldc_88YfdV64YuVTOdw0OwTo3OMMpkCciI0Z875Eq3qS6Fo) | onlyscrews |
| M5 X 45mm Hard Dowel Pins | For the pulley | 20 | 1.91 | [Link](https://onlyscrews.in/products/m5-x-45mm-hard-dowel-pins-dia-5mm-length-45mm?currency=INR&country=IN&variant=53296496017721&stkn=6e84ebfba1b8&srsltid=AfmBOooYPuf1Y5UIvdnVcB3wyyT6I3BgBfi1eKfbfEw2ttHG9k4DVQr-oas) | onlyscrews |
| 12V 3A power supply | For Power | 1 | 5.59 | [Link](https://robu.in/product/standard-12v-3a-power-supply-with-5-5mm-dc-plug-desktop-type/?gad_source=1&gad_campaignid=17427802559&gbraid=0AAAAADvLFWeNFfLjYJ39W-nS_4sWbPF81&gclid=Cj0KCQjwo_PRBhDNARIsAEcVALWph3h6QE-cwOkwUVcm4mqgnm8YQdb00utAdDjYq9M4xZu9O6it-PYaAn41EALw_wcB) | robu |
| Pin sockets | For Connection | 2 | 0.23 | [Link](https://robu.in/product/2-54mm-1x40-pin-female-single-row-header-strip-pack-of-10/?gad_source=1&gad_campaignid=17427802703&gbraid=0AAAAADvLFWcDnSG1W03jzKTevOWL8dN2p&gclid=Cj0KCQjwo_PRBhDNARIsAEcVALX20xFlt0RmoXuB9i_yK7OUUR2WnBMqRG3gxyZI7rpIPSGggEMj21IaArfPEALw_wcB) | robu |
| JST wire connectors | For the connector | 4 | 1.48 | [Link](https://robu.in/product/jst-xh-2-54mm-4-pin-female-housing-connector/?gad_source=1&gad_campaignid=17427802703&gbraid=0AAAAADvLFWcDnSG1W03jzKTevOWL8dN2p&gclid=Cj0KCQjwo_PRBhDNARIsAEcVALUnnn0kQXRptaygshQrHQ4GrH1CIv3uZGoWrwIsDPDtzLKa8ZbZNrYaAharEALw_wcB) | robu |
| JST 4-pin connectors | For Connection | 12 | 1.65 | [Link](https://robu.in/product/4-pin-jst-xh-2-54mm-pitch-plug-and-socket-with-cable-5-pcs/?gad_source=1&gad_campaignid=17427802703&gbraid=0AAAAADvLFWcDnSG1W03jzKTevOWL8dN2p&gclid=Cj0KCQjwo_PRBhDNARIsAEcVALV4Xu0R33MjW3TKi27UxTtMEh1mtRsRt6O31JcNEVRwyYGgDxC2bvwaAgyDEALw_wcB) | robu |
| JST 3-pin connectors | For the Connection | 12 | 1.52 | [Link](https://robu.in/product/3-pin-jst-xh-2-54mm-pitch-plug-and-socket-with-cable-10-pcs/?gad_source=1&gad_campaignid=17427802703&gbraid=0AAAAADvLFWcDnSG1W03jzKTevOWL8dN2p&gclid=Cj0KCQjwo_PRBhDNARIsAEcVALU-dsrENM3SdUrZCwZBL3aZIpX9c0CSFuw2bAay0t50bo2HKV8WC-kaAuSFEALw_wcB) | robu |
| Endstop Switch | For the limit end | 6 | 2.99 | [Link](https://robu.in/product/cnc-3d-printer-mech-endstop-switch/?gad_source=1&gad_campaignid=20387462343&gbraid=0AAAAADvLFWfUAYtwwMgGkSrCg8TecyWiB&gclid=Cj0KCQjwo_PRBhDNARIsAEcVALUVEq41N6LTqOY71-i7_OoxQ-DZz-_zx7lWjRimkFltpGfYirkDhusaAn3wEALw_wcB) | robu |
| A4988 driver Stepper Motor Driver | For the CNC Shield | 3 | 3.97 | [Link](https://robu.in/product/a4988-driver-stepper-motor-driver/?gad_source=1&gad_campaignid=20381096599&gbraid=0AAAAADvLFWekgUWdD-yQKIKT9ar2w3e5v&gclid=Cj0KCQjwo_PRBhDNARIsAEcVALXFLRpgExZwVO6s8_gYb_4l5NbCSciVEsRpVqOt-dY6pDRS95jUgwAaAlgnEALw_wcB) | robu |
| GT2 5mm Bore Aluminum Pulley Without Teeth | For the belt to move | 8 | 6.12 | [Link](https://www.flyrobo.in/gt2-5mm-bore-aluminum-pulley-without-20-teeth-for-6mm-belt?tracking=ads&tracking=4a9a9a&gad_source=1&gad_campaignid=17426303996&gbraid=0AAAAAC6AkE_NECiWtmL3gzgQd0fCbk3-i&gclid=Cj0KCQjwo_PRBhDNARIsAEcVALWtWxK-a4f3lJ1uvLOhbUf1l0i_MyVL6cz27qdDOn1AG1Hd2MrKTOIaAipLEALw_wcB) | flyrobo |
| GT2 Pulley 20 Teeth 5mm for 6mm | For drive the belt | 4 | 1.08 | [Link](https://robu.in/product/gt2-6mm-belt-width-20-teeth-5mm-bore-timing-pulley/?gad_source=1&gad_campaignid=20387462343&gbraid=0AAAAADvLFWfUAYtwwMgGkSrCg8TecyWiB&gclid=Cj0KCQjwo_PRBhDNARIsAEcVALXdWwLET5uyaohu0XNnp_Y0dAzfNmrIErzMyo2Ps2MA2Qm8VsP0euEaAr56EALw_wcB) | robu |
| SG90 Servo Motor | For the Pen Movement | 1 | 1.55 | [Link](https://robu.in/product/towerpro-sg90-9gm-1-2kg-180-degree-rotation-servo-motor-good-quality/?gad_source=1&gad_campaignid=20381096599&gbraid=0AAAAADvLFWekgUWdD-yQKIKT9ar2w3e5v&gclid=Cj0KCQjwo_PRBhDNARIsAEcVALUAwgs-BqwCSTB2tglRx1_5u7uQHVODmnASf51Fq6CcfjZDI1z5pcMaArlFEALw_wcB) | robu |
| CNC Shield V3 | CNC Control Boa | 1 | 1.60 | [Link](https://www.flyrobo.in/cnc-shield-v3-for-engraving-machine-3d-printer-a4988-drv8825-driver-expansion-board?tracking=ads&tracking=4a9a9a&gad_source=1&gad_campaignid=17426303996&gbraid=0AAAAAC6AkE_NECiWtmL3gzgQd0fCbk3-i&gclid=Cj0KCQjwo_PRBhDNARIsAEcVALXV9eErA8kUFejMuU87Y4kiCu4ZusP3GRvG_vjaQbks1Pe8SIi0RD4aAskkEALw_wcB) | flyrobo |
| Arduino Uno | The Main Board | 1 | 2.28 | [Link](https://robu.in/product/arduino-uno-r3-ch340g-atmega328p-devlopment-board/?gad_source=1&gad_campaignid=17413441824&gbraid=0AAAAADvLFWdfI1XB-KkKXV0RB4QUU0TIl&gclid=Cj0KCQjwo_PRBhDNARIsAEcVALUwC76VBNjlEC_UhJ4AEnzJoZIEqQEkTVERvXjqXoYtZt-cnzrkl68aAu-wEALw_wcB) | robu |
| GT2 Timing Belt 6mm | For Gantry System | 1 | 6.66 | [Link](https://robu.in/product/10m-gt2-width-6mm-white-open-timing-belt-for-3d-printer/?gad_source=1&gad_campaignid=20387462343&gbraid=0AAAAADvLFWfUAYtwwMgGkSrCg8TecyWiB&gclid=Cj0KCQjwo_PRBhDNARIsAEcVALW559IxzQVHFMmQXSUs8_ur-759EhIaRUzT6NXlhkmG7l5hYcAz2uoaAm_jEALw_wcB) | robu |
| V-Slot Idler Pulley | For Gantry System | 14 | 9.20 | [Link](https://www.flyrobo.in/openbuilds-plastic-wheel-idler-pulley?tracking=ads&tracking=4a9a9a&gad_source=1&gad_campaignid=17426303996&gbraid=0AAAAAC6AkE_NECiWtmL3gzgQd0fCbk3-i&gclid=Cj0KCQjwo_PRBhDNARIsAEcVALVZydW5oqzWb8p7Mpcs0WUBl-bKHlFv_qlc160ZvSgCLvOsrBOlTxsaAnJIEALw_wcB) | flyrobo |
| Nema 17 Bipolar Stepper Motor | The Main Motor | 3 | 40.90 | [Link](https://robu.in/product/fulling-fl42sth38-1684a-nema-17-stepper-motor/) | robu |
| 2020 Aluminium Extrusion | For the Frame | 5 | 37.09 | [Link](https://robu.in/product/easymech-20x20-t-slot-aluminium-extrusion-profile-1500-mm/?gad_source=1&gad_campaignid=17416544847&gbraid=0AAAAADvLFWeV6_fecEXW7yD2KwMGyNReC&gclid=Cj0KCQjwo_PRBhDNARIsAEcVALW-4mr0xMai9GUFMWCMWb8fglqwupc6Pt-b0wQmlohO40K5rTqcSpEaAnUyEALw_wcB) | robu |

<div align="center">
  <table border="0" cellpadding="0" cellspacing="0" style="border-collapse: collapse; max-width: 600px;">
    <tr>
      <td style="background: #ffffff; border: 1px solid #d0d7de; border-radius: 12px; padding: 20px; box-shadow: 0 4px 12px rgba(0,0,0,0.05); font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Helvetica, Arial, sans-serif;">
        <div style="font-size: 16px; font-weight: 600; color: #24292f; margin-bottom: 12px; border-bottom: 1px solid #d0d7de; padding-bottom: 8px;">
          Final Bill
        </div>
        <table width="100%" border="0" style="border-collapse: collapse; font-size: 14px; color: #57606a;">
          <tr>
            <td style="padding: 4px 0;">Component Subtotal:</td>
            <td align="right" style="font-weight: 500; color: #24292f;">$160.22</td>
          </tr>
          <tr>
            <td style="padding: 4px 0;"> Shipping:</td>
            <td align="right" style="font-weight: 500; color: #24292f;">$4.2</td>
          </tr>
          <tr>
            <td style="padding: 4px 0; padding-bottom: 8px;"> Tax:</td>
            <td align="right" style="font-weight: 500; color: #24292f;">$5.1</td>
          </tr>
          <tr style="border-top: 1px dashed #d0d7de;">
            <td style="padding: 12px 0 0 0; font-weight: 600; color: #24292f; font-size: 15px;">Net Total Cost:</td>
            <td align="right" style="padding: 12px 0 0 0; font-weight: bold; color: #2da44e; font-size: 18px;">$169.52</td>
          </tr>
          <tr>
            <td style="padding: 2px 0 0 0; font-size: 11px; color: #8c959f;">Projected Budget Allocation:</td>
            <td align="right" style="padding: 2px 0 0 0; font-weight: 500; font-size: 12px; color: #8c959f;">$170</td>
          </tr>
        </table>
      </td>
    </tr>
  </table>
</div>

**Project Under Hack Club**
