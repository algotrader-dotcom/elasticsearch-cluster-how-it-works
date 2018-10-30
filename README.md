# elasticsearch-cluster-how-it-works
![](https://www.elastic.co/assets/blt47da469cfb3097c3/cluster-topology.svg)

## Questions will be solved
- [] How a node in cluster talks to others?
- [] What happens when a node joins or leaves the cluster?
- [] What happens when a node stops or has encountered a problem?
- [] What is the role of master/client/data in cluster ?
- [] What is memory requirement for each node ?

## What is a cluster of nodes ? 
- Start a ES instance => a cluster of single node.
- Start another ES instance with the same `cluster.name` => a cluster of 2 nodes.
- How nodes talk to each other: `over TCP`
- How nodes talk to external: `JSON over HTTP`
- Each node can play one or more roles in cluster.

## What is role of master/client/data ?
### Master
- Create/Delete `indices`
- Add/Remove `nodes` from cluster
- Broadcast changes to other nodes
- Only 1 master node at a time.

### Data
- Holding `data` in the shards => CRUD, search, aggregations on `data`

### Client
- Routing requests to master/data => `smart router`

## Adding a node to cluster
## Removing a node to cluster
# References:
- https://medium.com/@duy.do/how-elasticsearch-cluster-works-97d537071b87
- https://medium.com/google-cloud/a-guide-to-deploy-elasticsearch-cluster-on-google-kubernetes-engine-52f67743ee98
- https://www.slideshare.net/PetarDjekic/elasticsearch-101-cluster-setup-and-tuning
