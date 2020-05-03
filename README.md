# HC-SA
Hill climbing and simulated annealing

###### Page 125 of Artificial Intelligence: A Modern Approach, Stuart Russell and Peter Norvig, 2010, 3rd Edition



The **hill climbing** search algorithm which is the most basic local search technique. 
At each step the current node is replaced by the best neighbor; 
in this version that means the neighbor with the highest <i>VALUE</i> but if a heuristic cost estimate 
<i>h</i> is used we would find the neighbor with the lowest <i>h</i>.
  

![Alt text](ss_1.png?raw=true "HC-Alg")


**Simulated annealing**

<a href="https://faculty.washington.edu/aragon/pubs/annealing-pt1.pdf"> Simulated annealing original research paper </a>

![Alt text](ss_3.png?raw=true "HC-Alg")


A hill-climbing algorithm that never makes "downhill" moves toward states with lower value (or higher cost) is guaranteed to be incomplete
, because it can get stuck on a local maximum. In contrast,
a purely random walk -- that is, moving to a successor chosen uniformly at random from the set of successors -- is complete but extremely inefficient.
Therefore, it seems reasonable to try to combine hill climbing with a random walk in some way that yiels both efficiency and completeness.

Iterative improvement consists of a search in this coordinate space for rearrangement steps which lead downhill. 
Since this search usually gets stuck in a local but not a global optimum, it is customary 
to carry out the process several times, starting from different randomly generated configurations, and save the
 best result.
 
 Random numbers uniformly distributed in the interval (0,l) are a convenient means of implementing the random part of the algorithm.
 
 Using the cost function in place of the energy and defining configurations by a set of parameters {xi}, it is straightforward with the Metropolis procedure 
 to generate a population of configurations of a given optimization problem at some effective temperature. 
 This temperature is simply a control parameter in the same units as the cost function. The simulated annealing process consists of first "melting" the system being optimized at a high effective temperature, then lowering the temperature by slow stages until the system "freezes" and no further changes occur.
 
 ![Alt text](ss_2.png?raw=true "HC-Alg")

 