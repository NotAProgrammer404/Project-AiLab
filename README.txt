An adventurer in an Enchanted Forest will navigate through a mystical forest, avoiding dangerous obstacels, overcoming challenges and ultimately reaching the hidden treasure located in the southwest corner. 

Overview: 
The Enchanted forest is represented as an 8x8 grid, where each cell corresponds to a specific part of the forest. The grid contaians various elements:
0: Safegrid(60% chance)
-1: Obstacle(40% chance)
2: Start Node(northwest corner)
3: Goal Node(southwest corner)
5: Endpoints(walls)

Libraries Used: 
Numpy: Used for efficient array manipulation and grid representation.
Random: Utilized for generating random values and decisions within the forest generation process.

Generating the Forest: 
The 'gen_forest(size)' function generates the enchanted forest: 
1.Node Generation: Each cell in the grid is randomly assigned a node type (node_type) and a cost (cost). The node types include safe grids, obstacles, and endpoints, with corresponding costs.
2.Connecting Nodes: : Nodes are connected based on their positions in the grid, creating a grid-like structure.
3.Start and Goal Nodes: The start and goal nodes are assigned node types 2 and 3, respectively, with costs of 0 and 1.
4.Endpoints: Random endpoints are generated, acting as impenetrable barriers to restrict movement in certain directions.
5.Obstacles: Some safe grids may be replaced with obstacles, hindering the adventurer's progress.
6.Breaking Connections: Connections to neighboring nodes are severed for endpoints, simulating walls in the forest.


Priority Queue(PQ) Implementation
The PQ class represents a priority queue used in the UCS algorithm:
Push: Adds an item to the priority queue based on its priority (cost).
Pop: Removes and returns the item with the highest priority (lowest cost).
MT: Checks if the priority queue is empty.
Remove: Removes a specific node from the priority queue.

Uniform Cost Search(UCS)
The 'UCS(graph)' function implements the Uniform Cost Search algorithm to find the optimal path through the enchanted forest:
Initialization: The start and goal nodes are identified, and a priority queue (PQ) is initialized with the start node's cost.
Exploration: The algorithm iteratively explores the forest, considering the neighboring nodes of the current node. It prioritizes nodes with higher costs, allowing the adventurer to reach the goal efficiently.
Path Reconstruction: Upon reaching the goal node, the algorithm reconstructs the optimal path by tracing back through the parent nodes.



