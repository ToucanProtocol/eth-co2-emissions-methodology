# eth-co2-emission-calculator

At [CO2ken](https://www.co2ken.io/) we're driven by building the tools to make the web3 space planet-positive. For that purpose, we've partnered with [Offsetra](https://offsetra.com/) — carbon market experts and offset retailers — to make sure we build meaningful tools with meaningful impact.

This repository is a shared effort between both our teams to lay the very first foundation for a carbon emission calculator of the Ethereum network. Where would love to see this going: an oracle which provides emissions data for an Ethereum transaction. We understand that the methodology we're proposing is far from perfect because data to accurately estimate related carbon emissions is scarce. Hence, we spun up this repository with the objective to create an open place for discussions and community-led improvements.

### Context
CO2ken started in 2020 at [EthLondon](https://ethlondon.com/) and went on to win the *Carbon Footrpint Track* in the [Blockchain for Social Impact Incubator](https://blockchainforsocialimpact.com/incubator-winners-2020/).  For more context take a look at our blog post [CO2ken Genesis](https://medium.com/curve-labs/co2ken-genesis-74d7a1387ea1).

In order to allow for the Ethereum transaction carbon offset functionality, we had to estimate the carbon intensity per unit of gas. Here's how we went about it (copied from [CO2ken Genesis](https://medium.com/curve-labs/co2ken-genesis-74d7a1387ea1)):

1. Look at the [energy consumption of Ethereum](https://digiconomist.net/ethereum-energy-consumption) for a given period,  and divide it by the [total amount of gas](https://www.etherchain.org/charts/totalGasUsage) used during that period.
2. Multiply this value with the [grid emission factor](https://www.iges.or.jp/en/pub/list-grid-emission-factor/en) of China. This factor describes how much CO2 is emitted when producing 1 MWh of electricity. China has an extensive cryptocurrency mining industry and a comparably bad energy to carbon emissions ratio which makes it a safe estimate, which is why we chose to use it. [estimating the location and the energy mix of the miners is key. Clearly, this was an oversimplification for hackathon purposes][...]   

Alternatively, we could take the energy consumption per Ethereum transaction found [here](https://digiconomist.net/ethereum-energy-consumption). But looking at gas gives us a more granular metric — and also, without getting into too much detail, it’s what various folks have argued for online [1](https://twitter.com/CryptoDemetrius/status/1144357399744196609) [2](https://hackernoon.com/green-smart-contracts-theres-more-to-blockchain-energy-consumption-than-consensus-898fb23eea75) [3](https://blog.usejournal.com/eip-2050-ghg-emissions-offsetting-for-crypto-transactions-7daaaee443fb). But hey, this is far from perfect and we’d be happy to collect your ideas as well. You can find all our calculations [here](https://docs.google.com/spreadsheets/d/1IpgKLB5e6JR12gjSplZ-Y1_xB9ylt8SNFyEKmhPtQ1A/edit#gid=650467083).

One thing we shouldn’t forget: we’re dealing with CO2 emissions. If we use the data we have, take the most conservative estimate, and start offsetting these blockchain emissions, we will at worst offset too much. Given the state of the planet, we kind of have to do this anyway.

Offsetra have created a first website at [carbon.fyi](https://carbon.fyi/) which returns the carbon emissions for a given wallet address. You can find the data sources behind that calculation [here](https://docs.google.com/spreadsheets/d/1KEw6yp2vmeA5LXZAuXGPjvVOtIVOvwzLdjwF3PizCgw/edit#gid=651392927).
