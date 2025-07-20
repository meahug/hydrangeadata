# [What the flowers around us say about the earth beneath our feet](https://meahug.github.io/hydrangea/)
## Hydrangeas as a litmus test of the earth's soil

[Read the hydrangea story here](https://meahug.github.io/hydrangea/)

I started this project as a small Datawrapper map exploring hand-collected data of something I noticed in my neighborhood: hydrangea colors and their corresponding pH. This ended up as a broader rabbithole exploration:  regional soil pH trends across the country, and the specific types of soil that exist in Brooklyn. I was also interested in historical geological events that may have caused these soil qualities to exist in the first place, like sediment deposits (or ice sheets!).

Ultimately, I wanted to build a narrative about the plants around us carrying visual information. This information has a lot to tell us about the local ecosystem of our neighborhoods, and what geological events in the past helped shape this local ecosystem.

## Project findings

Upon collecting hydrangea colors and plotting them to soil pH, I noticed a few patterns. Potted plants had a higher pH, most likely due to being hand-watered with tap water, where potted soil increases more quickly to match the pH of the tap water being used. Overall, my hydrangeas skewed blue-purple, which is somewhat of an East Coast phenomenon where the soil is more acidic (overall, hydrangea color reflect a lot of local soil variation, but could follow regional soil pH patterns). 

Zooming out to the regional USA level led to explorations of macro-scale conditions like climate and soil sediment that cause regional pH differences.

This led me to some curiosity about the soil type in my area of Brooklyn, 'till substratum'. Till substratum is attributed to glacial deposits and leans more acidic in pH. I did a deep dive on the Laurentide ice sheet's terminal moraine across Staten Island, Brooklyn and Queens, which lies along Prospect Place, Prospect Park, Greenwood Cemetary and other later-developed green spaces in this stretch of NYC. (There are more green spaces along the terminal moraine because large boulder and rock deposits mean that this land was left undeveloped much later than surrounding areas of the boroughs.) 

I can't conclusively attribute the ice sheet's terminal moraine to my area of Brooklyn's soil acidity, but I loved discovering this piece of history from 20,000 years ago and really wanted to include it in this story.


## Data collection & analysis

**Hand-collected hydrangea data:** I took photos of every hydrangea I encountered along Prospect Place and recorded their approx color, corresponding pH, and whether they were potted or not. I uploaded this data to geojson.io and then DataWrapper. I also exported to [hydrangeapoints.csv](https://github.com/meahug/hydrangeadata/blob/main/hydrangeapoints.csv) for use in [Jupyter notebooks](https://github.com/meahug/hydrangeadata/blob/main/hydrangea_analysis.ipynb) to take averages and means of subgroups. 

**USA soil pH map:** It was difficult to find a working file for [USA soil pH patterns but I eventually found a .tiff file of a soil pH dataset](https://scholarsphere.psu.edu/resources/ea4b6c45-9eba-4b89-aba6-ff7246880fb1) that I could import into QGIS and use a color ramp scale to depict pH at the national level. I matched the color ramp to the supposed hydrangea color that corresponds to the pH. This dataset was determined by spatial pattern recognition at a 100m scale using satellite data. I was hesitant to use a dataset that leveraged AI/spatial pattern recognition, but upon reading into the methodology of the dataset, I discovered the soil pH data had an accuracy of 87%, which I learned (from Jeremy's class) is a fairly good accuracy rating for AI classification datasets overall. I couched this dataset with the word "approximate" to account for this margin of error. I then brought the color ramp map into Illustrator for editing and added an approximate color ramp legend and a Brooklyn reference point.

**Ice sheet map:** I saw other articles referencing the New York State Museum for maps of the Laurentide ice sheet terminal moraine location in NYC. I found [maps outlining the terminal moraine here](https://www.nysm.nysed.gov/publications/map-chart-series). I did some messy georeferencing by outlining the terminal moraine in Illustrator, converting to SVG and overlaying on top of the nyc boros shapefile from an earlier QGIS exercise.

**Other bits of data:** 
- [Brooklyn soil survey](https://www.soilandwater.nyc/files/8935eaa76/rss_postermap_200dpi.pdf)
- [NYC Drinking Water 2024 Report](https://www.nyc.gov/assets/dep/downloads/pdf/water/drinking-water/drinking-water-supply-quality-report/2024-drinking-water-supply-quality-report.pdf)
- [Laurentide ice sheet in New York](https://cp.copernicus.org/articles/20/2167/2024/cp-20-2167-2024-assets.html)
- [Hydrangea pH and other pigment facts](https://www.americanscientist.org/article/curious-chemistry-guides-hydrangea-colors)

## New skills and approaches I learned through this project
Some new skills I learned included Datawrapper (for the initial map and basemap styling), scrollytelling using the provided template, flexbox css, geojson.io (for plotting hydrangea coordinates and attributes: color, corresponding pH and potted or not), QGIS (for manipulating the USA soil pH map using a color ramp and .tiff files, and for projecting the NYC boroughs using the correct projection in the terminal moraine/ice sheet map), jupyter notebook (for taking mean pHs of potted vs unpotted hydrangeas). Some other new approaches included Illustrator (which is not quite a new tool to me) for customizing QGIS/SVG maps - a new approach that Larry's tutorial was very helpful for, assessing found dataset spatial recognition AI accuracy rates, and attempting to build a concise narrative in a contained project + figuring out my journalistic tone (very new to me!).

## Things I'd like to try to do if I had more skills and time
- Veronica taught us about georeferencing the other day. I could've used georeferencing in QGIS for the terminal moraine & Laurentide ice sheet map - I did this by hand using illustrator to trace SVGs and comparing the New York State Museum pdf side by side with my NYC boroughs QGIS / shapefile map. It was annoying to do it this way!
- Crowdsourcing - Aaron had a very neat idea to allow other folks to track and submit the colors/pH of the hydrangeas around them through a collaborative MapBox survey and add them to a shared map. This would've been a cool citizen science opportunity - but not quite sure how to do this yet.
- ai2html for scrollytelling - looking forward to learning this