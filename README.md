The most unbiased way to produce linear extensions is probably "convex_hull".
This algorithm produces the n! ``hypercube duplication linear extensions". For N=[0,1,2,3], here are some: 

[]
[3]
[1]
[1, 3]
[0]
[0, 3]
[0, 1]
[0, 1, 3]
[2]
[2, 3]
[1, 2]
[1, 2, 3]
[0, 2]
[0, 2, 3]
[0, 1, 2]
[0, 1, 2, 3]

[]
[3]
[1]
[1, 3]
[2]
[2, 3]
[1, 2]
[1, 2, 3]
[0]
[0, 3]
[0, 1]
[0, 1, 3]
[0, 2]
[0, 2, 3]
[0, 1, 2]
[0, 1, 2, 3]

[]
[3]
[2]
[2, 3]
[0]
[0, 3]
[0, 2]
[0, 2, 3]
[1]
[1, 3]
[1, 2]
[1, 2, 3]
[0, 1]
[0, 1, 3]
[0, 1, 2]
[0, 1, 2, 3]

[]
[3]
[2]
[2, 3]
[1]
[1, 3]
[1, 2]
[1, 2, 3]
[0]
[0, 3]
[0, 2]
[0, 2, 3]
[0, 1]
[0, 1, 3]
[0, 1, 2]
[0, 1, 2, 3]

etc. 

Then, we produce a linear extension ``in the convex hull'' of these extremal (=hypercube duplication) linear extensions with the mean of a random walk between them, by capturing each time the first element that has not been yet added to the linear extension we are producing.
