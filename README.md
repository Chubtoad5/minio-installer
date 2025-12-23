# minio-installer
Minio container installer for linux based systems


# Usage

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
  $0 install
  $0 save
  $0 uninstall
  $0 install -registry myregistry:5000 user password
  $0 install push -registry myregistry:5000 user password