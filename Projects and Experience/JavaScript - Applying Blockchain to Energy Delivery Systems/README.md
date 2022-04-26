### Please refer to the dedicated website for our project here: [Applying Blockchain To Energy Delivery Systems](https://sdmay20-12.sd.ece.iastate.edu/)

# Applying Blockchain to Energy Delivery Systems
## Problem Statement
- Energy Delivery Systems are deployed in an environment that is geographically distributed utilizing public internet infrastructure for communications. The integrity of measurements, commands, and authenticity of control devices performing communication are critical for trusted operations.

## Proposed Solution
- The purpose of this project is to develop a blockchain Energy Delivery System solution to solve the problem statement. The project is driven by the need described in the problem statement above, to create a secure network for a geographically diverse Energy Delivery System. To help mitigate security concerns, the use of blockchain technology would provide a secure network for managing Energy Delivery Systems by removing the dependency on a central service. Additionally, a permissioned blockchain system ensures a higher level of security when concerned with cyber attacks similar to a fifty-one percent attack. With this project we hope to deploy a permissioned blockchain system for interaction between devices on an Energy Delivery System and users managing those devices.

## Technologies & Methodologies
- We used an Agile approach to development using two-week sprints with a retro and demo at the end of each sprint, as necessary. We followed a test-driven development process where all merge requests were required to pass all component and system-level tests and be reviewed and approved by at least one other member of the team. We also used Gitlab issues to track individual and team progress on tasks taken from the Gantt chart we created.
- We developed a software solution using a component based architecture, where the components consisted of an API, a User Interface, and the Blockchain Network (network of individually hosted nodes that uses a Publisher to post data, a Ledger to authenticate and contain data, and smart contracts for the manipulation and query of data).
  - The blockchain network was developed using HyperLedger Fabric that used YAML configuration files for structuring/setting up the network and Docker Composer for defining, creating, and deploying containerized nodes. The network reports ledger updates to the API, receives requests to run smart contracts from the API, and after authenticating the requester, runs smart contracts in order to update the ledger using a Publisher. The publisher uses Node.js and is able to post data to the network. We used the default key value database called CouchDB to handle translation logs and ledgers. Smart Contracts give users of the system the ability to query, create, and/or update an entry in the blockchain network based on the users permissions for the system.
  - The API was developed using Node.js and runs smart contracts when new performance data has been received by a device on the network or an authenticated user requests to view data. 
  - The User Interface was developed using ReactJS because ReactJS is primarily used for building single page applications, which fitted our expected solution for the web user interface. The UI allowed users to request data from devices on the network and manage the blockchain users.



## Diagrams
>![Simple Use Case Diagram](https://user-images.githubusercontent.com/88903387/165389649-543d65ed-6748-4234-8bdc-dc6bd7bc7615.png)
>![High Level Module Diagram](https://user-images.githubusercontent.com/88903387/165389683-3207e714-d62c-40ef-ba4b-3022968315b4.png)
