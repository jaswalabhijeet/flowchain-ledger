![](https://raw.githubusercontent.com/flowchain/flowchain.github.io/master/images/logo-text%40128.png)

Private ledger that supports streaming and real-time data flow.

# Introduction

Flowchain is a private blockchain system for the Internet of Things, and it is a device server application for full scale hardware which is from MCU to mainstream servers.

Flowchain leverages the emerging technologies of blockchain, peer-to-peer, web of things, IoT and open IoT cloud.

## Testing

To start a flowchain node:

```
git clone https://github.com/flowchain/flowchain-core.git
cd flowchain-core
npm install
node index.js
```

The server will start at ```localhost:8000``` by default. To start another flowchain node at port ```8001``` and join an existing network:

```
export PORT=8001
node node1.js
```

After ```index.js``` has been joined, its _successor_ will become ```node1.js```. To fix the default join node, please open ```node1.js``` and modify the ```join``` property:

```
server.start({
    onstart: onstart,
	onmessage: onmessage,
	join: {
		address: 'localhost',
		port: 8000
	}
});
```

## Flowchain Modules

* wotcity.io: (https://github.com/wotcity/wotcity-wot-framework)[https://github.com/wotcity/wotcity-wot-framework]
* flowchain: (https://github.com/flowchain/flowchain)[https://github.com/flowchain/flowchain]
* DevifyPlatform: (https://github.com/DevifyPlatform/devify-server)[https://github.com/DevifyPlatform/devify-server]
* node-p2p-chord: (https://github.com/jollen/node-p2p-chord)[https://github.com/jollen/node-p2p-chord]

## History

current:
 * Add PicoDB support

v0.5: 2016.12.28
 * Support transaction verify
 * Update boot node and peer node applications

v0.4: 2016.12.28
 * Bug fixes. ([#62bbfb876f0cca1c4144cc55831a2a5cd42e4f6d])
 * Support leveldb and nedb
 * Add new event: ```ondata```

v0.3: 2016.12.27
 * New difficulty algorithm based on normal distribution
 * Support [IoT broker architecture](https://wotcity.com)
 * Support data query
 * Support failure check

v0.2: 2016.12.26
 * New feature: Save K to successor(K)
 * New feature: event aggregation
 * Support block store based on LevelDB

v0.1: 2016.12.23
 * Ontology: blockchain, IoT, WoT, p2p and IoT hub/gateway.
 * Architecture: REST, RPC

## License

Copyright (C) 2016-present Jollen. The source code is licensed under the MIT license found in the [LICENSE](LICENSE) file.
