## EC2 hibernation needs:
- enable hibernation & hibernation prereqs

### When instances are started
1. EBS root volume is restored to its prev state
2. RAM contents are reloaded
3. proceses that were previously runing are resumed
4. previously attached data volume are reattached

### charges
- not charged for this instance usage when it is stopped or data transfer.
- charged for storage of EBS & RAM

## System Manager(SSM)
- To use: 'AWS resource" or AWS agent installed in on-prem server

## RDS Proxy
- Connection reuse
- Can integrate with secret manager
- IAM authentication
- use cases: connection pooling, improve read performance

## Aurora
- copy data in 1s
- can read data from second region
- RPO in 1s, RTo in 1m
- use cases: DR, global low latency read, improve availability