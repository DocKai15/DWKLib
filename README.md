# DWKLib
This is a personal library for Altium symbols, footprints, templates and more. I'm still trying to figure out how to write these.
## Templates
### Schematic Templates
The schematic template is helpful because it will autofill the document information when you fill out the parameters. This can be added to Altium via the Preferences tab > Data Management > Templates > Add > Load from file
To use it, create a schematic document. In the properties tab, under "Page Options," select the template. Then, fill out the DrawnBy, Title, and Revision parameters in the Properties > Parameters tab.

## Schematic Library
The DWKLib.SchLib contains symbols that correspond to footprints in the PCB Library. Each symbol contains parameters for Value (part name), Manufacturer, and Manufacturer Part Number which are to be filled out manually. **If ordering assembly from JLC, include the LCSC Part Number.** Symbols like capacitors, resistors, transistors etc. can be reused by assigning multiple footprints to them. Other symbols, like digital ICs will likely need their own separate symbol.
### Adding a Symbol
If a symbol does not exist, it can be created easily. 
1. Make sure to pull the repository before making changes, because these libraries are in binary and conflicts cannot be resolved easily.
2. Add the symbol. Make sure to add the aforementioned parameters, and leave pins passive (avoids headache idk). If an IC does something that can be easily represented by symbols (i.e. AND gate) try to include those. I think it's nicer on the eyes than a bunch of empty yellow boxes. When assigning footprints, just add the footprint model (and not the pcb library) Altium will figure it out.
3. Commit and push in one breath. This way, if there is a conflict, there's less work to do to resolve it.

## Footprint Library
The DWKLib.PcbLib contains footprints and models. If adding a footprint, follow the same pull/push procedure as adding a symbol. Some tips:
- Dont use Ultra Librarian (NOT WORTH IT)
- The Altium IPC Compliant Footprint Wizard can be really helpful for making footprints based on the info in datasheets