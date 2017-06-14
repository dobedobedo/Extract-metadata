# Extract-metadata
Use exiftool to extract metadata of a photo series and save it to a Python dictionary
# Note
This script uses exiftool, see http://www.sno.phy.queensu.ca/~phil/exiftool/  
Add the exiftool executable to path or put it in the same folder.
# Usage

Add the following code in your python script:  
- **import Retrieve_Metadata**<br />
- **from Retrieve_Metadata import PathImage**<br />

- **Metadata = Retrieve_Metadata.RetrieveData(PathImage, 'Tags')**<br />

'Tags' are optional and must be separated by comma.  
  
For example,  
Metadata = Retrive_Metadata.RetrieveData(PathImage, 'GPSPosition', 'GPSAltitude') will get a dictionary like:  
{'IMG_170204_044007_0716_NIR.TIF': {'GPSAltitude': '39.2 m Above Sea Level',
  'GPSPosition': '24 deg 47\' 14.17" S, 152 deg 16\' 19.11" E'},  
 'IMG_170204_044007_0716_NIR2.TIF': {'GPSAltitude': '39.2 m Above Sea Level',
  'GPSPosition': '24 deg 47\' 14.17" S, 152 deg 16\' 19.11" E'}}  
  
Then you can use your own script to parse the data as you like.
