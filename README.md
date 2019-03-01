### Very first github and python notebook


Are we safe? 

Task:
- Chose one dimension of this data-set of near-earth objects to estimate how safe we really are.  
- Try to make an inference about the total population of near-earth objects based on your measurements.
- Present your findings to each other, including your recommended actions based on your conclusions.

DEFINITION (Wikipedia)

Potentially hazardous asteroids (PHAs) are defined as having a minimum orbital intersection distance with Earth of less than 0.05 astronomical units (19.5 lunar distances) and an absolute magnitude of 22 or brighter. As of January 2018 there are 1,885 known PHAs (about 11% of the total near-Earth population), of which 157 are estimated to be larger than one kilometer in diameter (see list of largest PHAs below).Most of the discovered PHAs are Apollo asteroids (1,601) and fewer belong to the group of Aten asteroids (169).

SOLUTION 

Take the moid_au column and do a simple exploratory data analysis with a histogram. In this way we can observe how many objects cross the risk threshold. Later we will select those with moid_au<0.05 and h_mag >= 22.
The Poisson distribution may be useful to model events such as the number of meteorites greater than 1 meter diameter that strike Earth in a year.
