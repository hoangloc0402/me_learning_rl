### Me learning RL
This is just a repository for containing my experiments during learning Reinforcement Learning

#### 1) Fundamental concepts:
<ul>
  <li> <strong>State value func</strong>: V(s: State) -> expected future rewards </li>
  <li> <strong>State action value func</strong>: Q(s: State, a: Action) -> expected future rewards</li>
  
</ul>


#### 2) Dynamic programming techniques:
Model based: Need to know the transition matrix of the environment
Loop until the value function converges using Bellman Backup Operator
<ul>
  <li> <strong>Value Iteration</strong>: estimate Q(s, a), use argmax to get V(s), then derived the optimal policy fron the converged V(s)</li>
  <li> <strong>Policy Iteration</strong>: Randomly select a policy, find its V(s), then use V(s) to make an improvement to the old policy</li>
  
</ul>
