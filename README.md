java c
GEOS2111/GEOS2911: HAZA RDS, CLI MATE CHANGE AND DISASTERS
NATURAL HAZARD MANAGEMENT: CASE STUDY FROM THE BIG ISLAND OF HAWAII
GEO S 2 1 11,  WEEK  6 - 8,  10
INTRODUCTIONThe Big Island of Hawaii is the largest island that makes up the Hawaiian Island Chain (Fig. 1). The Hawaiian Islands are a series of age-progressive volcanic islands (younging to the southeast) that were formed by the movement of the Pacific plate over a slowly moving mantle plume, a finger-like upwelling of hot, buoyant material coming from the core-mantle boundary. The Hawaiian Islands, and in particular, the Big Island of Hawaii, are therefore highly suspectable to the hazards posed by volcanoes.The Big Island of Hawaii, the southeasternmost island of the Hawaiian Island chain, hosts the only actively erupting volcanoes along the chain. The three active volcanoes on the island are Hualalai, Mauna Loa and Kilauea. Collectively, they cover the majority of the island and pose a significant threat to its environment, infrastructure and inhabitants. To view the summit of the Kilauea volcano to assess the current level of activity, click here:https://www.youtube.com/usgs/live

Fig. 1: The islands that make up the Hawaiian Island chain showing how they formed as the Pacific plate drifted over the Hawaii hotspot (mantle plume). The hotspot is currently located under the Big Island of Hawaii. Source: TASA Graphic Arts, Inc.The volcanic related hazards that affect the island include lava flows, ash falls, explosive eruptions and volcanic  induced  earthquakes.  However,  these  aren’t  the  only  hazards.  Others  exist  such  as tsunamis, bushfires/wildfires, floods and extreme storms that may be associated with the remnants of tropical cyclones.While the  Big  Island of  Hawaii is far  removed from Sydney, Australia, it provides a simple and contained area to assess hazards and their impact on different stakeholder groups as well as a comprehensive set of digital files that can be used for analysis. This will allow you to gain insights into the mapping and communication of hazards that can be taken forward to assess hazard risk in more complex areas and societies.
AIMS, LEARNING OUTCOMES AND MATERIALThe purpose of this practical is for you to design a series of hazard zone maps for the Big Island of Hawaii based on the hazards posed by the following hazards: lava flows, earthquakes, tsunamis, and wildfires/bushfires. Further, you will assess land use and demographic data to produce a vulnerability map of the Big Island of Hawaii and then combine that with the hazard maps to produce a hazard risk  map.   Lastly,  you  will  use  these  maps  to  communicate  hazard  and  hazard   risk  to  various stakeholders/interest groups.You will work on your hazard zone maps individually during Weeks 6-8 and will then work in a group in Week 10 to design a presentation targeted towards a particular stakeholder group based on one of the hazards you have explored.
As part of this practical, you will:
•    Examine different aspects of natural hazards that are known to impact the Big Island of Hawaii and their historical records.
•    Investigate how these data can be used to generate hazard risk maps.
•    Assuming the  role of a hazard specialist, use  both oral and written methods to communicate hazard risks to various stakeholder groups.
All the material you need for this practical is located on Canvas under Week 6. This practical will extend over 4 sessions (week 6-8,  10).
This  practical  is  modified  from:  Greene,  A.R.,  Garcia,  M.O.,  Becker,  N.,  and  Poland,  M.  Natural Hazards on the Island of Hawaii. https://serc.carleton.edu/hawaiian_volcanoes/74390.html
HAZARD SPECIALIST GROUPS FOR GROUP PRESENTATIONS
At the beginning of Week 6, you will be assigned to one of three hazardstakeholder groups:
•     Scientific community (hazard science specialists)
•    Government agency (Office of Planning and Sustainable Development)
•     Business group (tourism operators)Each group will need to prepare a presentation on one of the hazards and communicate the hazard risk  posed  by this hazard. The way to communicate this information will differ depending on the different groups so keep that in mind when designing your maps and presentation.
TIME MANAGEMENTThis worksheet contains material covering 4 practical sessions (8 hours). Combining all this material in one document has been done deliberately so that students can work at their own pace. However, to offer some guidance on where you should beat after each practical, see below:
• Week 6 – Part 1 and 2 (individual work)
• Week 7 – Part 3 and 4 (individual work)
• Week 8 – Part 5 and 6 (individual work)
• Week 10 – Part 7 (groupwork)
INDIVIDUAL GIS ASSIGNMENT (ASSIGNMENT 3)For Assignment  3  (Individual GIS assignment), you will need to incorporate some of the figures generated from this practical into your information flyer. It is therefore in your interest to complete all the work in the practicals and engage with the material. You are also encourage to extend yourself, particularly in Part 6, to produce maps for your flyer that will be most informative.
All details about Assignment 3 can be found on Canvas.
PART 1
SETTING  UP YOUR QG IS  PROJECTThe first step before you can assess any spatio-temporal data that can help you generate a hazard zone map for your speciality, is to set up a QGIS project with some base maps and data loaded for the Big Island of Hawaii.
TASK 1: DOWNLOADING AND DISPLAYING THE GENERAL DATA
Download the General.zip file from Canvas under Week 6. In that directory you will find 4 data files that have been downloaded for you.
- landsat_hawaii_15m – landsat (raster) image of Hawaii at 15 minute resolution
- HawaiiDEM_lowres.img – low resolution DEM (Digital Elevation Model) of Hawaii from the USGS
- coast_n83.shp – coastline of the Hawaiian Island Chain
- BigHawaii_coastline.shp – coastline of just the Big Island of Hawaii
- cntrs500_n83.shp – topographic contours every 500 feet (~150 m)
- Hawaii_volcanic_features.shp – includes the boundaries between the different volcanoes and rift zones.
- MainPlaces.shp – four population centres on Hawaii, for reference
•    Open a new QGIS project and save it somewhere in your folder structure where it won’t be automatically deleted.
•     Load all the data into your QGIS project (Fig. 2). Remember that one of these layers is raster data.
•    You should have a lot of experience with symbology. Use symbology to help visualize the data in the best possible way.

