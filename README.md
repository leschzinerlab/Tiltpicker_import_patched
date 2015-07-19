# Tiltpicker_import_patched

##Original code by Neil Voss: 
TiltPicker-2.0b13: http://emg.nysbc.org/redmine/projects/software/wiki/TiltPicker 

##Installation & setup
Make sure to look at the original document, which can be found in docs/INSTALL.txt and docs/USAGE.txt

##Changes: ApTiltPicker_import.py 
A patched ApTiltPicker.py that allows users to import particle coordinates and align them using the angle and tilt axis calculated with Tilt Picker.

The command line options are identical, except now the user can specify --picks1 and --picks2, which will be files containing the center coordinates (X and Y) of particles for the untilted and tilted micrographs. Example coordinate files can be found the data folder as data/picks1_import.spi and data/picks2_import.spi. 

##Example command

```ApTiltPicker_import.py -1 data/rawu049b.mrc -2 data/rawu048b.mrc --picks1=data/picks1_import.spi --picks2=data/picks2_import.spi --output=data/outputpicks_import.spi``` 

**To import particles: **
* Select 5 - 6 particles in both image that are the same
* Click 'Theta' button then 'Run' to calculate tilt angle
* Click 'Optimize' and then 'Run' (click run multiple times in a row) to calculate tilt axis properly.
* Click 'Import' to insert particles
* When finished, click 'Forward' and the aligned picks will be saved automatically into the specified output file

