### Floyd Warshall Algorithm<br>
([The Website](https://www.geeksforgeeks.org/floyd-warshall-algorithm-dp-16/))<br>
It is used to find the <mark>shortest path between vertexes<mark>.<br>

![Vertex and edges](https://upload.wikimedia.org/wikipedia/commons/b/b2/Floyd-Warshall-Algorithm-Problem.png)<br>

It used a *matrix* to keep track of the shortest distance between any two vertexes.<br>
If there is no connection between them, the cost in the matrix is infinity, otherwise will be the distance between two vertexes. **Floyd Warshall Algorithm** transverses each point and update each value in the matrix with the shortest distance to each other.<br>

Assuming have 3 vertexes<br>
|   | A | B | C |
|---|---|---|---|
| A | 0 | ∞ | 0 |
| B | 0 | 0 | 0 |
| C | ∞ | 0 | 0 |

The logic of Floyd Warshall Algorithm is to update each point by comparing distances from different pathes.<br>

`for (k = 0; k < V; k++) { //Pick one vertex as intermediate `<br>
`   for (i = 0; i < V; i++) { //Pick one as the start `<br>
`       for (j = 0; j < V; j++) { // Pick one as the end `<br>
`           if (dist[i][k] + dist[k][j] < dist[i][j]) `<br>
`               dist[i][j] = dist[i][k] + dist[k][j]; `<br>
`               //Check whether adding this intermediate make the path shorter `<br>
`        } `<br>
`   } `<br>
`}`<br>

>Yvonne Wu Sep.16 2022 Software Engineer


