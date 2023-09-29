# Foundry

**Foundry is a blazing fast, portable and modular toolkit for Ethereum application development written in Rust.**

Foundry consists of:

- **Forge**: Ethereum testing framework (like Truffle, Hardhat and DappTools).
- **Cast**: Swiss army knife for interacting with EVM smart contracts, sending transactions and getting chain data.
- **Anvil**: Local Ethereum node, akin to Ganache, Hardhat Network.
- **Chisel**: Fast, utilitarian, and verbose solidity REPL.

## Documentation

<https://book.getfoundry.sh/>

## Usage

### Build

```shell
forge build
```

### Test

```shell
forge test
```

### Format

```shell
forge fmt
```

### Gas Snapshots

```shell
forge snapshot
```

### Anvil

```shell
anvil
```

### Deploy

```shell
forge script script/Counter.s.sol:CounterScript --rpc-url <your_rpc_url> --private-key <your_private_key>
```

### Cast

```shell
cast <subcommand>
```

### Help

```shell
forge --help
anvil --help
cast --help
```

## foundry-goerli-YT

```shell
3777* mcd foundry-projects2
3778* forge init foundry-goerli-YT
3779* cd foundry-goerli-YT/
3780* c
3781* touch remappings.txt
3782* forge remappings
3783* forge test
3784* forge test --gas-report
3785* forge test -vv

3787* forge test -vvvv
3788* anvil
3789* export PRIVATE_KEY=0xac0974b784d7bf4f2ff80
3790* forge script script/Counter.s.sol --fork-url http://localhost:8545 --broadcast
3791* forge build
3792* forge script script/Counter.s.sol --fork-url http://localhost:8545 --broadcast --private-key=$PRIVATE_KEY
3793* forge script script/Counter.s.sol --fork-url http://localhost:8545 --broadcast
3794* forge script script/CrowdFunding.s.sol --fork-url http://localhost:8545 --broadcast --private-key=$PRIVATE_KEY
3795* export CONTRACT_ADDR=0xe7f1725e90bb3f0512
3796* export CAMPAIGN_OWNER_PRIV_KEY=0x59c6995e92f4603b6b78690d
3797* export CAMPAIGN_OWNER_ADDRESS=0x7099791b50e0d17dc79C8
3798* export CAMPAIGN_DONOR_PRIV_KEY=0x5de411870fc3fb9a804cdab365a
3799* cast send $CONTRACT_ADDR "createCampaign(address,string,string,uint256,uint256,string)"  $CAMPAIGN_OWNER_ADDRESS "Campaign 1" "Campaign 1 Description" 10ether 1695963850 + 300 "https://i.kym-cdn.com/photos/images/newsfeed/002/205/307/1f7.jpg" --private-key=$CAMPAIGN_OWNER_PRIV_KEY
3800* cast call $CONTRACT_ADDR "getCampaign(uint256)(address,string,string,uint256,uint256,uint256,string)" 0
3801* cast send $CONTRACT_ADDR "donateToCampaign(uint256)" 0 --value 10ether --private-key=$CAMPAIGN_DONOR_PRIV_KEY
3802* cast call $CONTRACT_ADDR "getCampaign(uint256)(address,string,string,uint256,uint256,uint256,string)" 0
3803* cast balance $CAMPAIGN_OWNER_ADDRESS
3804* cast send $CONTRACT_ADDR "withdraw(uint256)" 0 --private-key=$CAMPAIGN_OWNER_PRIV_KEY
3805* cast balance $CAMPAIGN_OWNER_ADDRESS
3806* export GOERLI_URL=https://eth-goerli.g.alchemy.com/v2/ssfgfhfhhfhfh
3807* export PRIVATE_KEY=12345678
3808* export ETHERSCAN_KEY=ABCDEFGHIJKLMNOPQRSTUVWXYZ
3809* forge create --rpc-url $GOERLI_URL --private-key $PRIVATE_KEY src/CrowdFunding.sol:CrowdFunding --etherscan-api-key $ETHERSCAN_KEY --verify

3811* forge create --rpc-url $GOERLI_URL --private-key $PRIVATE_KEY src/CrowdFunding.sol:CrowdFunding --etherscan-api-key $ETHERSCAN_KEY --verify
3812* echo "# foundry-goerli-YT" >> README.md
```
