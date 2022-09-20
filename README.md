### Floyd Warshall Algorithm

([The Website](https://www.geeksforgeeks.org/floyd-warshall-algorithm-dp-16/))
It is used to find the **shortest path between vertexes**.

![Vertex and edges](https://upload.wikimedia.org/wikipedia/commons/b/b2/Floyd-Warshall-Algorithm-Problem.png)

It used a _matrix_ to keep track of the shortest distance between any two vertexes.
If there is no connection between them, the cost in the matrix is infinity, otherwise will be the distance between two vertexes. **Floyd Warshall Algorithm** transverses each point and update each value in the matrix with the shortest distance to each other.

Assuming have 3 vertexes
| | A | B | C |
|---|---|---|---|
| A | 0 | ∞ | 0 |
| B | 0 | 0 | 0 |
| C | ∞ | 0 | 0 |

The logic of Floyd Warshall Algorithm is to update each point by comparing distances from different pathes.

```javascript
for (k = 0; k < V; k++) {
  //Pick one vertex as intermediate
  for (i = 0; i < V; i++) {
    //Pick one as the start
    for (j = 0; j < V; j++) {
      // Pick one as the end
      if (dist[i][k] + dist[k][j] < dist[i][j])
        dist[i][j] = dist[i][k] + dist[k][j]
      //Check whether adding this intermediate make the path shorter
    }
  }
}
```

> Yvonne Wu Sep.16 2022 Software Engineer

## Comment

I would avoid using `HTML` code in Markdown where possible. For example, you use the `<mark>` and `<br>` HTML tags in this document. I have removed them. Stick to pure Markdown where possible. Consider using stars, e.g. `**s**` to bring emphasis to some text, and type the regular `Enter` key in your editor to create new lines.