Fig. 2. Basemap and data for Hawaii as displayed in QGIS. Remember to use symbology to help visualise the data!
TASK 2 : PREPARING YOUR DIGITAL ELEVATION MODEL (DEM)
A Digital Elevation Model (or DEM) is a digital representation of terrain surfaces (elevation). We can use DEMs (Digital Elevation Models) to derive useful datasets like slope, azimuth and hillshade, for making cross-sections to show elevation changes across an area and as a general basemap to easily visualise areas of higher and lower elevation.
You have been provided with a low-resolution DEM of the Big Island of Hawaii as part of your general datasets (HawaiiDEM_lowres). It is a raster or gridded dataset. As this dataset has been created by the USGS, the elevation unit is feet. We want to change this to the metric system and will convert this to meters.
•     Go to the top menu and click on Raster – Raster Calculator.
•    Select your destination directory and save it as a file called HawaiiDEM_lowres and output format as a .img file. Choose whatever name you like but a good name might be HawaiiDEM_lowres_m
•    To convert from feet to meters type, in the Raster calculator Expression window type: “HawaiiDEM_lowres@1” * 0.3048
•    Click OK

Fig. 3. Set-up for the raster calculator expression window.
Do the usual thing of using symbology to display this data.
You won’t need the original DEM (HawaiiDEM_lowres) anymore so remove this layer.
TASK 3 : DOWNLOADING AND DISPLAYING THE LAND USE DATA
Download the LandUse.zip file from Canvas under Week 6. In that directory you will find 3 data files that have been downloaded for you from the Hawaiian Government portal.
- cty_zoning_haw.shp – Hawaii County Zoning as of April 2022
- ccd15.shp – 2015 Census County Divisions (aka Districts)
- geonames.shp – Hawaii Geographic Place Names
You may want to load these data into QGIS as they can tell you something about land use patterns and population centres which may help to inform. which communities and infrastructure are most at    risk of particular hazards.
• Load all the data into your QGIS project
•     For the cty_zoning_haw.shp, a new field called SIMPLEZONE has been created where the city zones have been reduced to 8 categories for simplicity. Use this field to colour the polygons by going to
Symbology, selecting Categorised, then selecting SIMPLEZONE as the Value and then clicking the Classify button (Fig. 3). Play around with the colours to display the fields in your preferred way.
•     Examine the different zone categories to get a sense of what type of industry, communities will be impacted by various hazards.

Fig. 4. Symbology window for the cty_zoning_haw.shp layer.
•     For the ccd15.shp, use symbology to display the polygons either by name (using the name field) or population (using the Pop15 field).
•    Click the information button to get a sense of the different names of the districts within Hawaii and   the populations for each district. This will help you get a sense where more people will be impacted by particular hazards.
•     Load the geonames.shp file to have a few reference population centres on your map as well as landscape features, such as calderas, valleys, lava flows, etc.
As this data will be useful once you generate your hazard map, you may want to untick these layers for now and only display them when you need to use them later in the practical.

