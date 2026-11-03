# CR-6 Touchscreen firmware for Marlin 2.1.x

## Do You Need This Firmware?

*If you have [a BTT SKR board with the BTT TFT](https://damsteen.nl/blog/2020/11/25/how-to-btt-skr-cr6-installation) you do not need this firmware.*

**Everyone else** needs this version of the CR6Community display firmware, to use their stock Creality CR6 TFT display with the Marlin 2.1.x software developed under Pull Request (PR)#19588.


## What Problem(s) Does This Firmware Solve?

In 2021, the CR6 community submitted PR#19588 to merge the cleaned-up CF6.1 UI and extended functionality upstream. The pull request stalled as Marlin evolved from 2.0.8.x to 2.1.x, a major update that fundamentally rewrote the extui API. Consequently, the original CF6.1 handlers and UI fell out of sync and were excluded from the Marlin 2.1.x branch.

In fall 2026, the Marlin core team (led by Thinkyhead) revived PR#19588. They have rewritten the extui, dgus, and Creality handlers to comply with the current API while preserving the established CF6.1 DWIN_SET interface. The team is now asking CR6 owners to flash the build, run hardware tests, and report on stability and feature parity.

This repository hosts the curated DWIN_SET firmware to facilitate those tests. If validation confirms Marlin 2.1.x fully supports the CF6.1 baseline, this release will simply mirror the official firmware on the CR6 Community GitHub. If testing surfaces issues requiring DWIN_SET adjustments, those fixes will be developed, discussed, and published here.

## Downloads

All CR6 printers using the stock TFT display will need to flash the exact same DWIN_SET to their display.
That firmware is available from the Source.zip file attached to the Latest Release on this site.

## Installing This Firmware to your Touchscreen
___________________________________________________________________________________________
**CAUTION: If you are using a MAC to prepare the SD card and to copy DWIN_SET to the card, 
PLEASE FIRST READ [THIS FAQ:](https://github.com/CR6Community/Marlin/wiki/Troubleshooting-Problems-with-Firmware-Flashing#my-screen-looks-like-this-picture-after-flashing-it)**
__________________________________________________________________________________________

  1. Download the Source.zip file from the latest Release's Assets list
  2. Extract the DWIN_SET folder and contents from that .zip file into a new blank directory
  3. Find and read ALL of the README files BEFORE attempting to flash your display (You'll be glad you did!)
  4. Figure-out which DGUS 2 is presently running on your display (it may help you later, to know what you started with)
  5. DO NOT FLASH ANY KERNEL FILES TO YOUR DISPLAY, unless:  
    5.1 You have inadvertently "bricked" your display by flashing the DGUS2 kernel upgrade files to a display calibrated for DGUS2 v4.5+  
    5.2 Your display is running version 1.x of DGUS2, and you want to fix the text kerning (in which case, add the DGUS2 v3.5 kernel file to your DWIN_SET.)
  6. Flash your display with the DWIN_SET folder 
  7. If anything went wrong, try the TROUBLESHOOTING.MD instructions
  8. Please provide feedback in Comments or Issues, as applicable

## Contributing

If you wish to contribute to the project, please provide your inputs by raising a new Issue or by commenting on an Open Issue on this repository, and/or by contributing to the discussion on the [CR6Community Discord #lcd-discussion channel](https://discord.gg/yDY6pb2BQS)

## Credits

[InsanityAutomation](https://github.com/InsanityAutomation/Marlin/tree/CrealityDwin2.0_Bleeding) initiated the refactoring project. It is upon that work that Thinkersbluff has built this Release.

[The core CR-6 Community firmware dev team](https://github.com/CR6Community/Marlin#credits) did the heavy-lifting that resulted in the CF6.1 baseline.

Icons from [Font Awesome](https://fontawesome.com/) and [Remix Icon](https://remixicon.com/).

Font from [Google Fonts](https://fonts.google.com/specimen/B612) and customized with [FontForge](https://fontforge.org/).
