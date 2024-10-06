# RWA Bootcamp by Chainlink October 2024

[RWA Premier - Detailed Reference of Real-World Assets](https://github.com/andrejrakic/rwa-primer/tree/main)

Other resource links:

- [Day-1 youtube link](https://www.youtube.com/watch?v=iXWovCSahE0)
- [Day-2 youtube link](https://www.youtube.com/watch?v=OvfGvtNzEOM)
- [Gitbook presentation link](https://cll-devrel.gitbook.io/tokenized-rwa-bootcamp-2024/)
- [Github source code link](https://github.com/andrejrakic/rwa-primer/blob/main)

## What are Real-World Assets (RWAs)?

Real-world assets (RWAs) in blockchain are digital tokens that represent physical and traditional financial assets, such as currencies, commodities, equities, and bonds.

## What are Tokenized Real-World Assets (RWAs)?

Tokenized real-world assets (RWAs) are blockchain-based digital tokens that represent physical and traditional financial assets, such as cash, commodities, equities, bonds, credit, artwork, and intellectual property.

## Tokenizing Real-World Assets

Tokenizing real-world assets involves representing the ownership rights of assets as onchain tokens. In this process, a digital representation of the underlying asset is created, enabling onchain management of the asset’s ownership rights and helping to bridge the gap between physical and digital assets. 

## Benefits of Tokenized Assets

- `Liquidity`: Tokenized real-world assets (RWAs) can make traditionally illiquid assets more easily tradable. 
- `Transparency`: Since the tokenized assets are represented onchain, transparency and auditable asset management are ensured.
- `Accessibility`: Tokenized RWAs can broaden the potential user base of certain asset types.

## How To Tokenize Real-World Assets

The high-level process of tokenizing a real-world-asset involves several steps.

- `Asset selection`: Determining the real-world asset to be tokenized.

- `Token specifications`: Determining the type of token (fungible or non-fungible), the token standard to be used (like ERC20, ERC721, or ERC1155), and other fundamental aspects of the token.

- `Blockchain selection`: Choosing the public or private blockchain network on which to issue the tokens. Integrating Chainlink Cross-Chain Interoperability Protocol (CCIP) helps make the tokenized RWA available on any blockchain.

- `Offchain connection`: Most tokenized assets require high-quality offchain data from secure and reliable oracle services. Using a trusted verification mechanism to confirm the assets backing the RWA tokens is essential for maintaining user transparency. This typically involves a reputable service like Chainlink.

- `Issuance`: Deploying the smart contracts on the chosen network, minting the tokens, and making them available for usage.

## Deploy RealEstateToken.sol to Avalanche Fuji

Make sure to turn the `Solidity compiler optimizer on` to `200 runs` and `set `EVM version` to `Paris`.

Add the following in `DEPLOY` configuration section in `Remix`:

- `URI_`: ""

- `ccipRouterAddress`: 0xF694E193200268f9a4868e4Aa017A0118C9a8177
    - Refer https://cll-devrel.gitbook.io/tokenized-rwa-bootcamp-2024/day-1/exercise-1-cross-chain-real-estate#deploy-realestatetoken.sol-to-avalanche-fuji
    - Cross check from: https://docs.chain.link/ccip/supported-networks/v1_2_0/testnet#avalanche-fuji

- `linkTokenAddress`: 0x0b9d5D9136855f6FEc3c0993feE6E9CE8a297846
    - Refer https://cll-devrel.gitbook.io/tokenized-rwa-bootcamp-2024/day-1/exercise-1-cross-chain-real-estate#deploy-realestatetoken.sol-to-avalanche-fuji
    - Cross check from: https://docs.chain.link/ccip/supported-networks/v1_2_0/testnet#avalanche-fuji

- `currentChainSelector`: 14767482510784806043
    - Refer https://cll-devrel.gitbook.io/tokenized-rwa-bootcamp-2024/day-1/exercise-1-cross-chain-real-estate#deploy-realestatetoken.sol-to-avalanche-fuji
    - Cross check from: https://docs.chain.link/ccip/supported-networks/v1_2_0/testnet#avalanche-fuji

- `functionsRouterAddress`: 0xA9d587a00A31A52Ed70D6026794a8FC5E2F5dCb0
    - Refer https://cll-devrel.gitbook.io/tokenized-rwa-bootcamp-2024/day-1/exercise-1-cross-chain-real-estate#deploy-realestatetoken.sol-to-avalanche-fuji
    - Cross check from: https://functions.chain.link/ after `Connect Wallet` and Selecting `Avalance Fuji network`

## Homework

You will need to enter the following contract addresses that you deployed to Avalance Fuji:

- RealStateToken.sol:   0x32F411b1b788C01C40ce63068A73Fe02C2e5a9B5
- Issuer.sol:           0x630883c9411032E48De1E904Aa3060397b8c1700
- RWALending.sol:       0xA29cF0E68f58988BD9108628D3e101EAb91A5320
- EnglishAuction.sol:   0xc8B3E2d1F5b8C7143a55f4b5360E3c3BE6d8db73

Subscription ID: 13239

## Call the issue function of the Issuer.sol smart contract

To issue an ERC-1155 token to Alice, call the issue function of the Issuer.sol smart contract from the address you used to deploy that contract, and provide:

- `to`: Alice's wallet address (put any address you own)
- `amount`: 20
- `subscriptionId`: The Chainlink Functions Subscription ID you just created
- `gasLimit`: 300000
- `donID`: 0x66756e2d6176616c616e6368652d66756a692d31000000000000000000000000 (fun-avalanche-fuji-1)

Chainlink Function url [https://functions.chain.link/fuji/13239]

- `Subscription id`: `13239`
- `Consumers` added: 2
- `Consumer 1` address: `0x630883c9411032E48De1E904Aa3060397b8c1700`
- `Cousumer 2` address: `0x32F411b1b788C01C40ce63068A73Fe02C2e5a9B5`

Chailink Automation url: https://automation.chain.link/fuji/54467677339141086500662304650729934318048962756677572353893022489582490236471

