# Moraydular Power Bus #

A compact (50x200mm) 12-way power distribution PCB for Eurorack modular synthesizers. 

Can be built as a simple passive bus board with shrouded or unshrouded headers, using standard .156" and/or flat connectors for power input and chaining. Optionally power indicator LEDs (highly recommended!) and onboard minimal +5V regulation from +12V rail may be added.

## Ordering and Building Notes ##

The .dip file contains the PCB design in DipTrace format. The Gerber files are confirmed to pass checks for Seeedstudio, 5x20cm 2-layer PCB. They will probably work fine as-is for Itead, Tinysine, Elecrow and other prototype PCB services. Consider spending extra for 2-3 oz traces and thick PCB.

Populating the PCB should be straightforward. Only thing to note is that the pads for all the connectors have quite wide thermal reliefs, so soldering them may require some extra heat and patience.

## Bill of Materials ##

For plain passive board:

 * **12x** 16-pin (2x8) 0.1" shrouded box header (eg. Reichelt WSL 16G) OR unshrouded pin strip
 * **6x** PCB-mount Faston / Abiko / flat connectors (eg. Reichelt FS-P 6,35)
 	* Alternative: **1x** 4-pin 0.156" PCB mount connector (MTA156, Molex KK .156)
 	* Or you can just solder the wires from PSU directly to the PCB
 * **3x** 3mm LEDs
 * **3x** Current limiting resistors according to LEDs you've chosen (2x 1K, 1x 220R as indicated on PCB silkscreen should be fine at least for normal red or green leds)

For +5V onboard regulation add the following:

 * **1x** 7805 voltage regulator
 	* Use a heatsink according to your planned current draw
 	* Pin-compatible DC-DCs such as OKI-78SR-5/1.5-W36-C should work and provide more current with better efficiency and no heatsink required, but currently untested
 * **2x** standard rectifier diodes, any of 1N4001...1N4007 will do
 * **1x** 10uF electrolytic capacitor, 16V or higher voltage rating
 * **1x** 100nF ceramic capacitor