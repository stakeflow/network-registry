# Network Registry

This repository is designed to manage, identify, and personalize entities in the Stakeflow Explorer.   

The structure of the repository is shown below:   
```shell
cosmos-hub/
├─ validators/
│  ├─ cosmosvaloper1wdrypwex63geqswmcy5qynv4w3z3dyef2qmyna/
│  │  ├─ validator-details.json
│  │  ├─ logo.png
│  ├─ cosmosvaloper1xqz9pemz5e5zycaa89kys5aw6m8rhgsvwhv7le/
│  │  ├─ logo.svg
│  │  ├─ validator-details.json
autonity/
├─ validators/
│  ├─ 0x51b26F1Fbe01De79226067cc11f32c4bef4F56F8/
│  │  ├─ logo.svg
│  │  ├─ validator-details.json
│  ├─ 0x98F3a54308221352AfFa2cE7089A7f1E2AC2409e/
│  │  ├─ logo.png
│  │  ├─ validator-details.json
│  ├─ 0xA065Ae42A6cc991996a46E799Be642B2cDFea1E2/
│  │  ├─ logo.svg
│  │  ├─ validator-details.json
another-network/
├─ validators/
```

In the root directory, the folders that correspond to each network, supported by the Stakeflow explorer are placed.   

Each network folder contains the folders of the entities represented in the given network. For now, it is only the Validators folder, but folders with new entities will be added as Stakeflow evolves.   

The Validators folder contains the folders of the individual validators, named according to the validator address of each individual validator.   

Each validator folder contains two files - `logo.svg` or `logo.png` and `validator-details.json`   

`logo.svg` - is an image file representing the validator's logo.   

`validator-details.json` - is a JSON file that contains basic information about the validator and has the following template:   
```javascript
{
    "moniker": "",
    "keybase": "",
    "description": "",
    "website": ""
    "email": "",
    "github": "",
    "twitter": "",
    "discord": "",
    "telegram": ""
}
```
In order to add your validator to Stakeflow, you need to create a pull-request, that adds a folder named according to the valoper address of your validator and containing properly arranged `logo.svg` and `validator-details.json` to the folder of the appropriate network. Please pay **attention**, that the *moniker* field of `validator-details.json` is mandatory

#### You can see how to add your validator info following the [instruction](https://github.com/stakeflow/network-registry/blob/main/TUTORIAL.md).
