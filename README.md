# TX-Fuzz

TX-Fuzz is a package containing helpful functions to create random transactions. 
It can be used to easily access fuzzed transactions from within other programs.

## Usage

```
cd cmd/livefuzzer
go build
./livefuzzer <command> <rpc-url> <pvkey> <mnemonic> <start..end> [<hex-formatted-seed>] [<bool-access-list>]

For Example:
./livefuzzer spam https://127.0.0.1:8545 <PRIVATE_KEY_OF_THE_ACCOUNT> "MNEMONIC_PHRASE_TO_GENERATE_ACCOUNTS_FOR_TX_SPAMMING" 0..10
```

Tx-fuzz allows for an optional seed parameter to get reproducible fuzz transactions

## Advanced usage
You can optionally specify a seed parameter or a secret key to use as a faucet

```
./livefuzzer spam <seed> [no-al] <SK> 
```
