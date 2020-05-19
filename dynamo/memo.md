# [dynamo](https://www.allthingsdistributed.com/files/amazon-dynamo-sosp2007.pdf)

## targets
- always writable
- a few hundred ms latency

## architectures
### consistent hash
- customized **virtual nodes** applied so that workload can be distributed evenly
- back up data in **3 successor nodes** in the ring clockwise
- **zero-hop DHT**, [see DHT](https://medium.com/@michael.dufel_10220/distributed-hash-tables-and-why-they-are-better-than-blockchain-for-exchanging-health-records-d469534cc2a5)

### vector clock & reconciliation
- [paper we love about vector clock](https://www.youtube.com/watch?v=hK6m6WBk-d8&list=LLse5BXp203aIUsbUPwgfI2w&index=27&t=0s)
- [good examples of vector clock](https://www.youtube.com/watch?v=jD4ECsieFbE&t=103s)
- **"always writable"**, reconcile during read

### sloppy quorum & hinted handoff
- [quorum, R+w>N]()
- [description](https://jimdowney.net/2012/03/05/be-careful-with-sloppy-quorums/)

### Merkle tree (hash tree)
- 

### gossip protocol
- think of [raft consensus protocol](http://thesecretlivesofdata.com/raft/)