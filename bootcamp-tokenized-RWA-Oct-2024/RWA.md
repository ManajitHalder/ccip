# RWA Bootcamp by Chainlink October 2024

- [Day-1 youtube link](https://www.youtube.com/watch?v=iXWovCSahE0)
- [Day-2 youtube link](https://www.youtube.com/watch?v=OvfGvtNzEOM)
- [Gitbook presentation link](https://cll-devrel.gitbook.io/tokenized-rwa-bootcamp-2024/)

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

