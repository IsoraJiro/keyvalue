Smart contract for key value

1/ Create account for smart contract
near create-account keyvalue.test_nhaplycafedang.testnet --masterAccount test_nhaplycafedang.testnet --initialBalance 10

2/ Deploy smart contract
near deploy --wasmFile target/wasm32-unknown-unknown/release/key_value_storage.wasm --accountId test_nhaplycafedang.testnet

3/ Create key/value & store in smart contract
near call keyvalue.test_nhaplycafedang.testnet create_update '{"k": "gfs", "v" : "2022"}' --accountId keyvalue.test_nhaplycafedang.testnet

4/ View key/value stored in smart contract
near view keyvalue.test_nhaplycafedang.testnet read '{"k": "gfs"}' --accountId keyvalue.test_nhaplycafedang.testnet

5/ Delete key stored in smart contract
near call keyvalue.test_nhaplycafedang.testnet delete '{"k": "gfs", "v" : "1"}' --accountId keyvalue.test_nhaplycafedang.testnet
