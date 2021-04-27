
### Hardhat project (smart contract)

In one terminal, start your hardhat node:

```bash
cd hardhat-sample
yarn install
yarn hardhat-node
```

In another terminal, compile and deploy the contracts as well as creating the typechain interfaces:

```bash
cd hardhat-sample
yarn build
yarn hardhat-deploy:local
```

Tip: you can link your projects with yarn to sync updates easily.

```bash
yarn link
```

### Next.js project (frontend UI)

To get started on the UI:

```bash
cd dapp
yarn install
yarn link hardhat-sample
yarn dev
```
