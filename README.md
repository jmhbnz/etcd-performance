# Qualifying etcd performance


## Background

The etcd project currently has a number of mechanisms for measuring the performance of etcd, however these are:
- Not run frequently on consistent hardware
- Not well documented or understood
- Not regularly maintained

This repository overhauls the existing efforts, reusing as much as possible to produce a framework that can effectively democratize and regularly qualify the performance of etcd.

## Scalability dimensions

The performance and scalability of an etcd cluster is not a simple topic, and is not limited to a single variable. There are a number of critical variables which influence how an etcd cluster will perform. Moving forward, these variables will be referred to as "scalability dimensions".

The initial scalability dimensions used are listed below, however these will be expanded once the initial framework is in place:

1. Cluster size - The number of members in the etcd cluster.
2. Key size - The size of the keys stored.
3. Value size - The size of values stored in each key.
4. Operation type - What type of key operation is being performed.
5. Operation count - How many requests of the operation are performed.

