# blockchain-developer-bootcamp-final-project

- Payment splitting for group buys of tokens/crowdsales (input token address for acceptable incoming (dai,usdc, usdt, etc), enter expected conversion (to weth, usdc, etc), set pool closed and dont allow more incoming, sweep pool to outgoing token (possibly only erc20s, not eth; pool has to be closed; individual contribution % gets set at this point
  - Could also set it up so that anyone contributing to the pool gets swapped right then and there and % of pool gets set then, but would be higher gas amount
  - Workflow would be like user creates pool and enables whitelisted tokens for incoming (from kleros token curated registry); Deploys contract; Users contribute funds from their accounts using UI, or transferring tokens directly (need to look at how to do it automatically); if enabled, this set sweeps immediately, else, pool it and record user info; close pool no more contributions; can also reopen pool; sweep pool converts all to single output, sets % for return, and perm closes pool (possibly add button to do both in single txn); Distribute function to allow token contract address to be entered (must have non zero balance in acc); This sends the % back to all the users
  - If only one whitelisted and it matches the output, then no need to swap and should allow 
  - Possibly make users extract their portion rather than auto send to save gas on the sender

