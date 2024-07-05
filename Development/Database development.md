
### DynamoDB
#### AWS DynamoDB Accelerator(DAX)
		- Is a fully managed, highly available, in-memory cache for Amazon DynamoDB that delivers up to a 10x performance improvement, from milliseconds to microseconds, even at millions of requests per second. A DAX cluster is a collection of individual DAX nodes, each of which maintains a copy of your DynamoDB table data.
##### Key features:
			- Caching layer: in memory caching layer infront of DynamoDB tables.
			- High availability: as configured in multiple nodes in multiple availability zones.
			- Scalability: DAX clusters can scale out by adding more nodes to the cluster to handle increasing load.
			- Write-through cache: DAX also synchronizes the cache with updated data.
			- Read replicas
##### Components
			- Nodes, endpoints, subnet groups, parameters groups, security groups




