floyd-warshall
==============

This README file outlines the Recursive code of the Floyd Warshall algorithm written by - 
	Nawal Saxena-sgnsaxen@liverpool.ac.uk


Contents
-----------
1. Introduction
2. Data structures used
3. Pseudocode



1. Introduction
---------------
The Floyd Warshall algorithm is used to find shortest paths between all pairs of vertices in a graph. It is a dynamic-programming algorithm; shortest path distances are calculated bottom up, these estimates are refined until the shortest path is obtained. Positive and zero weight cycles in the graph are ignored, and negative weight cycles can be detected. 
The algorithm runs in O(V^3) time (Time complexity), where V is the number of vertices in the graph.



2. Data structures used
-----------------------
1. Python - adjacency and parent matrices stored using standard Python list


3. Pseudocode
-------------
Required Recursive code can be written as

Given an adjacency matrix W, Here W represents the weight Materices generated

FLOYD-WARSHALL( W ):
{
n = W.rows   Number of rows
D(0) = W
for k = 1 to n			When the value of k is 1, 2, 3.......n
	for i = 1 to n		When the value of i is 1, 2, 3, .....n
    	for j = 1 to n		When the value of j is 1, 2, 3,......n
let D(k) = = [ d[i][j]^(k-1 ] be a new n x n matrix
	
	d[i][j]^(k) = min(d[i][j]^(k-1), d[i][k]^(k-1) + d[k][j]^(k-1))

	return D(n)
}
