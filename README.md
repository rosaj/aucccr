# AUCCCR
Python implementation of the clustering algorithm proposed in the paper [AUCCCR: Agent Utility Centered Clustering for Cooperation Recommendation](https://www.hal.inserm.fr/INRIA/hal-03181696v1).

The AUCCCR groups data points into a unknown number of clusters (compred to KMeans with predetermined number of clusters).

AUCCCR can also have different types of calculating distances between data points, and the parameters are:

```
:param testr: List of lists
 - list of data points to be clustered. Each data point may have more than one value characterizing it

:param d: distance between x and y
 - function that takes two parameters and returns the distance between them, e.g., euclidean distance

:param n: distance between data point and the group's barycenter (as measured by a distance function d)
 - function that takes one parameter and returns distance from group's barycenter, e.g. 1.0/(1.0+x)

:param v: the value of the group of size N
 - function that takes one parameter and returns a value of the group, e.g., sqrt(x)

:param conv: if True, algorithm will converge, otherwise it may get stuck
 - True/False

:param atom: agents are “atoms”, too small relatively to the whole system to have significant influence individually
 - True/False

:param prc: the number of (random) initial values to try
 - a number, e.g., 20

:param mmt: momentum effect - loop termination if no changes was made in mmt iterations
 - a number, e.g., 5
```
