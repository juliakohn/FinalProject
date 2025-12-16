<h1>Mapping and Analyzing Bicycle Fatalities in NYC</h1>
<p>
Julia Kohn | Command Line GIS Fall 2025 | Rutgers University | Dr. Will Payne
</p>
<p>
This series of maps analyzes bicycle fatalities in New York City and complexities that surround them. To create the below maps, the following datasets were used:
</p>
<p>
• <strong>Poverty Rate by Census Tract: </strong> This dataset was found through the United States Census data American Community Survey. I had to filter the ACS data to just show poverty rates. This data was from 2020. While there were no significant quality issues, I did show unreliable and missing data for this dataset in one of my static maps, and many tracts were deemed unreliable or were missing data. <br><br>
• <strong>Bike Priority Districts: </strong> This dataset was found on NYC OpenData, and was updated in 2025. The data was compiled and uploaded by the NYC Department of Transportation through their Vision Zero View Data system. The data was in CSV form. To make the layer more understandable, I dissolved the layer so that districts adjacent to one another just dissolved into one larger district. <br><br>
• <strong>NYC Bike Network Data: </strong> I created a bike network layer from OpenStreetMaps (OSMnx). This data is updated regularly by volunteers, and can be updated any minute. When creating this layer, I quickly realized that OSM does not categorize Staten Island as part of NYC, so I had to create a network for Staten Island separately and then combine it with the other NYC network after.<br><br>
• <strong>NYC Safe Routes to School Priority Schools: </strong> This dataset was found on NYC OpenData, and was updated in 2024. This data was compiled and uploaded by the NYC Department of Transportation. The data was in CSV form. I had no issues with this data. However, I did create a second layer from this to show priority schools overlapping with bike priority districts, which I did by clipping the data to the bike priority districts layer and coloring it differently from the main schools layer in my interactive map. <br><br>
• <strong>Motor Vehicle Collisions/Crashes (to get bicycle fatality data): </strong> This dataset was found on NYC OpenData, and was updated in 2024. This data was compiled and uploaded by the New York Police Department (NYPD). The data was in CSV form. However, this dataset is huge, with millions of rows...so, to make it easier to use, I filtered it on OpenData before downloading it to only download data with crashes involving a bicycle fatality.<br><br>
• <strong>Bike Fatality Network (bike routes nearest to a bike fatality): </strong> This dataset was created by performing a spatial join (sjoin.nearest) using the bike network from OSMnx and the cyclist fatality dataset. <br><br>
• <strong>NYC Arterial Vs. Non-Arterial Roads layer (roads within bike network): </strong> This dataset was created by categorizing the bike network layer (described above) by primary, secondary, or tertiary highways vs. all other roads (as categorized by OSM). This allowed me to show what kind of road my bike fatality network roads are located within.
</p>
<iframe src="interactivemap.html" height="905" width="102%"></iframe>
<img src="/FinalProject/bfn_withROADS.png" alt="NYC Bike Fatality Network Map" width="1000">
<img src="/FinalProject/bfn_arterial.png" alt="NYC Bike Fatality Network Map with Arterial vs Non-Arterial" width="1000">
<img src="/FinalProject/poverty_reliability_and_bike_network.png" alt="NYC Bike Fatality Network Map with Poverty Rates" width="1300">
<img src="/FinalProject/bikfatal_normpop (1).png" alt="NYC Bike Fatalities Normalized by Population" width="1000">
<img src="/FinalProject/bfn_locations.png" alt="NYC Bike Fatality Locations with Bike Priority Districts" width="1000">
