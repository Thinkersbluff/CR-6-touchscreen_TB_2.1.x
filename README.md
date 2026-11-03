# CR-6 Touchscreen firmware for Marlin 2.1.x

## Do You Need This Firmware?

*If you have [a BTT SKR board with the BTT TFT](https://damsteen.nl/blog/2020/11/25/how-to-btt-skr-cr6-installation) you do not need this firmware.*

**Everyone else** needs this version of the CR6Community display firmware, to use their stock Creality CR6 TFT display with version 2.1.x of the Marlin 2.1.x software.


## What Problem(s) Does This Firmware Solve?

The firmware released on this site largely delivers the User Interface (UI) and the User eXperience (UX) for the CR6 printer owner/operators' interactions with the Marlin 2.1.x backend.

Version 6.1 of the CR6 Community Firmware (CF6.1) - first released in June 2021 - is a fork of Marlin 2.0.8.1.
The primary goal of the CR6 Community project - as stated in their repository summary - was, "cleaning-up the source code changes for the CR-6 so it can be merged upstream."
The devs on that project also set themselves the ambitious secondary goal, "We also want to extend the functionality to make it fully functional"

The CR6 Community devs' efforts to achieve those two goals concurrently resulted in a set of custom-designed "handler" modules, along with CR6-unique UI/UX features packed into the companion CF6.1 DWIN_SET firmware, exploiting the Marlin/lcd/extui interface, as it existed in Marlin 2.0.8.1.

The devs stabilized CF6.1, then raised PR#19588 with upstream Marlin, asking that the resulting CR6 UI and extui integration be merged back into the Marlin core distribution.

Unfortunately, PR#19588 did not result in re-integration of the CR6 Community Firmware, in 2021, and the architecture and functionality of Marlin did not remain "static" in the five years after that.

Marlin evolved from 2.0.8.x to 2.0.9.x to 2.1.x.

The extui integration API evolved at each new version.

In some cases, the custom handlers of the CR6 Community 6.1 release now rely on features and functions that no longer exist at Marlin 2.1.x and do not comply with the new extui API.  Undertandably, the CF6.1 UI also does not support features that are new since 2.0.8.1, so the secondary goal of the CF project would require additional work, now, to catch-up with the latest features.

In the fall of 2026, Thinkyhead and the Marlin 2.1.x design team have updated and re-engaged in PR#19588.
They have the extui/dgus/creality handlers, to align with the new extui API and to be compatible with the existing CF6.1 DWIN_SET baseline.

Now, they have invited CR6 printer owners to download and hardware-test that software, and to provide them with feedback as to whether it "works" on their printers.


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
