# Rainbow 🌈

An open source repository for Rainbow Swap front end interface and smart contracts maintained by [Blackbot](https://blackbot.technology/). Rainbow Swap is a Aggregator on TON 💎.

![main banner.png](docs%2Fassets%2Fmain%20banner.png)

### Interfaces

- Web: [rainbow.ag](https://rainbow.ag)

### Contact

- Telegram: [@rainbow_swap](https://t.me/mattdev071)
- Email: [info.blackbot@gmail.com](mailto:mattdev071@gmail.com)

### Problem

TON DEXes have fragmented liquidity, each with its own set of liquid tokens. As the TON ecosystem grows, this uneven distribution worsens, leading to inefficient trades and arbitrage opportunities. Users often lose money due to the high price impact when swapping tokens on a single DEX.

### Solution

Rainbow Swap aggregates liquidity from multiple TON DEXes, distributing trade volume across optimal routes to minimize price impact and slippage. This ensures users get the best possible prices in a single transaction.

### Examples

![not example.png](docs%2Fassets%2Fnot%20example.png)
![usdt example.png](docs%2Fassets%2Fusdt%20example.png)


# Development info

### Getting Started

1. Clone repository
```
git clone https://github.com/0xblackbot/rainbow-swap.git && cd rainbow-swap
```

2. Install dependencies
```
yarn
```

3. Start the development server
```
yarn start
```

[Instruction on how to run development application as TMA](docs%2FTMA-development.md)

If you want to contribute your code, before making a pull request - ensure, that code passes all pipeline checks. You can manually check it before a pull request running commands
```
yarn ts
yarn lint
```

### Smart contract

`Rainbow routing wallet` smart contract acts as a middleman, enabling seamless swaps between two different decentralized exchanges (DEXes) in a single transaction.  
In order to insure against the loss of assets (there was no such cases yet), it also allows users to withdraw TON or jettons, similar to a Jetton Wallet contract.  

Events diagram:

![smart-contract-events-diagram.svg](docs%2Fassets%2Fsmart-contract-events-diagram.svg)

Smart contract are written using [FunC](https://docs.ton.org/develop/func/overview) language.  
All code could be found in [contracts](contracts) folder.  

To build `Rainbow routing wallet` smart contract run
```
yarn build:contract
```

