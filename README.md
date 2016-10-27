###Summary   
The goal of the project of data visualization was to acquant viewers with the ski opportunities in the State Salzburg, Austria to help them choose next ski destination easier.   
I've collected some key information about the ski resorts and put them on the map which should help perceive information about many different places smoothly. To estimate popularity of the ski resorts, the metric "number of nights tourists spent during the winter season 2015/2016". There are also such information as number of ski lifts, length of slopes and ski pass price.  
TOP 3 ski resorts in terms of nights spent are Salzburger Sportwelt, SaalbachHintergl. Leogang Fiberbr. and Zellam See - Kaprun. ~54% of all nights in ski resorts of State Salzburg tourists spend in these 3 areas. The probable reason is the longest slopes and the wide of choices.  
I've mentioned also that the correlation between number of nights spent and number of ski lifts are the largest among all the data availabe. I find it interesting to calculate the ratio of number of nights spent per 1 ski lift in the ski area and get the most popular resort - Obertauern - which reasonably smaller than TOP 3 resorts but attracts tourists to spend more nights per one lift than others. I guess this resort is less spreaded than others and offer diverse skiing experience.  
   
###Design   
To create the visualization such technologies as d3.js v.3 and TopoJSON were used.   
I've decided to use TopoJson because it gives more opportunities for merge map elements than GeoJSON.   
In the visualization 2 TopoJSON maps (Austria, counties - states and Austria, counties - local communities) were used.   
Statistical information about night spent by the tourists during the winter season 2015/2016 belongs to http://www.statistik.at/. Key information about ski areas was gathered from http://www.salzburgerland.com/.   
In the project I've used different visualization elements such as: maps, rectangles, donut chart, bullet chart, etc.   
   
###Feedback   
I've gotten the number of interesting feedbacks on the project. To group recommendations, viewers recommended to explain the metrices and graphics; change user experience (colors / scales); add more data; formalize outcomes; improve the code formatting. The text of all feedbacks are in the bottom of this document.  
What was implemented based on the feedbacks:
1. Outcomes were visualized.
2. Explanation of the data / charts were added to the tooltip under the question mark.
3. Zoom was added to remind the viewer where the ski area is on the map of the country.
4. Code formatting was improved according to https://github.com/felixge/node-style-guide#2-spaces-for-indentation. The indentation was unified and changed to two spaces; 80 characters per line; single quotes; lowerCamelCase for variables and function names.
What was not implemented:
1.  Additional data was not added. Great that viewers were interested to get more and more data to the visualization. As there are already data from disperate sources, and perfection is not the key goal of this project, no new information were added.  
2.  Legend switch to color the map based on different metrices. The same idea as in p.1
   
###Resources   
1.  https://bost.ocks.org/mike/   
2. http://bl.ocks.org/ilanman/9598445   
3. http://stackoverflow.com/   
4. http://www.salzburgerland.com/   
5. www.statistik.at/   


####Feedbacks  
This is a really cool visualization, thanks for sharing it! I didn't now anything about the ski industry in Austria. The ski areas are clear and it's fun and easy to access information about them. I really like how the ski area information is displayed. Here are some things to consider to make the information even more clear:

It seems like #of nights spent is a proxy for the popularity level of the region. What is this measuring exactly? Number of nights spent at hotels etc? It may be good to explain this to the reader.
The legend containing number of nights spent is a little difficult to see. It might be worth making it larger.
It's not clear to me what the km of slopes indicates. Is that the distance occupied by actual ski slopes?
It's also not clear to me what the color encoding on for slopes represents (red, black, blue) Is this difficulty level?

It'd be nice to see if I could find what the cheapest Sky resort is at, or even a way of visualizing how that makes a difference. This could be another variable rank of the Rating of the region, etc. Or even drawing from an API from a User feedback site.

—
map color:
I understand that you wanted to make Austria visible around the area (I assume to localize it well), but how it is currently is quite distracting.
The color orange is very intense - yet Austria's shape is only the frame for your actual visualization. I'd suggest to use a much more mellow color, or even better: only outlines.
Also: currently the very thick borders of the countries are confusing for me. If you'd make Austria not colored you could use only thin lines for that.

map size:
Again, considering that the focus of your visualization are the ski resorts, I would certainly make them be bigger! Currently they are only tiny areas and some of them are even difficult to distinguish or locate when hovering.
You could maybe have a starting screen showing Austria and then zoom to the ski resorts - or just have a small location map somewhere in the corner and have it zoomed right from the beginning.

gray areas:
What are these? I assume they are Bezirke in Salzburg - but as a user of your page this is not clear. You mention there are 18 ski areas and I went to count to figure out whether these gray ones are included.
They seem to be part of your visualization - the way they are presented at the moment - however they are actually not.
I would either not include the border lines and simply make it one gray section, or at least leave some explanation in the hover functionality.
But better for a great visualization is always: Leave out what you don't need!

hover & click:
It's currently not clear that clicking gives you additional information. I'd just include a prompt somewhere that explains that (e.g. in the hover option).
Also: once 1 area has been clicked, it seems I can't go back to just hovering and seeing the names?

stats:
The slopes doughnut chart is totally great I think :)
Gives a good overview of the difficulty of the slopes present, while the km count also allows you to relate it to other skiing areas!

I don't quite understand the ski pass prices chart. Why is half dark gray and half light gray? What is the middle bar, and what the black thingy? I assume it's got something to do with average prices, but I really can't be sure. I wouldn't know how to compare prices from these charts, so I think they need a different design or some more explanation.

—
Some things probably you could consider adding are legends. For example, as a non-skier myself, I don't know how to interpret the colors of the donut graph. Then it's also not very clear how to interpret the bullet graphs - what for example is the meaning of the target vertical line and of the grey colors in the body of the graph.

Also, I have the (subjective) feeling that making the borders between the map areas a dark color, instead of white, will increase the map contrast and will make it easier for reading.

— 
From the POV of practicality, at the moment it is quite hard to get an idea on what region has got the biggest length of slopes, or what region is most/less expensive etc. It would be good to add switches of legend which would switch it from number of days to cost of ski pass or length of slopes.
