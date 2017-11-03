# Algorithms - TSP(Nearest Neighbor)
In this project, you will attempt to solve the TSP using different algorithms, evaluating their theoretical and experimental complexities on real and random datasets

## Description
We define the TSP problem as follows: given the x-y coordinates of N points on a 2D plane (i.e. vertices), and a cost function c(u, v) defined for every pair of points (i.e. edge), find the shortest simple cycle that visits all N points. The cost function c(u,v) is defined as the Euclidean distance between points u and v. Please see the TSPLIB documentation (which is included with the project, and [here](http://comopt.ifi.uni-heidelberg.de/software/TSPLIB95/tsp95.pdf)) for details. 

This version of the TSP problem is metric: all edge costs are symmetric and satisfy the triangle inequality. For more details about types of TSP, please refer to the lectures slides.

## Data
You will run the algorithms you implement on real world datasets consisting of actual Pokestops in the Pokemon Go game. We have used data from several different cities and varied the instance sizes to vary the diffculty.

The first five lines include some information about the dataset. For example, the Atlanta.tsp file looks like this:
NAME: Atlanta
COMMENT: 20 locations in Atlanta DIMENSION: 20
EDGE WEIGHT TYPE: EUC 2D NODE COORD SECTION
1   33665568.000000 -84411070.000000 
2   33764940.000000 -84371819.000000
...
...
...
EOF

The remaining line are space delimited and contain the node ID, x value, and y value of each node in the dataset. The x and y values are given as latitude and longitude points that have been multiplied by 1e6. The file will end with a single line that only contains the string “EOF”. As the EDGE_WEIGHT_TYPE is always EUC_2D you should use Euclidean distance, as described in the TSPLIB documentation, as the cost function between points. It is important to read the TSPLIB documentation because the distance values you use should be rounded in the way that is given in that document.

## Evaluation
Comprehensive Table: Include a table with columns for each of your MVC algorithms as seen below. For all algorithms report the relative error with respect to the optimum solution quality provided to you in the MVC instance files. Relative error (RelErr) is computed as (Alg-OPT)/OPT . Round time and RelErr to two significant digits beyond the decimal. For local search algorithms, your results for each cell should be the average of some number (at least 10) of runs with different random seeds for that dataset. You will fill in average time (seconds) and average vertex cover size.