Fig. 5. An example of the district and land use zone data layers displayed in QGIS.
PART 2
HAZARD SPECIALITY:  EARTHQUAKES
TASK 1: PREPARING AND DISPLAYING THE DATA
Download the Earthquakes.zi代 写GEOS2111/GEOS2911: HAZARDS, CLIMATE CHANGE AND DISASTERS
代做程序编程语言p file from Canvas under Week 6. In that directory you will find two data files that have been downloaded for you.
- Hawaii_historical_EQ.csv - downloaded from the USGS website and includes all earthquakes that occurred around the Island of Hawaii since records began of magnitude 3 and above
- Hawaii_significant_EQs_NOAA.csv – downloaded from the NOAA website and contains
information about all significant earthquakes that have impacted the Big Island of Hawaii since records began.
Now we want to load this data into QGIS and create a shapefile of these data so you can easily load them next time.
•     To load a .csv file, go to the top menu and click Layer – Add Layer - Add Delimited Text Layer
•     Under Filename, search for your .csv file. Ensure that File Format is CSV, that the X Field is
Longitude and the Y field is Latitude. Click Add and then click OK for the default projection. Close the window. Hint: Make sure that the projection is not listed as invalid!
• Right-click on the new layer (e.g. Hawaii_significant_EQs_NOAA) and click Export and Save
Features As. Under Format select ESRI Shapefile, under Filename select what you want to name the file and where, leave everything else as is but untick Add Saved File to Map at the bottom of the
window. Click OK. You will now have a saved shapefile of the data that can be easily loaded in next time as a vector data layer.
•     Repeat these steps for all the .csv files.
To make sense of the earthquake data, we usually want to display it such that it is coloured by the depth of the earthquake and sized by magnitude. Without a special plugin, this cannot be done
seamlessly. Instead, use symbology to plot as depth and separately as magnitude. You may want to load the layer in twice and apply different symbology for each so you can flip between layers.
Here is an example of how you can size by magnitude.
• Right-click the layer, click Properties and then go to Symbology
•     To size earthquakes by magnitude, select Single Symbol and then choose a colour that you like. Select Opacity to be 50%
•     Click the Data Defined Override button to the right of Size and then under Field Type select mag. Then click Edit and enter the following expression: 2 ^ "mag" / 10. This ensures that the symbols are  nicely scaled but feel free to play around with this scaling.
• Click OK to apply the symbology.

