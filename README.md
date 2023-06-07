# LinkEvent

LinkEvent is a decentralized event registration platform built on blockchain technology. It leverages the power of smart contracts and Chainlink's decentralized oracle network to create a secure, transparent, and efficient event registration system.

## Inspiration

The goal of LinkEvent is to explore the possibilities of digital identification while ensuring the safety of sensitive personal information. We understand that posting such data on-chain can have long-lasting consequences. Therefore, we have focused on developing best practices for storing semi-secure data, such as a person's work email, without the risk of permanent damage.

By targeting event registration, we present a practical use case that is ephemeral and pragmatic, lowering the barriers for individuals skeptical about digital identity adoption.

## Features

- Create and manage events
- Seamless event registration process
- Secure storage of participant data
- Offloading expensive data to IPFS using Chainlink
- Data validation and integrity checks
- Front-end agnostic design

## How it Works

LinkEvent combines Solidity smart contracts with a React Native front-end to deliver a robust and user-friendly experience. To overcome the cost limitations of storing large string data on-chain, we utilize Chainlink to bridge the gap with IPFS (InterPlanetary File System). The data submitted through the app is stored on IPFS, while a CID (Content Identifier) is generated and stored on-chain along with other cost-effective uints. AWS Lambda functions handle the IPFS connection and badge creation.

This approach offers several advantages:

- Data validation: The contract can validate identity against an API or implement content policies, ensuring adherence to predefined standards.
- Data integrity: By building JSON objects on IPFS through the contract, we can ensure compliance with a standardized format and prevent malicious or inappropriate data submissions.
- Front-end agnostic: LinkEvent's infrastructure requirements are enforced at the contract level, allowing developers to create their own front-end while maintaining the platform's technical guarantees.
- Scalability: LinkEvent's cost remains fixed, regardless of additional data requirements, as the storage burden is offloaded to IPFS.

## Challenges

During the development of LinkEvent, we encountered several challenges. Our team had to learn Solidity from scratch to write the smart contracts. Additionally, the documentation for external adapters and Chainlink nodes proved to be lacking, requiring extensive exploration and discovery through resources like NAAS on Linkpool.

Testing Chainlink posed difficulties, as local testing was not possible, necessitating deployment and testing on a testnet for each iteration. We hope to see improvements in the infrastructure to simplify the testing process in the future.

## Accomplishments

Throughout the development process, we achieved several notable milestones. We created a reusable module called Storable, similar to Ownable, which allows the addition of data offloading to any contract. Moreover, we implemented an efficient pseudo-linked list structure in the Registrations contract to enhance the performance of navigating through the extensive registrations array.

## What's Next for LinkEvent

We are incredibly excited about the potential of LinkEvent. Having invested over 140 hours into this project, we are keen to gauge its reception from the community. Moving forward, we plan to continue refining and expanding LinkEvent, albeit at a slower pace due to the current intensity of development. We are open to collaboration, incubator opportunities, and accelerators should the project gain traction.

Events hold significant potential for crypto adoption. Imagine concert tickets sold in Doge or Coachella tickets sold in Solana, with transactions processed at incredible speeds and without the risk of server crashes during registration.

## Technologies Used

- Amazon Web Services (AWS)
- Chainlink
- Ethereum
- Keychain
- Linkpool
- Python
- React Native
- Solidity
