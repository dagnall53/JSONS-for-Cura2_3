# JSONS-for-Cura2_4- and 2.5 
Definitions for Cura2.4 (on) to add a dual extrusion "Flux capacitor" type delta 
 
 Save the extruders in /extruders
 Save the printer in /definitions
 
If you need to change the Gcodes , do so in a Json editor (I use notepad++) , as Cura does not have an inbuilt editor for Gcode and dual extruders. I would then advise checking with a Json checker.

The machine definition start GCode has a conventional "default_vaue" setting, but more importantly, it is immediately re-written by a "value" setting. You can probably get rid of the "default_value" setting, but I left it in. 
The "value" setting employs the "extruderValue" variable so that the Extruder start and sto codes can be used in the main machine start sequence. This avoids having to copy and paste the extruder G code into the Machine definition. In contrast to the "default_vaue", the "value" needs to have \\n for the line breaks, and text contained in ' single quotes. The advantage is that it then evaluates the variable "extrudervalue" and inserts the answer in the code.