Fig. 6. Earthquakes scaled by magnitude.
Here is an example of how to colour by depth.
• Right-click the layer, click Properties and then go to Symbology
•    To colour earthquakes by depth, select Categorized and select depth as the Value.
•    Click the Classify button to generate categories based on depth.
•     Play around with the Colour Ramp field to adjust the colours that best represent the data. Don’t forget to click the Classify button anytime you change the colour ramp.
• Click OK to apply the symbology.
•     You can also use Graduated or Rules-based selections so that you can more easily see the separation between deeper and shallower earthquakes.
Create some maps that can be used in your group presentation and/or assignment.
TASK 2 : EXPLORE YOUR DATA AND ANSWER QUESTIONS
Now it is time to explore the historical and significant earthquake data as this can help guide the
creation of seismic hazard maps and to determine which areas are more vulnerable to the effects. Rather than prescribing what you should do, you should think about the types of information that
would be valuable for you as a hazard manager. You could consider recording this information in a table. For example, you may want to make a selection of all the >5.5 magnitude earthquakes and  use the statistics window to record the number, mean depth, depth range, maximum magnitude, etc.
The significant earthquake layer will tell you something about deaths, injuries and damages. Once you have explored your data, answer these guiding questions:
1.   Beneath which volcanoes do most earthquakes occur?
2.   What are the range of depths that the earthquakes occur and how does this compare to other earthquake prone areas?
3.   At what depth do the largest earthquakes occur?
4.   What do the different earthquake magnitudes generally mean in terms of the shaking and damage?
5.   What is a possible cause of earthquakes beneath Kīlauea Volcano?
6.   What could the cluster of offshore seismicity indicate?
TASK 3 : MAKE A PRELIMINARY HAZARD ZONE MAP
Based on the mapping of historical earthquakes and an understanding of the significant earthquakes that have occurred on the Big Island of Hawaii, you will create a very basic hazard map by generating an Earthquake Density Heatmap. Before you get QGIS to do this for you, think about what a hazard map for the main island may look like: e.g. where would you expect the highest and lowest seismic hazard? What is guiding your vision of the hazard zone map?
To generate an earthquake density heatmap where higher density areas will represent higher earthquake hazard and lower density representing lower hazard, do the following:
•     Go to the Processing menu and select Toolbox.
•     Under Interpolation, double-click the Heatmap (Kernel Density Estimation).
•     In the Heatmap window, select the Hawaii_historical_EQ layer as the input point layer.
•    Now you want to play around with the radius parameter to get the most appropriate density
estimation. This value represents the size of the search radius. Play around with this parameter, try 0.1 and 10 as end-members but explore some others in between to get a good estimation based on the data distribution you have.
•     Next, you want to set the resolution or output raster size. We will use a resolution of 1000 pixels x
1000 pixels for all our rasters (plug these values into the rows and columns section).
•    Next, you want to scaleby magnitude such that earthquakes with higher magnitude are given more weight. Under Advanced Parameters, select the mag field under Weight from Field. Select Output Scaling Value to be Scaled.
• Select where you want your output raster to be saved.
•     Click Run.
An earthquake density heat map will be displayed. However, it extends into the oceans as it included data from these regions. As we are only interested in generating a hazard map for land, let’s clip the raster to the coastline of Hawaii.
•     In the top menu, click on Raster – Extraction - Click Raster by Mask Layer.
•     The Input Layer is name of your heatmap raster, the Mask Layer is the BigHawaii_coastline.shp and then click Run.
• Rename the layer to be Earthquake Heatmap.
By default, the heatmap is coloured as greyscale. Play around with the symbology to improve the display. Remember that this is a raster data file. Some tips include:
•     Try Singleband Pseudocolour and Quantile for Mode with 5 classes.
• Test different colour ramps.
The density heatmap, with a weighting for magnitude, forms the basis of a very simple, preliminary earthquake hazard map (i.e. areas with the highest density and largest magnitude of events will correspond to the highest seismic hazard).
Instead of creating a new raster layer, you can use the legend to remap the heatmap values into a hazard rating.
•     Under Symbology, make sure you have 5 classes of values (you can set this if using Equal Internal for Mode. Under the label column, click on each value such that the lowest density is labelled as Very Low and the highest value as Very High. Use High, Moderate and Low for the values in between.
•    Create a map and makesure you adda legend.

Fig. 7. An example of how you can remap the heatmap to show hazard zone using the colours and legend.
You should now have a figure which shows earthquake hazard zones for Hawaii. This is a valuable tool for communicating hazard potential. Keep in mind that these hazard zones are relative to
Hawaii and not representative of a global hazard zone classification system.
If you wanted to create an accompanying raster dataset that will also represent seismic hazard, you can also do this. This will be important when you want to combine hazard ratings from different
hazards into the one map. To do this, we will reclassify our existing heatmap raster into 5 ratings:
•    1 = very
•    2 = low
•    3 = medium
• 4 = high
• 5 = very high
But how do we choose which ranges of values correspond with which rating? An easy way to get a range of values separated into 5 bands (to correspond to the 5 hazard ratings) is to make use of the symbology functionality.
•    Go to symbology of your heatmap and go to Singleband Pseudocolour and choose Quantile for Mode. Choose 5 classes and click Classify.
•     You should now see that values are assigned for each colour. These values give you a starting point     for assigning the values for each hazard rating. See Fig. 8 for an example of what these values might be (note: the values may be different for you because you may have chosen different parameters
along the way).
• Fill in the following table with the values for each rating:
Minimum
Maximum
Hazard rating


1


2


3


4


5

Fig. 8. The values assigned to each colour gives you a starting point for your classification.
•     Go to the Processing Toolbox and under Raster Analysis, click on the Reclassify by Table option.
•    Choose the appropriate heatmap as the raster layer and click on the 3 dots next to Reclassification table. Now click on Add Row and add the value ranges from your table above. Once you are happy, click Run.You should now have a raster called Reclassified raster that contains 5 different classifications.  Rename the raster into something useful, like Seismic Hazard Zones, and then use symbology to visualise it appropriately. This is your final seismic hazard zone map of the Big Island of Hawaii.
Questions to consider:
1.   What other factors should be considered to create a more comprehensive seismic hazard map of Hawaii?
2.   What would an adjusted Hawaii seismic hazard map look like?







         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
