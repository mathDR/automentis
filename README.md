# automentis
Collection of ideas and code for automated self learning embodied robot

Ideas:
1.  Add multioutput kernel to jax-mc-pilco.
2.  Look at using the open-loop RL (pontryagin) formulation for the mean GP as the initial condition for the rollout optimiation.
  * The idea:  solve the optimization for $u_t$ like in the open loop RL paper.
  * Use those $s_t, u_t$ pairs as a regression target for the controller parameters.
  * Use those controller parameters as the initial condition for the full rollout optimiation.
3. Store all data from the interaction with the env system.  But only add those data to the states that are not currently predicted by the model.
4. Augment the GP model to a fully sparse variational GP formulation using the dual formulation for optimization of hyperparameters.