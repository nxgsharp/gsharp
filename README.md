# gsharp
G#


# Under construction #


## Content: ##
### Folder "Simple project to convert" ###
Contains a simple G# project and G#Object prepared for conversion to NXG.
Search for bookmark #ToDo to see where code has been altered to be prepared for conversion to G# as much as possible. 
A VI has been creatred as placeholder for missing NXG functions "G#Object_NXGNotImplemented".
A few helper VIs have been created in  the private folder to minimise conversion problems with flattened string being a byte array in NXG.

## List of major issues that must be addressed ##

#1 Conversion library. to be able to convert code using G# to NXG, G#Object (to start with) needs to be made into a NXG library and a conversion file needs to be created, which specifies how code using G# shall convert. This file specifies what VI will replace old VIs, how inputs will connect to (new or changed) inputs and outputs and such things.

#2 Classes can no longer be referenced by path. Instead, the fully qualified name is used. Code that depend on path to a class has to adapt so instead the fully qualified name is used. G#Object-methods that use path for classes and VIs must change. How can old code be converted? If old code cannot be converted automatically, how can we help in the manual conversion.

#3 Flatten to string is replaced with byte array. This causes some conversion issues, but code has been adapted as far as possible.

#4 G#Object is not in a lvlib. Conversion will put the code in "Loose files". The NXG G#Object has to be in a namespace (library). The conversion must redirect the code to link to the library.

## List of major issues that must be addressed ##
