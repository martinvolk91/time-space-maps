# Time Space maps

How would a world map look like if the distances between points were 
representing travel time instead of distance in space?
<br/>
This project aims to answer this exact question (on a smaller scale).

### Idea
The initial plan was to create a time space map of the Vienna U-Bahn 
metro railway network.
<br/>

Wienerlinien (the company running the city railway) has an API that is 
open to public which allows you to retrieve departures and arrivals schedule.
<br/>

Travel data between all station pairs needs to be retrieved since the time-space
map is user-centric. This means that the map looks different depending on the
user's position.
<br/>

Next step is to calculate new coordinates. We want to preserve the orientation by
calculating the angle between the source station and the destination station (if 
there is a station to the north of our current position on the normal map we want it
to be "north" on the time-space map as well). Using the angle and travel time 
we can then calculate the new longitude and latitude.
<br/>

### Resources
https://www.data.gv.at/katalog/dataset/wiener-linien-echtzeitdaten-via-datendrehscheibe-wien