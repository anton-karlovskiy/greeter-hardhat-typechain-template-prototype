
### Hardhat project (smart contract)

#### Notes

- `tsconfig.json`
- `main` and `types` properties in `package.json`

In one terminal, start your hardhat node:

```bash
cd greeter
yarn install
yarn hardhat-node
```

In another terminal, compile and deploy the contracts as well as creating the typechain interfaces:

```bash
cd greeter
yarn build
yarn hardhat-deploy:local
```

Tip: you can link your projects with yarn to sync updates easily.

```bash
yarn link
```

#### TODOs

- Could remove `"./scripts"` and `"./test"` from `"include"` of `tsconfig.json` as they are not used in the frontend project.
- Can set up `yarn install` via GitHub repository.
```bash
  "dependencies": {
    "GitRepo": "git+https://<token-from-github>:x-oauth-basic@github.com/<user>/<GitRepo>.git"
  }
```
- Could use [yalc](https://github.com/wclr/yalc) rather than `yarn link`.
- Should establish approaches to deploying to mainnet and testnet as well as to the local network.

### Frontend project (e.g. create-react-app or Next.js)

To get started on the UI:

```bash
cd dapp
yarn install
yarn link greeter
yarn dev
```

Import in a UI component like so:
```js
import {
  Greeter,
  Greeter__factory
} from 'greeter';
```
