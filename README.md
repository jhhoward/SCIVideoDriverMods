# SCI Video Driver Mods
This is a collection of modified video drivers for the Sierra SCI engine.

* CGACOMPO.DRV - A driver that uses the CGA composite mode to create additional colours via NTSC artifacting
* CGADITH.DRV - Another CGA composite driver that uses dithering to try simulate the colours of the EGA palette
* CGASCAN.DRV - As before but uses scanlines instead of dithering to simulate the EGA palette
* CGANEW.DRV - A 4 colour CGA driver that uses the alternate cyan/red palette. In a lot of cases it can give better results than the stock CGA driver.

## Usage
These drivers should work with any 16 colour SCI based game. e.g. Space Quest III and the EGA release of Space Quest IV

Drop into the game folder and edit RESOURCE.CFG to point to the new driver. For example:

`videoDrv=CGACOMPO.DRV`

If using with DOSBox then set your `machine` type to `cga` to emulate the CGA composite mode and the cyan/palette. If you don't do this, the composite modes will appear as 640x200 monochrome and the CGANEW.DRV will appear as cyan/magenta.

## Known issues
* When using with games that use a point & click interface, the mouse cursor hotspots are (sometimes incorrectly) at the top left of the cursor icon.
* For some games when using the composite drivers, thin text can be illegible.
