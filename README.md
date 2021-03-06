# bakekujira
![Image of schematic](images/bakekujira_schematic.png)
![Image of pcb](images/bakekujira_pcb.png)
![Image of pcb render](images/bakekujira_pcb_render.png)

## Features
* TKL, F-row less
* split 
* per-key RGB
* underglow
* Proton-C
* support for 128x32
* QMK

# BOM

Part | Part number | Number needed | Link
------------ | ------------- | ------------- | -------------
 Proton-C | n/a | 2 | https://mkultra.click/qmk-proton-c/ note: EXTREMELY LIMITED stock everywhere, most are gone
 Mill Max low profile Sockets | 315-47-164-41-001000 | X | n/a
 Mill Max pins Pins |  3320-0-00-15-00-00-03-0 | X |  n/a
 LEDs | SK6812MINI-E | 104 (or get as many as you can) | https://www.aliexpress.com/item/4000476037223.html?spm=a2g0s.9042311.0.0.27424c4dQxUpgR 
 TRRS Connectors | MJ-4PP-9 | 2 | https://www.aliexpress.com/item/32368285821.html?spm=a2g0s.9042311.0.0.27424c4dQxUpgR 
 Kailh hot swap sockets | n/a | minimum 74 | https://www.aliexpress.com/item/4001051840976.html?spm=a2g0s.9042311.0.0.27424c4dQxUpgR 
 Tactile Push button | 4x4x1.5mm 4pin SMD | 2 | https://www.aliexpress.com/item/1005001328036177.html?spm=a2g0s.9042311.0.0.27424c4d8ExoPG 
 0805 4.7K resistor | n/a | 2 | https://www.aliexpress.com/item/4000906183506.html?spm=a2g0s.9042311.0.0.27424c4d8ExoPG 
 0805 510R resistor | n/a | 2 | https://www.aliexpress.com/item/4000906183506.html?spm=a2g0s.9042311.0.0.27424c4d8ExoPG 
 0603 100nF (aka 0.1uF) ceramic capacitors | n/a | minimum 104 | https://www.aliexpress.com/item/4000193649637.html?spm=a2g0s.9042311.0.0.27424c4d8ExoPG 
 1N4148 diodes | n/a | minimum 74 | https://www.aliexpress.com/item/4000685043735.html?spm=a2g0s.9042311.0.0.27424c4d8ExoPG 
 
# Software

## Installation
1. clone my fork of qmk_firmware
2. `cd qmk_firmware/`
3. Grab the chibios submodules:
   `git submodule sync —recursive && git submodule update --init —recursive`
4. open up qmk msys
5. `qmk compile -kb bakekujira -km default -bl dfu-util-split-left` (do the right side also, you only have to do this once for each side)

## Notes
* `onigaku` repo (not included in this repo) has all symbols and footprints
* Sorry for not using Kanji, thought Kana had a better overall fit!
* The art design is temporary. I will be changing the mascot to something easier on the eyes.

# Suggestions
* Order more than you need of the diodes, caps, and leds, and kailh sockets. FYI, in most cases there is a MOQ
* The 01.uF capacitors aren't absolutely needed, but it will help with fluctuations and possibly prevent LEDs from burning out.

# Soldering Hints
* It's easier to use a wider/bigger tip in some cases.
* For the small solder pads, make sure you are tinning and using flux to ensure that the very tip of your soldering tip will hold a bead of solder.
* For the Kailh sockets, you can put solder on both pads first and then pushing down on the kailh socket while heating up the ends one at time.

# LEDs
* When soldering the underglow LEDs, bend the terminals/legs down so they touch the soldering pads.
* Solder the LEDs in the order that wired up and test as you go. Please see the diagram (ie solder the under glows first)
* If the LED looks broken or melted, it's probably broken.

## Inspiration
Picked apart a lot of boards, including:
* Corne
* Corne Waffle
* marevelous65 split
* ganymede

## TODO
* build case
* build plate
* working out breakout board for 256x32 (see other SSD1326 breakout repo)

## REV2
* move proton-c and plugs out instead of tucked in line with the top row to allow for more case options
* Add holes for M2x4 or M2x9 screws/standoffs to allow for more case options
* sound and speakers
* oled 256x32, which may end up here under rev1

## Credits
My QMK friends who have not openly judged me on being an idiot (except for xyz):
* Drashna
* foostan
* waffle
* tzarc
* xyz
