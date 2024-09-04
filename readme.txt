QUICK
version 1.0
===========

Quick stands for "quasi cliques".
It is an efficient algorithm to find
maximal quasi-cliques from undirected graphs. The Quick algorithm uses
several effective pruning techniques based on the degree of the vertices to
prune unqualified vertices as early as possible, and these pruning techniques
can be integrated into existing algorithms to improve their performance
as well. Our experiment results show that Quick is orders of
magnitude faster than previous work on mining quasi-cliques.



1. Usage:

    quick graph_file  r  min_size max_size output_file

2. graph_file format: the graph file contains the adjacency lists of 
	   all the vertices in the graph. The vertex ids must start with 0 and 
           be consecutive integers. Each line corresponds to the adjacency list of
           an vertex. If a vertex is not adjacency to any other vertices, then the
	   corresponding line is empty. For example, given a graph G=(V, E), 
	   where V={0, 1, 2, 3} and E={(0, 1), (0, 3), (1, 3)}, then the 
           contents of the data file are: 
	   1 3
           0 3

	   0 1

3. Output_file format: Every quasi-clique occupies one line. The first number is 
	   the size of the quasi-clique, followed by the list of vertices. 

4. r: the minimum degree threshold
   min_size: the minimum size threshold
   max_size: the maximum size threshold



Credits:

The Quick program is developed by Guimei Liu. The project is supported in
part by a MOE Tier-1 grant "R-252-000-274-112: Graph-Based Protein Function 
Prediction" and a SERC PSF grant "SERC 072 101 0016 (R-252-000-316-305): 
Pattern Spaces: Theory, Techniques and Applications". 

If you use this software, please cite the following paper:

Guimei Liu, Limsoon Wong. Effective Pruning Techniques for Mining Quasi-Cliques. 
Proceedings of European Conference on Machine Learning and Principles and 
Practice of Knowledge Discovery in Databases (ECML PKDD), 
pages ???--???, Antwerp, Belgium, 15-19 September 2008. 


