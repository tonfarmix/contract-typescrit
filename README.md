fTON
Farmix is decentralized, open-source Leveraged Yield Farming.

fTON consists of these components:
1. Contract: The smart contract code that is running on-chain. The code is available here on this repository.
2. Frontend: The Web Interface that helps users in deposit to Lending Pool, leverage on DEX and withdraw from Lending Pool.3. Backend: Helps smart-contracts to work with external information, for example, as DEX. Ensures stable operation of the application.

Deployed Contracts

Testnet: 
    https://testnet.tonviewer.com/kQBCL8NLgieN-9ySFDB1_0038tsW-cxOOseIFTXanYbvZY4H

Users
There are two groups of users who would be interested in using hTON: depositors and farmers.

Depositors
Depositors deposit their money in Lending Pools (the pool entry amount must be >= 1 Ton). Their money is taken by farmers who farm positions with leverage on DEX. The proceeds are divided between farmers and depositors. When the depositor wants to withdraw his money, he needs to click the Withdraw button and withdraw his invested money + % of the farmers' positions.

Farmers
To become a farmer you need to pledge a certain percentage to the amount of leverage. Afterwards, a DEX window opens inside the service, where the farmer can choose an attractive position and take a leverage of 1.5x-3x. In case of loss, his pledged money from the pool is distributed among the depositors. If he wins, he receives a percentage of the profit from the position.

Smart Contracts

There are 5 smart contracts in the fTON protocol: Liquidity, Oracle, Borrow, Lend, LendMint.

Liquidity

Liquidity is responsible for the correct price-to-coin ratio. If the price of a coin begins to fall by more than 25%, the pool automatically closes and sends money back to users.

Oracle

The Oracle is responsible for receiving information from dexes. Our project uses a completely on-chain oracle, for honest readings without excesses, as happens in off-chain oracles.

Borrow

Borrow acts as a leveraged loan from the Dex. Before taking leverage, you must make a deposit to a pool whose coin is in the user’s wallet.

Lend

Lend is a deposit into liquidity pools.

LendMint

After farming with leverage on Dexas, users receive LP tokens, which are wrapped tokens of the Dex on which farming took place.

Development
Install dependencies: npm install
Build contracts: npx blueprint build
Deploy: npx blueprint run
Test: npx blueprint test

