# Ex.No: 3  Implementation of Minimax Search
### DATE:  24/02/24                                                                          
### REGISTER NUMBER : 212221060118
### AIM: 
Write a mini-max search algorithm to find the optimal value of MAX Player from the given graph.
### Algorithm:
1. Start the program
2. import the math package
3. Specify the score value of leaf nodes and find the depth of binary tree from leaf nodes.
4. Define the minimax function
5. If maximum depth is reached then get the score value of leaf node.
6. Max player find the maximum value by calling the minmax function recursively.
7. Min player find the minimum value by calling the minmax function recursively.
8. Call the minimax function  and print the optimum value of Max player.
9. Stop the program. 

### Program:

import math def minimax (curDepth, nodeIndex, maxTurn, scores,targetDepth): # base case : targetDepth reached if (curDepth == targetDepth): return scores[nodeIndex] if (maxTurn): return max(minimax(curDepth + 1, nodeIndex * 2,False, scores, targetDepth), minimax(curDepth + 1, nodeIndex * 2 + 1, False, scores, targetDepth))









### Output:

![image](https://github.com/KarthikeyanJ118/AI_Lab_2023-24/assets/160995906/6307c5d7-44bb-414a-b82c-fa0bd6f28325)


### Result:
Thus the optimum value of max player was found using minimax search.

