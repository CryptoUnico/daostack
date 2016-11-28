
## Roadmap

# 0. Starting point

The Truffle Webpack Demo serves us as starting point:

* Token contract with an owner
* Contract launched with 10,000 ("Meta") tokens to owner
* The owner can distribute tokens to other addresses
* UI shows balances of addresses [1]
* Owner can send transaction through the UI

  [1] In the demo the addresses are opened through the testrpc; what's the alternative with a real chain? (and whether need to add anything to the demo then). Then, balances of which addresses will be shown in the UI? all non-zero balances? (in the demo there's a fixed set of balances shown also with zero balance); will any address that receives tokens will be added to the list? probably need to add a component there (UI and possibly also in connection to the blockchain).

  UPDATE: in the demo you can send tokens to a (valid) address that doesn't appear there;
  the UI shows the subtraction of tokens from the owner balance and doesn't add the new address to the accounts list. Which means we need to:

  1. Change the account list to be only of non-zero (>/epsilon) balance addresses
  2. Add the UI component that adds a new address to the list
  3. Perhaps order the list by size of balance (or add other options, by time of transaction, etc.)

# 1. add owner (UI)
# 2. add change owner
# 3. owner mine tokens (to himself) on the go
# 4. owner distribute tokens on the go (mine to himself + send)
# 5. add send from
# 6. add votePower (universal = 1)
# 7. votePower UI
# 8. change token distribution from owner to majority vote (owner is initial votePower)
# 9. vote on distribution (=1) votePower
# 10. general votePower and median vote
