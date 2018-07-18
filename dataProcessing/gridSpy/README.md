# NZ GREEN Grid Data processing code
[NZ GREEN Grid](https://www.otago.ac.nz/centre-sustainability/research/energy/otago050285.html) data includes:

 * 1 minute electricity power (W) data for c 40 households in NZ monitored from early 2014 using [gridSpy](https://gridspy.com/) monitors on each power circuit (and the incoming power)
 * Occupant time-use diaries (focused on energy use)
 * Dwelling & appliance surveys

NB: *None* of the data is held in this repo so *none* of the code here will work unless you also have access to the data.

## 1 minute electricity power (W) data

The code here processes the original Grid Spy data files to produce a 'safe' form. To do this it:

 * checks the available files
 * skips files which do not contain data (grid spy files are empty .xml if no data is available for a given household)
 * imputes data and time formats
 * loads all data for a given household
 * cleans the data
 * saves the data for each household to 1 file
 * saves meta data on each file processed

The code maked extensive use of package functions. You will need to look at the [package function code](../../R/) to understand what has been done.

> Track outstanding [issues](https://github.com/dataknut/nzGREENGridDataR/labels/gridSpy).