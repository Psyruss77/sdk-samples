# Work with SDK v.1 multisig example

In this example we use [ton-client-js](https://github.com/tonlabs/ton-client-js) (ton-client-node-js is deprecated) to deploy solidity multisig contract [SafeMultisigWallet.sol](https://github.com/tonlabs/ton-labs-contracts/blob/master/solidity/safemultisig/SafeMultisigWallet.abi.json) in to test [net.ton.dev](https://net.ton.live/) blockchain.

## Prerequisite

* Node.js >= [12.x installed](https://nodejs.org)
* [Docker](https://docs.docker.com/desktop/#download-and-install) (if you want to use local blockchain TON OS SE) daemon running

In order to do it, perform these steps:

1. Make preparations.
2. Deploy contract.
3. Use deployed contract.

Below we describe each of the steps in more detail.

## Make preparations

You can find the source code in `preparation.js`. In order to run it, use:

```sh
npm i
node preparation.js
```

In this step:

1. Generate a seed phrase based on a dictionary and number of words specified.
2. Use seed phrase to generate public and private key pair.
3. Write these in files.
4. Check the future contract address.


## Deploy contract

You can find the source code in `deploy.js`. In order to run it, use:
                                         
```sh
node deploy.js
```

In this step we use the key pair to deploy the contract. Before performing this step you need to ensure you have
at least 0.5 tokens on your future wallet address.

## Use deployed contract

You can find the source code in `work-with-multisig.js`. In order to run it, use:
                                                     
```sh
node work-with-multisig.js
```

In this step we:

1. Get the custodians list.
2. Send a transaction to transfer 0.1 token to pre-defined address.
3. Output sent transaction information.
