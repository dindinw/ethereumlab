Course materials for the March 2017
=========
Course website: http://soc1024.ece.illinois.edu/teaching/ece598am/fall2016/

Get the docker image with `docker pull socrates1024/ece598am:fall2016`

Basic resources on Serpent and smart contract programming security: [(EthereumLab)](http://mc2-umd.github.io/ethereumlab/) [(Serpent Programmer’s Guide)](http://mc2-umd.github.io/ethereumlab/docs/serpent_tutorial.pdf) [(Serpent Wiki)](https://github.com/ethereum/wiki/wiki/Serpent)

Resources in this directory:
--
   - [example-01-basics.py](example-01-basics.py) :
      Illustrates the use of the pyethereum.tester" simulation framework, along with useful idioms for printing the state of a contract, setting debug logs, and basic Serpent use
   - [example-02-buggy-lottery.py](example-02-buggy-lottery.py):
      A simple gambling game for 2 players, based on the block number. (Actually it's an example of several pitfalls, like those discussed in class)
   - [example-03a-rps.py](example-03a-rps.py):
      A Rock Paper Scissors game, also with several pitfalls
   - [example-03c-rps.py](example-03c-rps.py):
      A robustified version of the Rock Paper Scissors game
   - [example-04-micropayments.py](example-04-micropayments.py):
      A simple payment channel. Actually a useful smart contract for fast off-chain payments. Great starting point for learning about Lightning network, "State Channels", etc. Also provides idioms for verifying signatures and checking hashes, illustrates the use of Serpent macros
   - [example-05-merkletree.py](example-05-merkletree.py):
      Merkle tree example - The on-chain contract just stores the root hash of a dataset. The contract can verify a Merkle Tree proof that a particular element exists at a given element in the dataset. Starting point for a "decentralized file storage" application
   - [solidity-merkletree.py](solidity-merkletree.py):
      pyethereum also works with Solidity
   - [serpent_extern.py](serpent_extern.py):
     Illustrates how to call one contract from another

Building from the [Dockerfile](Dockerfile)
--
```
sudo docker build -t "ece598:dockerfile" ./
sudo docker run --name testinstance -it ece598:dockerfile
sudo docker start testinstance
sudo docker attach testinstance
```

What next?
---
Roughly, the instructions for the class project are "build something cool in 3 weeks" 

