# Description

## main.edp
Run the simualtion on the full structure and save the mesh, the deplacement field and the deformed mesh for visualization in Paraview.

Use to run single experiment.

## search.edp
Run the dichotomic search for optimal width. Save iteration results to "search.log" file.

## symmetric_case.edp
Similar to the "main.edp" script but use the symmetric property of the problem to run the simulation only on the left half of the problem.

## utils.edp
Collection of utility function to generate the mesh (full and symmetric structure) and to compute the deformation simulation.

# Experiments
## Meshsize h
methode adaptmesh uniforme avec hmin = hmax = h. e = 0.1.

| h    | uz(0, 0, 0) |
|------|-------------|
| 0.5  | -0.470      |
| 0.25 | -0.482078   |
| 0.1  | -0.495276   |
| 0.05 | -0.494969   |


## Graphical Exploration
We want to find the optimal (the smallest) 'e' that guarantees Uz(0, 0, 0) <= zo=0.1.
Bound e [0.001, 0.349];

| e   | uz(0, 0, 0) | 
|-----|-------------|
|0.05 |-4.06        |
|0.075|-1.185       |
|0.1  |-0.49        |
|0.2  |-0.06        |

## Dichotomic Search
| Iteration | a        | b        | e        | uz(0, 0, 0) |
|-----------|----------|----------|----------|-------------|
| 1         | 0.001    | 0.349    | 0.175    | -0.0922329   |
| 2         | 0.001    | 0.175    | 0.088    | -0.729313    |
| 3         | 0.088    | 0.175    | 0.1315   | -0.216698    |
| 4         | 0.1315   | 0.175    | 0.15325  | -0.137042    |
| 5         | 0.15325  | 0.175    | 0.164125 | -0.111578    |
| 6         | 0.164125 | 0.175    | 0.169563 | -0.101283    |
| 7         | 0.169563 | 0.175    | 0.172281 | -0.0966151   |
| 8         | 0.169563 | 0.172281 | 0.170922 | -0.0989118   |
| 9         | 0.169563 | 0.170922 | 0.170242 | -0.100082    |
| 10        | 0.170242 | 0.170922 | 0.170582 | -0.0994905   |
| 11        | 0.170242 | 0.170582 | 0.170412 | -0.099785    |
| 12        | 0.170242 | 0.170412 | 0.170327 | -0.0999336   |

# cas Symmetric
| e       |uz(0, 0, 0)| 
|---------|-----------|
|0.170327 |-0.0999877 |

