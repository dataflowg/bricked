# Bricked
LEGO recreations of National Instruments hardware.

![Bricked](./title.jpg?raw=true "Bricked")

This repository contains build instructions, parts lists, LDraw models, and POV-Ray scenes of a selection of NI hardware.

## Quick Links
* cRIO-904x build instructions ([single page PDF](Instructions/cRIO-904x%204-slot/Bricked_cRIO-904x_4-slot.pdf), [printable booklet PDF](Instructions/cRIO-904x%204-slot/Bricked_cRIO-904x_4-slot_booklet.pdf), [parts list](Instructions/cRIO-904x%204-slot/README.md))
* PXI-1042 build instructions (coming soon)

*The booklet PDFs are to be printed on both sides of the page, then folded and stapled in the center to create a book. Consult your printer manual for duplexing instructions.*

## License
[![License: CC BY-NC-SA 4.0](https://licensebuttons.net/l/by-nc-sa/4.0/80x15.png)](https://creativecommons.org/licenses/by-nc-sa/4.0/)
All works are licensed under a Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License.

## Tools Used
[LEGO Digital Designer](https://www.lego.com/en-us/ldd) (Initial prototype models, can export to LDraw)
[LDraw](https://www.ldraw.org/help/getting-started.html) (all-in-one-installer includes LDView, LDCad, and POV-Ray)
[FreeCAD](https://www.freecadweb.org/) (for converting NI's CAD models to POV-Ray)
[Web Lic](http://bugeyedmonkeys.com/lic/) (for generating instructions)

## Installation
Install LDraw using the All-In-One installer, making sure to install LDraw, LDView, LDCad, POV-Ray, and the LGEO models for POV-Ray.

After install, open POV-Ray, then select Tools->Edit master POVRAY.ini. Add the following lines so POV-Ray can find the high quality LGEO models (not a typo).
```
Library_Path="C:\Users\Public\Documents\LDraw\LGEO"
Library_Path="C:\Users\Public\Documents\LDraw\LGEO\lg"
Library_Path="C:\Users\Public\Documents\LDraw\LGEO\ar"
```

## Workflow
The general workflow is listed below. You might also like to use LEGO Digital Designer rather than LDCad, as it's little easier to get started.

1. Create the model in LDCad (or LDD, and export to LDraw format)
2. Open the model in LDView
3. Export the model from LDView to POV-Ray, checking the LGEO option and setting the POV-Ray version to 3.7
4. Open the exported scene in POV-Ray and do a quick test render
5. Add extra settings like radiosity, hdr sky sphere, focal blur, area lights, etc

Generating build instructions is a little more effort. It involves breaking the model up into build steps (and sub-models) using LDCad, and then importing that into Web Lic. Web Lic does a pretty good job of the build instructions out of the box, but needs some manual work to create callouts for sub-assemblies, and custom page layouts.