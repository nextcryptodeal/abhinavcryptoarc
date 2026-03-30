# abhinavcryptoarc
description how to deploy contract on arc
deploy a simple contract on arc testnet (easy step-by-step guide).
we’ll start by setting up your deployment environment via terminal:
— mac users open the terminal on your system
windows users install ubuntu (WSL) on your PC using this guide 
copy and paste command at each step

step 1: install foundry
curl -L https://foundry.paradigm.xyz | bash
foundryup

step 2: initialize project
forge init arc-deploy
cd arc-deploy

step 3: create your contract
touch src/HelloArc.sol

paste this inside 👇

// SPDX-License-Identifier: MIT
pragma solidity ^0.8.20;

contract HelloArc {
    string public greeting;

    constructor(string memory _greeting) {
        greeting = _greeting;
    }

    function setGreeting(string memory _greeting) public {
        greeting = _greeting;
    }

    function getGreeting() public view returns (string memory) {
        return greeting;
    }
}
