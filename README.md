# Learn Hashicorp Vault from Scratch

## 1. Download Vault CLI using Homebrew (Tested on MacOS)
```
brew tap hashicorp/tap
brew install hashicorp/tap/vault
```

Verify Vault CLI installation
```
vault --version
```

## 2. Start the Vault server on local machine and store Vault server address to env var
```
vault server -dev
export VAULT_ADDR='http://127.0.0.1:8200'
```
* note: do not run above command for production! only for development purpose

## 3. Creating vault secrets
```
vault kv put secret/firs_secret password=admin123
```
* note: by default we're only have the permission to write secret inside **secret/** folder, if you want to use another directory, we would cover later on chapter Vault Policy