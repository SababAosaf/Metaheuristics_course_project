# Adaptive differential evolution for Generating Alternative Land-use Allocation for Mixed Use Areas

The project was modified the codes in https://gitlab.com/nusrat.sharmin/land_use_optimization

The codes of this project are given to two main folder. In one
folder(land use optimization − master DE) the codes of adaptive differential
evolution with results are give. We also used swarm optimization which is given
in another folder(land use optimization − master Latest Swarm).
10
All the codes are written in matlab. The following files are used for This
project
• calculate compatibility.m
• handle input.m
• land uses.m
• non dominated sorting.m
• replace chromosome.m
• utility f unctions.m
• calculate landprice.m
• evaluate objectives.m
• initialize population.m
• neighborhood excel columns.m
• nsgaii main.m
• compatibility excel f ields.m
• genetic operator.m
• landdata excel columns.m
• nondominated sorting constraint.m
• tournament selection.m
For both the swarm and Differential Evolution these the same code structure
is used. The file names are also same. The content of genetic operator.m and
nsgaii main.m are different as we only changed the genetic operator . And for
12
the new genetic operator some new variables were needed. There slight changes
in main function were needed.
The functionality of the matlab files are as such
1. calculate compatibility.m - function calculate compatibility of the file
the compatibility of each plot with respect to the neighboring plots’ land use.
Values from compatibility index sheet of input data.xlsx are used.
2. handle input.m - function handle input defined in this file, is used to
load the data in all the sheets of input data.xlsx into data structures.
3. land uses.m - Contains class land uses with the values residential = 1,
commercial = 2, office = 3 and mixed = 8.
4. non dominated sorting.m - contains non dominated sorting function
which applies the Non dominated sorting algorithm on the initial population.
5. replace chromosome.m - This file consists a function replace chromosome
that replaces the chromosomes based on rank and crowding distance.
6. utility f unctions.m - This file has the definition of utility f unctions
class which implements the utility functions.
7. calculate land price.m - This file implements calculate land price method
that calculates the land prices of all the plots.
8. evaluate objectives.m - This file consists of evaluate objectives function
that calls calculate land price and calculate compatibility.
9. initialize population.m - This file implements initialize population func-
tion to generate the initial population for the whole process.
10. neighborhood excel columns.m - This file defines a class neighborhood excel columns
with the values plot id equal to 1 and neighbors equal to 2.
11. nsgaii main.m - This file is the entry point.
12. compatibility excel f ields.m - This file defines a class compatibility excel f ields
with the values residential equal to 1, commercial equal to 2, office equal to 3,
school college equal to 4, university equal to 5, health equal to 6 and civic equal
to 7.
13. genetic operator.m - The function genetic operator(parent chromosome,
V, mu, mum, l limit, u limit, percentage change allowed, minimum total ef f ective land price,
13
maximum total ef f ective land price, genetic operators change allowed) in this
file is utilized to produce offsprings from parent chromosomes for DE and only
mutate for Swarm.
14. land data excel columns.m - This file defines a class land data excel columns
that maps the excel column values of total land data sheet in the input data.xlsx
file to readable names.
15. non dominated sorting constraint.m - This file consists of non dominated sorting constraint
function which applies the Non dominated sorting algorithm on the population
of each iteration of NSGA-II algorithm and returns the population that satisfy
the given constraints, such as the percentage of change allowed on the map,
minimum total effective land price and maximum total effective land price.
16 .tournament selection.m - This file implements a function tournament selection(pool size,
tour size) which is the selection policy for selecting the individuals for the mat-
ing pool. The selection is based on tournament selection

