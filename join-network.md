
Reactivate bid
```bash
sudo casper-client put-deploy --secret-key /etc/casper/validator_keys/secret_key.pem --chain-name casper --session-path "$HOME/casper-node/target/wasm32-unknown-unknown/release/activate_bid.wasm" --payment-amount 300000000 --session-arg "validator_public_key:public_key='$(cat /etc/casper/validator_keys/public_key_hex)'"
```

Check that the deploy was successful with the casper-client get-deploy <deploy_hash> or by searching for the deploy_hash on https://cspr.live/.

https://github.com/casper-network/casper-node/wiki/Recover-from-Validator-Ejection
