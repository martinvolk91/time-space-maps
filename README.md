# Time Space maps

How would a world map look if the distances between points represented travel time instead of distance in space?
<br/>
This project aims to answer this exact question (on a smaller scale).

### Demo
Here you can see a demo I created: https://martinvolk91.github.io/time-space-maps/
<br/>
Try clicking on different stations to see the map change.
The blue circles show 10, 20, 30, and 40-minute travel borders.
<br/>

### Idea
The initial plan was to create a time-space map of the Vienna U-Bahn 
metro railway network.
<br/>

Wiener Linien (the company running the city railway) has an API that is 
open to the public, allowing you to retrieve departures and arrivals schedules.
<br/>

Travel data between all station pairs need to be retrieved since the time-space map 
is user-centric. This means that the map looks different depending on the
user's position.
<br/>

The next step is to calculate new coordinates. We want to preserve the orientation by
calculating the angle between the source station and the destination station (if 
there is a station to the north of our current position on the normal map, we want it
to be "north" on the time-space map as well). We can then calculate the new longitude 
and latitude using the angle and travel time.
<br/>

### Future
The current version of the map only deals with stations.<br/>
The next question is how would the railroads look if the same was applied
to them and not only the stations.
How would the map of the whole city look like
if we expanded it to roads as well?

### Resources
https://www.data.gv.at/katalog/dataset/wiener-linien-echtzeitdaten-via-datendrehscheibe-wien
