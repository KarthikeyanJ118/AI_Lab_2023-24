# Ex.No: 4   Implementation of Alpha Beta Pruning 
### DATE:  09/03/24                                                                          
### REGISTER NUMBER : 21222106018
### AIM: 
Write a Alpha beta pruning algorithm to find the optimal value of MAX Player from the given graph.
### Steps:
1. Start the program
2. Initially  assign MAX and MIN value as 1000 and -1000.
3.  Define the minimax function  using alpha beta pruning
4.  If maximum depth is reached then return the score value of leaf node. [depth taken as 3]
5.  In Max player turn, assign the alpha value by finding the maximum value by calling the minmax function recursively.
6.  In Min player turn, assign beta value by finding the minimum value by calling the minmax function recursively.
7.  Specify the score value of leaf nodes and Call the minimax function.
8.  Print the best value of Max player.
9.  Stop the program. 

### Program:
# Terminating condition. i.e
# leaf node is reached
if depth == 3:
    return values[nodeIndex]

if maximizingPlayer:
  
    best = MIN

    # Recur for left and right children
    for i in range(0, 2):
         
        val = minimax(depth + 1, nodeIndex * 2 + i,
                      False, values, alpha, beta)
        best = max(best, val)
        alpha = max(alpha, best)

        # Alpha Beta Pruning
        if beta <= alpha:
            break
      
    return best
  
else:
    best = MAX

    # Recur for left and
    # right children
    for i in range(0, 2):
      
        val = minimax(depth + 1, nodeIndex * 2 + i,
                        True, values, alpha, beta)
        best = min(best, val)
        beta = min(beta, best)

        # Alpha Beta Pruning
        if beta <= alpha:
            break
      
    return best










### Output:
![image](https://github.com/KarthikeyanJ118/AI_Lab_2023-24/assets/160995906/92376777-1c7f-4f74-9a05-462a74ed56c5)



### Result:
Thus the best score of max player was found using Alpha Beta Pruning.
