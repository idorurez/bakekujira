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
* support for 128x32 or 256x32 (256x32 wip)
* QMK

## Installation
1. clone qmk_firmware
2. `cd qmk_firmware/`
3. Grab the chibios submodules:
   `git submodule sync —recursive && git submodule update --init —recursive`
4. open up qmk msys
5. `qmk compile -kb bakekujira -km default`

## Notes
* `onigaku` repo (not included in this repo) has all symbols and footprints
* Sorry for not using Kanji, thought Kana had a better overall fit!

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

## Credits
* Drashna
* foostan
