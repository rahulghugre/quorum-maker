# Quorum Maker V2.0

Synechron's Quorum Maker is a tool that allows users to spin up nodes in a Quorum network. Manually editing configuration files and creating nodes is a slow and error-prone process. Quorum Maker can create any number of nodes of various configurations dynamically with reduced user input. This provides a wizard-like interface with a series of questions to guide the user when creating nodes. Quorum Maker can create nodes to:

-	run with docker-compose (Raft consensus/Quorum 2.0.0) for easy use in development environments; or,
-	nodes to be distributed on separate Linux boxes or cloud instances for a production environment (Raft consensus/Quorum 2.0.2)

![Quorum Maker 2](https://github.com/synechron-finlabs/quorum-maker/blob/master/img/QM2.png) 
# Quorum Maker provides the following benefits:
  -	An easy interface to create and manage the Quorum Network
  -	A modern UI to monitor and manage Quorum Network
  -	A Network Map Service to be used for identifying nodes and self-publishing roles.  
  -	Block and Transaction Explorer
  -	Smart Contract Deployment
  -	Email Notifications
## Features at a glance

Quorum Maker v2.0 is an upgrade on v1.0 released by Synechron in October 2017. This upgrade, and future expected upgrades, aim to support application developers in the pursuit of production readiness for the growing number of applications built on top of the Quorum platform. 

| Features | V 1.0 | V 2.0 |
| ------ | ------ |-----|
| Create Network | ![Yes](https://github.com/synechron-finlabs/quorum-maker/blob/master/img/tick.png "Available") | ![Yes](https://github.com/synechron-finlabs/quorum-maker/blob/master/img/tick.png "Available") |
|Join Network | ![No](https://github.com/synechron-finlabs/quorum-maker/blob/master/img/cross.png "Not Available")  | ![Yes](https://github.com/synechron-finlabs/quorum-maker/blob/master/img/tick.png "Available")|
|Delete Nodes	 	  | ![No](https://github.com/synechron-finlabs/quorum-maker/blob/master/img/cross.png "Not Available") | ![WIP](https://github.com/synechron-finlabs/quorum-maker/blob/master/img/wip.png "Work In Progress") |
|Quick Setup with Docker	 	  | ![Yes](https://github.com/synechron-finlabs/quorum-maker/blob/master/img/tick.png "Available") | ![Yes](https://github.com/synechron-finlabs/quorum-maker/blob/master/img/tick.png "Available") |
|Quick network with Docker Compose	 	  | ![Yes](https://github.com/synechron-finlabs/quorum-maker/blob/master/img/tick.png "Available") | ![WIP](https://github.com/synechron-finlabs/quorum-maker/blob/master/img/wip.png "Work In Progress") |
|Quorum Chain Consensus	 	  | ![Yes](https://github.com/synechron-finlabs/quorum-maker/blob/master/img/tick.png "Available") | ![No](https://github.com/synechron-finlabs/quorum-maker/blob/master/img/cross.png "Not Available") |
|Raft Consensus	 	  | ![Yes](https://github.com/synechron-finlabs/quorum-maker/blob/master/img/tick.png "Available") | ![Yes](https://github.com/synechron-finlabs/quorum-maker/blob/master/img/tick.png "Available") |
|Istanbul PBFT Consensus	 	  | ![No](https://github.com/synechron-finlabs/quorum-maker/blob/master/img/cross.png "Not Available") | ![WIP](https://github.com/synechron-finlabs/quorum-maker/blob/master/img/wip.png "Work In Progress") |
|Network Map Service  	 	  | ![No](https://github.com/synechron-finlabs/quorum-maker/blob/master/img/cross.png "Not Available") | ![Yes](https://github.com/synechron-finlabs/quorum-maker/blob/master/img/tick.png "Available") |
|Node Monitoring	 	  | ![No](https://github.com/synechron-finlabs/quorum-maker/blob/master/img/cross.png "Not Available") | ![Yes](https://github.com/synechron-finlabs/quorum-maker/blob/master/img/tick.png "Available") |
|Web UI	 	  | ![No](https://github.com/synechron-finlabs/quorum-maker/blob/master/img/cross.png "Not Available") | ![Yes](https://github.com/synechron-finlabs/quorum-maker/blob/master/img/tick.png "Available") |
|Block Explorer	 	  | ![No](https://github.com/synechron-finlabs/quorum-maker/blob/master/img/cross.png "Not Available") | ![Yes](https://github.com/synechron-finlabs/quorum-maker/blob/master/img/tick.png "Available") |
|Transaction Explorer	 	  | ![No](https://github.com/synechron-finlabs/quorum-maker/blob/master/img/cross.png "Not Available") | ![Yes](https://github.com/synechron-finlabs/quorum-maker/blob/master/img/tick.png "Available") |
|Email Notification	 	  | ![No](https://github.com/synechron-finlabs/quorum-maker/blob/master/img/cross.png "Not Available") | ![Yes](https://github.com/synechron-finlabs/quorum-maker/blob/master/img/tick.png "Available") |
|Restful API	 	  | ![No](https://github.com/synechron-finlabs/quorum-maker/blob/master/img/cross.png "Not Available") | ![Yes](https://github.com/synechron-finlabs/quorum-maker/blob/master/img/tick.png "Available") |
|Smart Contract Deployer	 	  | ![No](https://github.com/synechron-finlabs/quorum-maker/blob/master/img/cross.png "Not Available") | ![Yes](https://github.com/synechron-finlabs/quorum-maker/blob/master/img/tick.png "Available") |

# Quickstart

The first step to use Quorum Maker is to clone the source code from GitHub. 

```
$ git clone git@github.com:synechron-finlabs/quorum-maker.git 
```

Once the repository is successfully cloned, run `setup.sh` script. To minimize the pre-requisites and make setup easy, Quorum Maker uses docker and rest of the dependencies are baked to `syneblock/quorum-maker` image.

## Creating a Network

```
$ cd quorum-maker
$ ./setup.sh
```

After the required docker images are downloaded, Quorum Maker will present with few questions to complete the node setup. 

`Please select an option:`

`1) Create Network`

`2) Join Network`

`3) Remove Node`

`4) Setup Development/Test Network`

`5) Exit`

`option:` 1

`Please enter node name:` Org1

`Please enter IP Address of this node:` 10.0.2.15

`Please enter RPC Port of this node[Default:22000]:`

`Please enter Network Listening Port of this node[Default:22001]:`

`Please enter Constellation Port of this node[Default:22002]:`

`Please enter Raft Port of this node[Default:22003]:`

`Please enter Node Manager Port of this node[Default:22004]:`

This completes the creator node startup procedure. Quorum Maker collects the user provided parameters in order to generate geth and constellation inside the docker container. It also starts the NodeManager service.  and creates a directory with the node name provided. This directory has the script to start the node and other files required. You can stop the node any time using `Ctrl + C`, and restart by running `sudo ./start.sh` from the node directory (Eg. `Org1`). 

![Screenshot 1](https://github.com/synechron-finlabs/quorum-maker/blob/master/img/screenshot1.png) 

## Joining a Network
Once a node is created, you can create and join more nodes to form a Quorum Network. Ideally subsequent nodes should be created on other computers. If you are creating another node on the same computer, please make sure to use different ports. In this case you can use the same Quorum Maker clone, since it creates separate directories for each node.


```
$ cd quorum-maker
$ ./setup.sh
```

After the required docker images are downloaded, Quorum Maker will present users with a few questions to complete the node setup.

`Please select an option:`

`1) Create Network`

`2) Join Network`

`3) Remove Node`

`4) Setup Development/Test Network`

`5) Exit`

`option:` 2

`Please enter node name:` Org2

`Please enter IP Address of existing node:` 10.0.2.15

`Please enter Node Manager Port of existing node:` 22004   

`Please enter IP Address of this node:` 14.0.2.30

`Please enter RPC Port of this node[Default:22000]:`24000

`Please enter Network Listening Port of this node[Default:24001]:`

`Please enter Constellation Port of this node[Default:24002]:`

`Please enter Raft Port of this node[Default:24003]:`

`Please enter Node Manager Port of this node[Default:24004]:`

![Screenshot 2](https://github.com/synechron-finlabs/quorum-maker/blob/master/img/screenshot2.png) 

At this point, a directory with the node name is created and most of the files are created. To join the existing network, the active node requires the Genesis file specific to the network. Quorum Maker will contact the node chose in the wizard and request permission to join and receive the Genesis file. An administrator of that node will get notifications on UI and e-mail for the join request and needs to approve it.

> Note: The joining node will wait 5 minutes for the approval. If the request is not approved within that time, the Quorum Maker will quit. But the administrator of the other node can approve the request any time. Once the request is approved, the node can be restarted by executing `sudo ./start.sh` from the directory created and the setup will be resumed. 

## Approve/Reject Network
-	Once a join request has been sent by a node willing to join a network to one of the existing network participants, this node has the option to approve/reject this join request
-	If the join request is accepted, the main node's constellation port, genesis file and network ID is returned to the joiner. If the join request is rejected, the joiner's setup script exits

![Screenshot 3](https://github.com/synechron-finlabs/quorum-maker/blob/master/img/screenshot3.png) 

## Node Explorer
Quorum Maker provides a web interface to monitor the network. You can explore the blocks getting created and the transactions in them. Node admin can watch the performance of their node and other connected nodes to ensure availability and network resilience.

Administrators can view geth and constellation logs from Quorum Maker. 

![Screenshot 4](https://github.com/synechron-finlabs/quorum-maker/blob/master/img/screenshot4.png) 

Click on the node name of the table to view node details. You can also update the node name and role of your own node. Node name and Role are useful in a large network to identify the peers before sending transactions. Refer to the Quorum Maker API below to access node details using restful clients. 

![Screenshot 6](https://github.com/synechron-finlabs/quorum-maker/blob/master/img/screenshot6.png) 

## Monitoring and Email Notification
1.	There is an active monitoring system which checks whether the node is up every 30 seconds. If it fails to get the expected response which indicates that the node is functional, it waits for another 30 seconds and performs the health check again. If the check fails again then the user is notified
2.	The user is sent an email notification indicating that the node has gone down. The node admin must preconfigure the notification procedure by providing the following details on **Email Server Configuration** menu on UI:
- SMTP Sever Host
- Port
- Username
- Password

## Contract Deployment

Smart contracts can be deployed from Quorum Maker. Users can choose solidity files (Even multiple contracts !) and deploy them publicly  or privately.  

1.	Multiple contracts can be uploaded via the Compile and Deploy Tab
2.	The source .sol files are compiled using solc and subsequently deployed 
3.	The deployment is done either publicly or privately
4.	In case of private deployment the public keys of the concerned parties are sent from the UI
5.	The list of network participants and their corresponding public keys are fetched using a REST API call 
6.	Error messages that occur from compilation failures are also displayed on the UI

All the deployed contracts are easily accessible from the UI in the format contractAddress_contractName and contain the corresponding ABI, Bytecode and JSON

![Screenshot 5](https://github.com/synechron-finlabs/quorum-maker/blob/master/img/screenshot5.png) 

# Node Manager API

Quorum Maker provides APIs that it used internally, that are also useful for application development. Below is a list and explanation of each:

|URI|Method|Description|
|--|--|--|
|/block|GET|This endpoint returns a list of latest n blocks if the query string parameter number is equal to n. If the query string parameter reference is provided with query string parameter number equal to n, then n blocks starting before (reference – 1) is returned|
|/block/{block_no}|GET|This endpoint returns the details of a particular block based on block number|
|/txn |GET |This endpoint returns a list of latest n transactions if the query string parameter number is equal to n|
|/txn/{txn_hash}|GET|This endpoint gets the transaction details of a transaction based on hash. If txn_hash is sent as "pending" it returns a list of all pending transactions|
|/txnsearch/{txn_hash}|GET|This endpoint returns details of a particular transaction based on transaction hash alongside its corresponding block details for displaying the corresponding block information of the queried transaction on UI|
|/latestBlock|GET|This endpoint the latest block number and the difference between present time and the time of creation of the block|
|/peer|GET|This endpoint returns a combination of admin.nodeInfo and certain other details such as current node name, node count, active status, IP, RPC port, raft role, raft ID, blocknumber, pending transaction count as well as the genesis file|
|/peer/{peer_id}|GET|This endpoint returns the information gleaned from admin.peers but filtered by enode-id of a particular peer for displaying the pop up from the node table|
|/nodeList|GET|This endpoint returns the node name, role, public key and enode of all participants in the network by querying the Network Manager contract|
|/pubkeys|GET|This endpoint returns a list of network participants and their corresponding public keys for populating the contract deployment tab's network participants list|
|/deployContract|POST|Multiple contracts can be uploaded via multipart file upload through this endpoint. The source .sol files are compiled using solc and subsequently deployed. The deployment is done either publicly or privately. In case of private deployment the public keys of the concerned parties are sent from UI. The list of network participants and their corresponding public keys are fetched using a REST API call. Error messages that occur from compilation failures are also displayed on UI. All the deployed contracts are easily accessible from the UI in the format|

### Using a different version of Geth/Constellation 
If you need to run Quorum Maker with a different version of Geth or Constellation than comes with default docker image, use [Quorum-Maker-Image](https://github.com/synechron-finlabs/quorum-maker-image "Quorum-Maker-Image"). Create docker image locally and run Quorum Maker again. 

### Work In Progress

We expect the following areas to be part of future upgrades:

 - Support for Istanbul PBFT
 - Support for creating network using docker-compose for development/experimental purpose
 - HTTPS support
 - Password for private keys
