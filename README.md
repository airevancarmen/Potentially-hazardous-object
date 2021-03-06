### Very first github and python notebook


Are we safe? 

Task:
- Chose one dimension of this data-set of near-earth objects to estimate how safe we really are.  
- Try to make an inference about the total population of near-earth objects based on your measurements.
- Present your findings to each other, including your recommended actions based on your conclusions.

DEFINITION (Wikipedia)

Potentially hazardous asteroids (PHAs) are defined as having a minimum orbital intersection distance with Earth of less than 0.05 astronomical units (19.5 lunar distances) and an absolute magnitude of 22 or brighter. As of January 2018 there are 1,885 known PHAs (about 11% of the total near-Earth population), of which 157 are estimated to be larger than one kilometer in diameter (see list of largest PHAs below).Most of the discovered PHAs are Apollo asteroids (1,601) and fewer belong to the group of Aten asteroids (169).

VARIABLES 
Taken from https://data.nasa.gov/resource/2vr3-k9wn.json
"designation":"419880 (2011 AH37)",
"discovery_date":"2011-01-07T00:00:00.000",
"h_mag":"19.7", Absolute magnitude. Risk >= 22 
"i_deg":"9.65", Inclination degree. It is the angle between the orbital plane and the plane of reference, the Earth in this case.
"moid_au":"0.035", Minimum orbit intersection distance. Risk AU < 0.05 AU. 
"orbit_class":"Apollo",
"period_yr":"4.06",
"pha":"Y", phase.
"q_au_1":"0.84",
"q_au_2":"4.26"

SOLUTION 
Take the moid_au column and do a simple exploratory data analysis with a histogram. In this way we can observe how many objects cross the risk threshold. Later we will select those with moid_au<0.05 and h_mag >= 22.
The Poisson distribution may be useful to model events such as the number of meteorites greater than 1 meter diameter that strike Earth in a year.
