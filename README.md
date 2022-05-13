# alphawallet-curate

## Android test

```bash
$ cd android
$ ./gradlew clean test

> Task :lib:test

io.kleros.alphawallet.curate.android.KlerosCurateServiceTest > klerosCurateService STANDARD_OUT
    2022-05-13 17:32:53,611 [DEBUG ] KlerosCurateService - Trying Curate Ethereum for address 0xdAC17F958D2ee523a2206206994597C13D831ec7...
    2022-05-13 17:32:53,618 [DEBUG ] GraphClient - {"query":"{ litems( where: {registry: \"0x6e31d83b0c696f7d57241d3dffd0f2b628d14c67\", status: Registered, keywords_contains: \"0xdAC17F958D2ee523a2206206994597C13D831ec7\"} ) { keywords data } }"}
    2022-05-13 17:32:54,136 [DEBUG ] GraphClient - Response{protocol=h2, code=200, message=, url=https://api.thegraph.com/subgraphs/name/kleros/curate}
    2022-05-13 17:32:54,142 [DEBUG ] GraphClient - {"data":{"litems":[{"keywords":"0x6e31d83b0c696f7d57241d3dffd0f2b628d14c67 | Tether: USDT Stablecoin | 0xdAC17F958D2ee523a2206206994597C13D831ec7 | https://tether.to/","data":"/ipfs/QmbdRcL7MRjeEbMyZLPQ6v5PbAGp4atnGKD5GD374jF8tG/item.json"}]}}
    2022-05-13 17:32:54,148 [DEBUG ] KlerosCurateService - ipfsCid: /ipfs/QmbdRcL7MRjeEbMyZLPQ6v5PbAGp4atnGKD5GD374jF8tG/item.json
    2022-05-13 17:32:54,556 [DEBUG ] IpfsClient - Response: Response{protocol=h2, code=200, message=, url=https://ipfs.kleros.io/ipfs/QmbdRcL7MRjeEbMyZLPQ6v5PbAGp4atnGKD5GD374jF8tG/item.json}
    2022-05-13 17:32:54,557 [DEBUG ] IpfsClient - ResponseBody: {"columns":[{"label":"Public Name Tag","description":"The Public Name tag of a contract address indicates a commonly-used name of the smart contract and clearly identifies it to avoid potential confusion. (e.g. Eth2 Deposit Contract).","type":"text","isIdentifier":true},{"label":"Contract Address","description":"The Ethereum mainnet hexadecimal address of the smart contract being tagged.","type":"address","isIdentifier":true},{"label":"UI/Website Link","description":"The URL of the most popular user interface used to interact with the contract tagged or the URL of the official website of the contract deployer (e.g. https://launchpad.ethereum.org/en/).","type":"link","isIdentifier":true},{"label":"Public Note","description":"The Public Note is a short, mandatory comment field used to add a comment/information about the contract that could not fit in the public name tag (e.g. Official Ethereum 2.0 Beacon Chain deposit contact address).","type":"text"}],"values":{"Public Name Tag":"Tether: USDT Stablecoin","Contract Address":"0xdAC17F958D2ee523a2206206994597C13D831ec7","UI/Website Link":"https://tether.to/","Public Note":"The contract of Tether (USDT) stablecoin."}}
    2022-05-13 17:32:54,577 [DEBUG ] KlerosCurateService - IpfsItemValues: IpfsItemValues{publicNameTag='Tether: USDT Stablecoin', contractAddress='0xdAC17F958D2ee523a2206206994597C13D831ec7', uiWebsiteLink='https://tether.to/', publicNote='The contract of Tether (USDT) stablecoin.'}
    2022-05-13 17:32:54,578 [DEBUG ] KlerosCurateService - Trying Curate Ethereum for address 0xe592427a0aece92de3edee1f18e0157c05861564...
    2022-05-13 17:32:54,578 [DEBUG ] GraphClient - {"query":"{ litems( where: {registry: \"0x6e31d83b0c696f7d57241d3dffd0f2b628d14c67\", status: Registered, keywords_contains: \"0xe592427a0aece92de3edee1f18e0157c05861564\"} ) { keywords data } }"}
    2022-05-13 17:32:54,769 [DEBUG ] GraphClient - Response{protocol=h2, code=200, message=, url=https://api.thegraph.com/subgraphs/name/kleros/curate}
    2022-05-13 17:32:54,771 [DEBUG ] GraphClient - {"data":{"litems":[]}}
    2022-05-13 17:32:54,772 [DEBUG ] KlerosCurateService - No information from Curate Ethereum, trying Curate Gnosis for address 0xe592427a0aece92de3edee1f18e0157c05861564...
    2022-05-13 17:32:54,772 [DEBUG ] GraphClient - {"query":"{ litems( where: {registry: \"0x76944a2678a0954a610096ee78e8ceb8d46d5922\", status: Registered, keywords_contains: \"0xe592427a0aece92de3edee1f18e0157c05861564\"} ) { keywords data } }"}
    2022-05-13 17:32:54,965 [DEBUG ] GraphClient - Response{protocol=h2, code=200, message=, url=https://api.thegraph.com/subgraphs/name/eccentricexit/curate-xdai-ii}
    2022-05-13 17:32:54,966 [DEBUG ] GraphClient - {"data":{"litems":[{"keywords":"0x76944a2678a0954a610096ee78e8ceb8d46d5922 | Uniswap V3: Router 1 | 0xe592427a0aece92de3edee1f18e0157c05861564 | https://app.uniswap.org/#/swap","data":"/ipfs/QmeB3Tg5ue3GdaFBputGqBrFJWB112K4aVChpZEZ85nwa5/item.json"}]}}
    2022-05-13 17:32:54,966 [DEBUG ] KlerosCurateService - ipfsCid: /ipfs/QmeB3Tg5ue3GdaFBputGqBrFJWB112K4aVChpZEZ85nwa5/item.json
    2022-05-13 17:32:55,106 [DEBUG ] IpfsClient - Response: Response{protocol=h2, code=200, message=, url=https://ipfs.kleros.io/ipfs/QmeB3Tg5ue3GdaFBputGqBrFJWB112K4aVChpZEZ85nwa5/item.json}
    2022-05-13 17:32:55,106 [DEBUG ] IpfsClient - ResponseBody: {"columns":[{"label":"Public Name Tag","description":"The Public Name tag of a contract address indicates a commonly-used name of the smart contract and clearly identifies it to avoid potential confusion. (e.g. Eth2 Deposit Contract).","type":"text","isIdentifier":true},{"label":"Contract Address","description":"The Ethereum mainnet hexadecimal address of the smart contract being tagged.","type":"address","isIdentifier":true},{"label":"UI/Website Link","description":"The URL of the most popular user interface used to interact with the contract tagged or the URL of the official website of the contract deployer (e.g. https://launchpad.ethereum.org/en/).","type":"link","isIdentifier":true},{"label":"Public Note","description":"The Public Note is a short, mandatory comment field used to add a comment/information about the contract that could not fit in the public name tag (e.g. Official Ethereum 2.0 Beacon Chain deposit contact address).","type":"text"}],"values":{"Public Name Tag":"Uniswap V3: Router 1","Contract Address":"0xe592427a0aece92de3edee1f18e0157c05861564","UI/Website Link":"https://app.uniswap.org/#/swap","Public Note":"Version 1 of the Uniswap V3 Router."}}
    2022-05-13 17:32:55,107 [DEBUG ] KlerosCurateService - IpfsItemValues: IpfsItemValues{publicNameTag='Uniswap V3: Router 1', contractAddress='0xe592427a0aece92de3edee1f18e0157c05861564', uiWebsiteLink='https://app.uniswap.org/#/swap', publicNote='Version 1 of the Uniswap V3 Router.'}
    2022-05-13 17:32:55,107 [DEBUG ] KlerosCurateService - Trying Curate Ethereum for address 0xC18360217D8F7Ab5e7c516566761Ea12Ce7F9D72...
    2022-05-13 17:32:55,107 [DEBUG ] GraphClient - {"query":"{ litems( where: {registry: \"0x6e31d83b0c696f7d57241d3dffd0f2b628d14c67\", status: Registered, keywords_contains: \"0xC18360217D8F7Ab5e7c516566761Ea12Ce7F9D72\"} ) { keywords data } }"}
    2022-05-13 17:32:55,301 [DEBUG ] GraphClient - Response{protocol=h2, code=200, message=, url=https://api.thegraph.com/subgraphs/name/kleros/curate}
    2022-05-13 17:32:55,302 [DEBUG ] GraphClient - {"data":{"litems":[]}}
    2022-05-13 17:32:55,302 [DEBUG ] KlerosCurateService - No information from Curate Ethereum, trying Curate Gnosis for address 0xC18360217D8F7Ab5e7c516566761Ea12Ce7F9D72...
    2022-05-13 17:32:55,302 [DEBUG ] GraphClient - {"query":"{ litems( where: {registry: \"0x76944a2678a0954a610096ee78e8ceb8d46d5922\", status: Registered, keywords_contains: \"0xC18360217D8F7Ab5e7c516566761Ea12Ce7F9D72\"} ) { keywords data } }"}
    2022-05-13 17:32:55,498 [DEBUG ] GraphClient - Response{protocol=h2, code=200, message=, url=https://api.thegraph.com/subgraphs/name/eccentricexit/curate-xdai-ii}
    2022-05-13 17:32:55,498 [DEBUG ] GraphClient - {"data":{"litems":[]}}
    2022-05-13 17:32:55,498 [DEBUG ] KlerosCurateService - No information from Curate Gnosis for address 0xC18360217D8F7Ab5e7c516566761Ea12Ce7F9D72...

io.kleros.alphawallet.curate.android.KlerosCurateServiceTest > klerosCurateService PASSED


BUILD SUCCESSFUL in 4s

```
