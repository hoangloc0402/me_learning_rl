### Me learning RL
This is just a repository for containing my experiments during learning Reinforcement Learning

#### 1) Fundamental concepts:
<ul>
  <li> <strong>State value func</strong>: V(s: State) -> expected future rewards </li>
  <li> <strong>State action value func</strong>: Q(s: State, a: Action) -> expected future rewards</li>
  
</ul>


#### 2) Model-based:
By using dynamic programming techniques and the Bellman Backup Operator, loop until the value function converges
<ul>
  <li> <strong>Value Iteration</strong>: estimate Q(s, a), use argmax to get V(s), then derived the optimal policy fron the converged V(s)</li>
  <li> <strong>Policy Iteration</strong>: Randomly select a policy, find its V(s), then use V(s) to make an improvement to the old policy</li>
  
</ul>

#### 2) Model-free:
<ul>
  <li> 
    <strong>Monte Carlo</strong>: interact with the env repeatedly to obtain series of [state, action, reward] (aka episodes), update V(s) adter sampling each episode. Require the env to be episodic.
    <ul> 
      <li>First visit: Unbiased estimator, high variance</li>
      <li>Every visit: Biased estimator, high variance</li>
    </ul>
  </li>
  <li> <strong>Temporal Difference</strong>: Immediately update estimate of V(s) after each [s, a, r, s']. Can also be used in non-episodic or infinite-horizon env. Some bias, lower variance</li>
</ul>
<br>
<ul>
  <li>SARSA</li>: for computing TD target, use Q[next_state, next_action] -> on-policy
  <li>Q learning</li>: for computing TD target, max(Q[next_state]) -> off-policy
</ul>
