importar version para compilación de openzepelling
`truffle obtain --solc 0.6.0 `


solución temporal : cambiar todos a //SPDX-License-Identifier: MIT
                                    pragma solidity >= 0.5.0 < 0.7.0;
                              
truffle compile
truffle deploy 
      
let instance = await ERC20.deployed()
 let accounts = await web3.eth.getAccounts()
 
instance.decimals() //18
instance.name() //MyToken
instance.symbol() //tKN

instance.sendCoin(accounts[1], 10, {from: accounts[0]})


//npm install @openzeppelin/contracts
pragma solidity ^0.6.0;

import "@openzeppelin/contracts/token/ERC721/ERC721.sol";

contract MyCollectible is ERC721 {
    constructor() ERC721("MyCollectible", "MCO") public {
    }
}