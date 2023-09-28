# data-backup

_the objective of this repository is to find a solution to set up a data backup using minio_

## Proposed solution

### Active-passive replication

[MinioDocumentation](https://min.io/docs/minio/linux/administration/bucket-replication/enable-server-side-one-way-bucket-replication.html)

POC carried out on minio web console :
- Need admin privileges to setup a **replication rule** on a **versioned** bucket
- All bucket content is replicated on second bucket
- Existant objects are replicated
- New objects are replicated
- Deletion is effective on both

Tried to manually rm bucket objects from local machine, objects on replicated bucket were still intact.
POC realized with minimum configuration (encryption disabled)

