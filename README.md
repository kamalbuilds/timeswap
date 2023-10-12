# BRB Hackathon
Your challenge is to design and implement Account Abstraction (AA) features for Timeswap Protocol, catering to the needs of Liquidity Providers (LPs) and facilitating the protocol's internal operations. For LPs, AA should offer enhanced gas efficiency, flexibility, and simplified token management, while for the protocol's internal use, a multi-sig AA wallet needs to be developed for efficient management of protocol assets (withdrawing protocol fees). The main objective of this problem statement is to ease the UX for LPs and for protocol’s us

## Technicalities
Most of the transactions in Timeswap V2 Protocol happens around these periphery smart contracts:
- LendGivenPrincipal
- BorrowGivenPrincipal
- CloseLendGivenPrincipal
- CloseBorrowGivenPrincipal
- AddLiquidityGivenPrincipal
- RemoveLiquidityGivenPosition
- Withdraw
- Collect

Let us go over a brief description of what these do:
### LendGivenPrincipal
This gives the ability to open lend positions in Timeswap V2 Protocol by supplying principal (or asset). This function is used if someone wants to
lend crypto asset into a certain liquidity pool. A liquidity pool is identified by the strike price, maturity, token0 asset and token1 asset.

### BorrowGivenPrincipal
Similar to previous one, this one let's someone submit their collateral and borrow against it. This function is used when someone wants to open borrow
positions while leveraging their asset.

### CloseLendGivenPrincipal
This function is used to close the lend positions one owns. This function can only be called before maturity of the pool

### CloseBorrowGivenPrincipal
This function is used to close the borrow positions one owns. This function can only be called before maturity of the pool

### AddLiquidityGivenPrincipal
This function is used by Liquidity Providers to add liquidity to a particular pool. This creates Liquidity positions

### RemoveLiquidityGivenPosition
This function is used by Liquidity Providers to close their liquidity positions after the pool has matured

### Collect
This function is used by Liquidity Providers to close their liquidity positions before the pool has matured

### Withdraw
This function is used by lenders to close their lending positions after maturity

## Addresses
All the addresses of each contract has been provided based on chain id and contract version. Feel free to let us know if you would need any other information for building the project for this hackathon. Good luck and build away!
