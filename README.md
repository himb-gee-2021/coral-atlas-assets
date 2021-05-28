# Allen Coral Atlas assets
A trial for reading some [Allen Coral Atlas](https://allencoralatlas.org/) maps directly from Google Earth Engine Assets  

Contacts in case thigns are not working:  
  * [Mitchell Lyons](mitchell.lyons@gmail.com)  
  * [Rodney Borrego](rodbio2008@gmail.com)  

## Access group
The relevant assets are shared with the google group:  
himb-gee-2021@googlegroups.com

## Assets being trialled
Since the GEE assets are not production focused, there can be some changes in what product should actually be used (although this should be fairly minimal).  

### Current assets being shared:  
If you're using the Javascript API, then you can just run the script below. The advantage is that when we eventually modify/move the map assets, we can update the module paths and the assets should still load:  
https://github.com/himb-gee-2021/coral-atlas-assets/blob/main/aca_asset_grab  


### Hard coded paths
In case you need, the current paths to the actual asssets can be cross-references here:  
https://github.com/CoralMapping/gee-mapping-source/blob/master/global_reefs_modules/reef_params  

But for ease of use now, here's the current list as per above, the assets correspond like:  
  * segments: a multi-band stack, the band "depth" is what you want to select (please keep out of the other data as it probably is NOT licenced for use)  
  * geo_map_clean*: this is the current latest version of the geomorphic map  
  * benthic_map_clean*: this is the current latest version of the benthic map  

#### Hawaiian Islands
  * segments: "projects/coral_atlas/hawaii/in_out/hawaii_segmentation"  
  * geo_map_clean3: "projects/coral_atlas/hawaii/in_out/hawaii_geo_clean3"  
  * benthic_map_clean1: "projects/coral_atlas/hawaii/in_out/hawaii_benthic_clean1"  

#### Papua New Guinea & Solomon Islands  
  * segments: "projects/coral_atlas/png_solomons/in_out/pns_segmentation"  
  * geo_map_clean3: "projects/coral_atlas/png_solomons/in_out/pns_geo_clean3"  
  * benthic_map_clean2: "projects/coral_atlas/png_solomons/in_out/pns_benthic_clean2"  

#### Indonesian Archipelago  
  * segments: "projects/coral_atlas/Indonesia/in_out/indo_segmentation"  
  * geo_map_clean3: "projects/coral_atlas/Indonesia/in_out/indo_geo_clean3x"  
  * benthic_map_clean2: "projects/coral_atlas/Indonesia/in_out/indo_benthic_clean2"  

#### Great Barrier Reef and Torres Strait  
  * segments: "projects/coral_atlas/gbr_torres/in_out/gbrt_segmentation"  
  * geo_map_clean3: "projects/coral_atlas/gbr_torres/in_out/gbrt_geo_clean3"  
  * benthic_map_clean2: "projects/coral_atlas/gbr_torres/in_out/gbrt_benthic_clean2"  

#### Mesoamerican Reefs
  * segments: "projects/coral_atlas/mesoamerica/in_out/meso_segmentation"  
  * geo_map_clean3: "projects/coral_atlas/mesoamerica/in_out/meso_geo_clean3"  
  * benthic_map_clean2: "projects/coral_atlas/mesoamerica/in_out/meso_benthic_clean2"  


### Product/map details  
#### Bathymetry  
Derived from a composite of Sentinel-2, Landsat 8 and Planet Dove satallite imagery using an automated semi-empirical global approach [Li et al. 2021](https://doi.org/10.3390/rs13081469).  

The data itself is in integer format in depth in centimeters.

#### Geomorphic/benthic maps  
Mapped via a combined segmentation, machine learning, object-based approach in GEE [Lyons et al. 2020](https://doi.org/10.1002/rse2.157).  

The data iself is in integer format, and the class codes (and a colour scheme/palette) can be found here:  
https://github.com/CoralMapping/gee-mapping-source/blob/master/global_reefs_modules/colour_pals  

A complete explanation of all the classes - both in an ecologcal and remote sensing context can be found in [Kennedy et al. 2021](https://doi.org/10.1101/2020.09.10.292243)  

If you want to dig a bit deeper into the actual map production, then all of the source code for the mappign ocmponent of the ACA is here:  
https://github.com/CoralMapping/gee-mapping-source


