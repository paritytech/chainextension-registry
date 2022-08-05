# chainextension-registry

A list of known
[`ChainExtensions`](https://paritytech.github.io/substrate/master/pallet_contracts/chain_extension/index.html)
for
[`pallet-contracts`](https://github.com/paritytech/substrate/tree/master/frame/contracts).
A `ChainExtension` should be registered here when it is generally useful and offered as an
off-the-shelf module to other developers. The reason for that is to coordinate on their
IDs.

The extensions are defined in a json file. Example:

```json
[
    {
        "id": 1,
        "repository:": "https://github.com/paritytech/polkadot",
        "typeName:": "XcmExtension"
    },
    {
        "id": 99,
        "repository:": "https://github.com/paritytech/substrate",
        "typeName:": "AssetExtension"
    }
]
```

## Process

1. Open a PR to add a new chain extension to `registry.json`.
2. Don't make backwards incompatible changes to the extension after it is registered.
3. Add a new version under a new ID if you need to make incompatible changes.
