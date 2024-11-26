For the C2VSimFG version 2.0 update, we plan to implement the injection of brine waters back into geologic formations. Since some of these injections occur at shallow depths below the Mid_Tulare Claystone and Amnicola Claystone, brine-water injections were not included in C2VSimFG1.5. 

To proceed with this update, the required data must first be downloaded from the Department of Conservation/Oil and Gas Management website:

[Production and Injection Data](https://filerequest.conservation.ca.gov/?q=production_injection_data)
https://filerequest.conservation.ca.gov/?q=production_injection_data

The SQL files from the source need to be converted into CSV format. I have created a Jupyter Python notebook to facilitate this process. Each annual dataset contains three TABLES, and automation to iterate through all of them is not possible.

### Instructions:
1. **Unzip Each File**:
   - Unzip the downloaded files and locate the `.accdb` files.

2. **Run the Script**:
   - Use the provided notebook `injections_accdbfiles.ipynb` to process each `.accdb` file.
   - The script identifies and extracts the following files:
     - `1987CaliforniaOilandGasWellInjection`
     - `1987CaliforniaOilandGasWellProduction`
     - `1987CaliforniaOilandGasWells`

3. **Modify Input File**:
   - Change the input file in the script for each `.accdb` file.
   - Re-run the notebook for each year, from 1977 to 2020, or other relevant datasets.

This manual process ensures proper extraction and conversion of the required data for implementing the brine-water injections in C2VSimFG version 2.0.

For more information on GEOLOGY please visit this website:
https://webapps.usgs.gov/cogg/findings/mapping-aquifer-salinity-gradients-and-effects-of-oil-field-produced-water-disposal-using-geophysical-logs-elk-hills-buena-vista-and-coles-levee-oil-fields-san-joaquin-valley-california
Thanks to Michael J Stephens at USGS for sharing his codes and I modified his code somehow to run it:
and this paper:
https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0263477
