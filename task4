Task4a
#include<stdio.h>
const int MAX = 100;
void WarshallTransitiveClosure(int graph[MAX][MAX], int numVert);
int main(void)
{
    int i, j, numVert;
    int graph[MAX][MAX];
    printf("Warshall's Transitive Closure\n");
    printf("Enter the number of vertices : ");
    scanf("%d",&numVert);
    printf("Enter the adjacency matrix :-\n");
    for (i=0; i<numVert; i++)
        for (j=0; j<numVert; j++)
            scanf("%d",&graph[i][j]);
    WarshallTransitiveClosure(graph, numVert);
    printf("\nThe transitive closure for the given graph is :-\n");
    for (i=0; i<numVert; i++)
    {
        for (j=0; j<numVert; j++)
        {
            printf("%d\t",graph[i][j]);
        }
        printf("\n");
    }
    return 0;
}
void WarshallTransitiveClosure(int graph[MAX][MAX], int numVert)
{
    int i,j,k;
    for (k=0; k<numVert; k++)
    {
        for (i=0; i<numVert; i++)
        {
            for (j=0; j<numVert; j++)
            {
                if (graph[i][j] || (graph[i][k] && graph[k][j]))
                    graph[i][j] = 1;
            }
        }
    }
}

Task 4b

#include<stdio.h>
 #define V  4
#define INF 99999
 void printSolution(int dist[][V]);
void floydWarshell(int graph[][V])
{
    int dist[V][V], i, j, k;
 
    for (i = 0; i < V; i++)
        for (j = 0; j < V; j++)
            dist[i][j] = graph[i][j];
 
    for (k = 0; k < V; k++)
    {
        for (i = 0; i < V; i++)
        {
            for (j = 0; j < V; j++)
            {
                    if (dist[i][k] + dist[k][j] < dist[i][j])
                    dist[i][j] = dist[i][k] + dist[k][j];
            }
        }
    }
 
    printSolution(dist);
}
 void printSolution(int dist[][V])
{
    printf("Following matrix shows the shortest distances"
        " between every pair of vertices \n");
    int i, j;
    for (i = 0; i < V; i++)
    {
        for (j = 0; j < V; j++)
        {
            if (dist[i][j] == INF)
                printf("%7s", "INF");
            else
                printf("%7d", dist[i][j]);
        }
        printf("\n");
    }
}
 int main()
{
    int graph[V][V] = { { 0, 5, INF, 10 },
                        { INF, 0, 3, INF },
                        { INF, INF, 0, 1 },
                        { INF, INF, INF, 0 }
                      };
 
    // Print the solution
    floydWarshell(graph);
    return 0;
}
