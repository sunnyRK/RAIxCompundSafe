# RAI X Compound Challenge (Gitcoin GR9)

## Challenge

For this challenge, you’re invited to build an insurance solution where Safe owners can deposit ETH on Compound and keep the received cETH in a saviour contract. When a Safe gets liquidated, the saviour should redeem ETH from compound and add it in the Safe.

## Solution

I have used code of the Refelexr geb-safe-saviours.
you can check my code submission in [src/saviours/CompoundSafeSaviour.sol](https://github.com/sunnyRK/RAIxCompundSafe/blob/master/src/saviours/CompoundSafeSaviour.sol).

I have create a Compound Safe Saviour contract. Where user can deposit ETH on Compound and keep recieved cETH on saviuor contract. which will be Safe to gets liquidited.

[Here you can see CompoundSafeSaviour Implementation.](https://github.com/sunnyRK/RAIxCompundSafe/blob/master/src/saviours/CompoundSafeSaviour.sol)

## Implementation Methods

`deposit: ` where user come with its safeID and ETH. deposit eth into compound and get cETH and keeps it in Saviour Contract.

`witdraw: ` Where user come with its safeID and colleteral token amount. and function transfer cETH into ETH and tranfer to user as per collateral token amout.

`saveSAFE: ` It will be called by liquidation engine. If somepoint your collateral position down then liquidation engine will call saveSafe method and takes ETH from saviour contract and add into SAFE contract to save your position.

## Kovan Deployed Contract Address

For Compound Saviour
https://kovan.etherscan.io/address/0x4fdedb857bc7d621994ec69053a13ed2ba8f64d2#code