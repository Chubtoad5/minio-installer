# minio-installer
Minio container installer for linux based systems

# Core Features

- Automate MinIO pre-requisites (docker, self-signed certificates)
- Automate single-node MinIO container install based on user defined variables
- Loads mc container for local management
- Create a default bucket
- Download files locally and mirror to specified bucket
- Create an offline archive for air-gapped installations
- Support for pushing containers to a local registry
- Support for pulling containers from local registry


# Usage
```
Usage: ./minio-installer [command] [option]

Commands:
  help              | Display this help message
  install           | Install and configure MinIO (Docker Compose)
  save              | Prepare offline archive for air-gapped deployment
  uninstall         | Uninstall MinIO and remove data/config

Options:
  push              | Push MinIO images to a local registry, must include -registry option
  -registry         | Registry credentials for pushing or pulling from local registry (Format: -registry [registry:port username password])

Examples:
  ./minio-installer install
  ./minio-installer save
  ./minio-installer uninstall
  ./minio-installer install -registry myregistry:5000 user password
  ./minio-installer install push -registry myregistry:5000 user password
  ```