# Build

```bash
export AWS_ACCESS_KEY_ID=[...]

export AWS_SECRET_ACCESS_KEY=[...]

export AWS_DEFAULT_REGION=us-east-1

packer build -machine-readable build-cluster.json | tee build-cluster.log

export AMI_ID=$(grep 'artifact,0,id' build-cluster.log | cut -d: -f2)

```
