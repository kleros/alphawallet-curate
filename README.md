# alphawallet-curate

## Android test

```bash
$ cd android
$ ./gradlew clean test

> Task :lib:test

io.kleros.alphawallet.curate.android.KlerosCurateServiceTest > klerosCurateService STANDARD_OUT
    2022-05-12 15:33:20,813 [DEBUG ] KlerosCurateService - {"query":"{ litems( where: {registry: \"0x6e31d83b0c696f7d57241d3dffd0f2b628d14c67\", status: Registered, keywords_contains: \"0xdAC17F958D2ee523a2206206994597C13D831ec7\"} ) { keywords data } }"}
    2022-05-12 15:33:21,299 [DEBUG ] KlerosCurateService - Response{protocol=h2, code=200, message=, url=https://api.thegraph.com/subgraphs/name/kleros/curate}
    2022-05-12 15:33:21,304 [DEBUG ] KlerosCurateService - {"data":{"litems":[{"keywords":"0x6e31d83b0c696f7d57241d3dffd0f2b628d14c67 | Tether: USDT Stablecoin | 0xdAC17F958D2ee523a2206206994597C13D831ec7 | https://tether.to/","data":"/ipfs/QmbdRcL7MRjeEbMyZLPQ6v5PbAGp4atnGKD5GD374jF8tG/item.json"}]}}
    2022-05-12 15:33:21,308 [DEBUG ] KlerosCurateService - ipfsCid: /ipfs/QmbdRcL7MRjeEbMyZLPQ6v5PbAGp4atnGKD5GD374jF8tG/item.json
    2022-05-12 15:33:22,663 [DEBUG ] KlerosCurateService - Response: Response{protocol=h2, code=200, message=, url=https://ipfs.kleros.io/ipfs/QmbdRcL7MRjeEbMyZLPQ6v5PbAGp4atnGKD5GD374jF8tG/item.json}
    2022-05-12 15:33:22,663 [DEBUG ] KlerosCurateService - ResponseBody: {"columns":[{"label":"Public Name Tag","description":"The Public Name tag of a contract address indicates a commonly-used name of the smart contract and clearly identifies it to avoid potential confusion. (e.g. Eth2 Deposit Contract).","type":"text","isIdentifier":true},{"label":"Contract Address","description":"The Ethereum mainnet hexadecimal address of the smart contract being tagged.","type":"address","isIdentifier":true},{"label":"UI/Website Link","description":"The URL of the most popular user interface used to interact with the contract tagged or the URL of the official website of the contract deployer (e.g. https://launchpad.ethereum.org/en/).","type":"link","isIdentifier":true},{"label":"Public Note","description":"The Public Note is a short, mandatory comment field used to add a comment/information about the contract that could not fit in the public name tag (e.g. Official Ethereum 2.0 Beacon Chain deposit contact address).","type":"text"}],"values":{"Public Name Tag":"Tether: USDT Stablecoin","Contract Address":"0xdAC17F958D2ee523a2206206994597C13D831ec7","UI/Website Link":"https://tether.to/","Public Note":"The contract of Tether (USDT) stablecoin."}}
    2022-05-12 15:33:22,669 [DEBUG ] KlerosCurateService - IpfsItemValues: IpfsItemValues{publicNameTag='Tether: USDT Stablecoin', contractAddress='0xdAC17F958D2ee523a2206206994597C13D831ec7', uiWebsiteLink='https://tether.to/', publicNote='The contract of Tether (USDT) stablecoin.'}

io.kleros.alphawallet.curate.android.KlerosCurateServiceTest > klerosCurateService PASSED

BUILD SUCCESSFUL in 4s

```
