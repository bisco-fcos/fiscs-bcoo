1. see block number:
[group:1]> getBlockNumber
0
2. see node data:
[group:1]> getNodeIDList
[
    d6324e69f51e6c958b8200acdf7563daf3d7a3a6229890919471caa08157da0dfe37b3744235c9da42bd3b38d1c2f36383e3e3e00361c122b2b8ab466cd4edb8,
    b064fd55a6ca405cec1cb1a07d8499ee8bb8b17555e9c5b5d75b68086fe0ff780cf724484ad223592a233a9f785a6f210c651da128d60387cd006b19275b5b6d,
    daad460882e0a44a78ae8dd2ae08cf9a4e7f4fb1ba073f01041cfdb21031d6a9f25c7d200a947d572834270e44a489a9503bea6128640a79e90156119183ff89,
    bf01ab643930cc89a49abfab7f273c7ad1735ccd2f458e7cee47b09cd294d477a08149417dafea64188d887ff0f576d9dc509d2502b47bf75e43cbb6c41e7d32
]
[group:1]> getNodeVersion
{
    "Build Time":"20190506 10:55:15",
    "Build Type":"Linux/clang/RelWithDebInfo",
    "Chain Id":"1",
    "FISCO-BCOS Version":"2.0.0-rc2",
    "Git Branch":"master",
    "Git Commit Hash":"1bded79259c2b98a5e713dbbceeda53056acc6d7",
    "Supported Version":"2.0.0-rc2"
}
3. deploy HelloWord intelligient contract:
[group:1]> deploy HelloWorld
contract address:0x8c17cf316c1063ab6c89df875e96c9f0f5b2f744
4. view getDeployLog
[group:1]> getDeployLog

2019-05-28 16:24:37  [group:1]  HelloWorld            0x8c17cf316c1063ab6c89df875e96c9f0f5b2f744
5. call intelligent contract
[group:1]> getBlockNumber
1

[group:1]> call HelloWorld 0x8c17cf316c1063ab6c89df875e96c9f0f5b2f744 set "Hello, FISCO BCOS"
0xc672bbca7fd658a32771577cd1458b5bbd1aaeb66e028759e8874b0890df3d3b

[group:1]> getBlockNumber
2

[group:1]> call HelloWorld 0x8c17cf316c1063ab6c89df875e96c9f0f5b2f744 get
Hello, FISCO BCOS
6. see blocknumber again:
[group:1]> getBlockNumber
2
7. get link data
[group:1]> getNodeIDList
[
    d6324e69f51e6c958b8200acdf7563daf3d7a3a6229890919471caa08157da0dfe37b3744235c9da42bd3b38d1c2f36383e3e3e00361c122b2b8ab466cd4edb8,
    b064fd55a6ca405cec1cb1a07d8499ee8bb8b17555e9c5b5d75b68086fe0ff780cf724484ad223592a233a9f785a6f210c651da128d60387cd006b19275b5b6d,
    daad460882e0a44a78ae8dd2ae08cf9a4e7f4fb1ba073f01041cfdb21031d6a9f25c7d200a947d572834270e44a489a9503bea6128640a79e90156119183ff89,
    bf01ab643930cc89a49abfab7f273c7ad1735ccd2f458e7cee47b09cd294d477a08149417dafea64188d887ff0f576d9dc509d2502b47bf75e43cbb6c41e7d32
]
[group:1]> getNodeVersion
{
    "Build Time":"20190506 10:55:15",
    "Build Type":"Linux/clang/RelWithDebInfo",
    "Chain Id":"1",
    "FISCO-BCOS Version":"2.0.0-rc2",
    "Git Branch":"master",
    "Git Commit Hash":"1bded79259c2b98a5e713dbbceeda53056acc6d7",
    "Supported Version":"2.0.0-rc2"
}
8. deploy HelloWorld in CNS way
[group:1]> deployByCNS HelloWorld.sol 2.0
contract address:0x0b9ce0c6c4a85816bb328815d6befd7aa56119e8
9. view blockNumber again
[group:1]> getBlockNumber
4
10. get Blockchain Data again
[group:1]> getNodeIDList
[
    d6324e69f51e6c958b8200acdf7563daf3d7a3a6229890919471caa08157da0dfe37b3744235c9da42bd3b38d1c2f36383e3e3e00361c122b2b8ab466cd4edb8,
    b064fd55a6ca405cec1cb1a07d8499ee8bb8b17555e9c5b5d75b68086fe0ff780cf724484ad223592a233a9f785a6f210c651da128d60387cd006b19275b5b6d,
    daad460882e0a44a78ae8dd2ae08cf9a4e7f4fb1ba073f01041cfdb21031d6a9f25c7d200a947d572834270e44a489a9503bea6128640a79e90156119183ff89,
    bf01ab643930cc89a49abfab7f273c7ad1735ccd2f458e7cee47b09cd294d477a08149417dafea64188d887ff0f576d9dc509d2502b47bf75e43cbb6c41e7d32
]
[group:1]> getNodeVersion
{
    "Build Time":"20190506 10:55:15",
    "Build Type":"Linux/clang/RelWithDebInfo",
    "Chain Id":"1",
    "FISCO-BCOS Version":"2.0.0-rc2",
    "Git Branch":"master",
    "Git Commit Hash":"1bded79259c2b98a5e713dbbceeda53056acc6d7",
    "Supported Version":"2.0.0-rc2"
}

