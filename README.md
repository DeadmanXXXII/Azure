# Azure

Certainly! Here is a comprehensive list of Azure CLI commands, organized by their functionality.

# Azure CLI Commands

## General Commands

- **Login to Azure:**
  ```bash
  az login
  ```

- **Log out of Azure:**
  ```bash
  az logout
  ```

- **List available subscriptions:**
  ```bash
  az account list
  ```

- **Set a specific subscription:**
  ```bash
  az account set --subscription "Subscription Name or ID"
  ```

- **Get the current subscription:**
  ```bash
  az account show
  ```

- **Get Azure CLI version:**
  ```bash
  az --version
  ```

## Compute

- **List all virtual machines:**
  ```bash
  az vm list --output table
  ```

- **Create a new virtual machine:**
  ```bash
  az vm create --resource-group MyResourceGroup --name MyVM --image UbuntuLTS --admin-username azureuser --generate-ssh-keys
  ```

- **Start a virtual machine:**
  ```bash
  az vm start --resource-group MyResourceGroup --name MyVM
  ```

- **Stop a virtual machine:**
  ```bash
  az vm stop --resource-group MyResourceGroup --name MyVM
  ```

- **Delete a virtual machine:**
  ```bash
  az vm delete --resource-group MyResourceGroup --name MyVM --yes --no-wait
  ```

- **List all VM sizes:**
  ```bash
  az vm list-sizes --location eastus
  ```

## Storage

- **List all storage accounts:**
  ```bash
  az storage account list --output table
  ```

- **Create a new storage account:**
  ```bash
  az storage account create --name mystorageaccount --resource-group MyResourceGroup --location eastus --sku Standard_LRS
  ```

- **Delete a storage account:**
  ```bash
  az storage account delete --name mystorageaccount --resource-group MyResourceGroup --yes
  ```

- **List containers in a storage account:**
  ```bash
  az storage container list --account-name mystorageaccount --output table
  ```

- **Create a new container:**
  ```bash
  az storage container create --name mycontainer --account-name mystorageaccount
  ```

- **Delete a container:**
  ```bash
  az storage container delete --name mycontainer --account-name mystorageaccount
  ```

## Networking

- **List all virtual networks:**
  ```bash
  az network vnet list --output table
  ```

- **Create a new virtual network:**
  ```bash
  az network vnet create --resource-group MyResourceGroup --name MyVNet --address-prefix 10.0.0.0/16
  ```

- **Delete a virtual network:**
  ```bash
  az network vnet delete --resource-group MyResourceGroup --name MyVNet
  ```

- **List all network security groups:**
  ```bash
  az network nsg list --output table
  ```

- **Create a new network security group:**
  ```bash
  az network nsg create --resource-group MyResourceGroup --name MyNSG
  ```

- **Delete a network security group:**
  ```bash
  az network nsg delete --resource-group MyResourceGroup --name MyNSG
  ```

## Resource Management

- **List all resource groups:**
  ```bash
  az group list --output table
  ```

- **Create a new resource group:**
  ```bash
  az group create --name MyResourceGroup --location eastus
  ```

- **Delete a resource group:**
  ```bash
  az group delete --name MyResourceGroup --yes --no-wait
  ```

## SQL Database

- **List all SQL servers:**
  ```bash
  az sql server list --output table
  ```

- **Create a new SQL server:**
  ```bash
  az sql server create --name myserver --resource-group MyResourceGroup --location eastus --admin-user myadmin --admin-password mypassword
  ```

- **Delete a SQL server:**
  ```bash
  az sql server delete --name myserver --resource-group MyResourceGroup --yes
  ```

- **List all databases in a server:**
  ```bash
  az sql db list --server myserver --resource-group MyResourceGroup --output table
  ```

- **Create a new database:**
  ```bash
  az sql db create --resource-group MyResourceGroup --server myserver --name mydatabase --service-objective S0
  ```

- **Delete a database:**
  ```bash
  az sql db delete --resource-group MyResourceGroup --server myserver --name mydatabase --yes
  ```

## App Services

- **List all app services:**
  ```bash
  az webapp list --output table
  ```

- **Create a new app service:**
  ```bash
  az webapp create --resource-group MyResourceGroup --plan MyAppServicePlan --name MyWebApp --runtime "NODE|14-lts"
  ```

- **Delete an app service:**
  ```bash
  az webapp delete --resource-group MyResourceGroup --name MyWebApp
  ```

- **List all app service plans:**
  ```bash
  az appservice plan list --output table
  ```

- **Create a new app service plan:**
  ```bash
  az appservice plan create --name MyAppServicePlan --resource-group MyResourceGroup --sku B1
  ```

- **Delete an app service plan:**
  ```bash
  az appservice plan delete --name MyAppServicePlan --resource-group MyResourceGroup --yes
  ```

## Key Vault

- **List all key vaults:**
  ```bash
  az keyvault list --output table
  ```

- **Create a new key vault:**
  ```bash
  az keyvault create --name MyKeyVault --resource-group MyResourceGroup --location eastus
  ```

- **Delete a key vault:**
  ```bash
  az keyvault delete --name MyKeyVault --resource-group MyResourceGroup
  ```

- **List secrets in a key vault:**
  ```bash
  az keyvault secret list --vault-name MyKeyVault --output table
  ```

- **Set a secret in a key vault:**
  ```bash
  az keyvault secret set --vault-name MyKeyVault --name MySecret --value "MySecretValue"
  ```

- **Get a secret from a key vault:**
  ```bash
  az keyvault secret show --vault-name MyKeyVault --name MySecret
  ```

## Cosmos DB

- **List all Cosmos DB accounts:**
  ```bash
  az cosmosdb list --output table
  ```

- **Create a new Cosmos DB account:**
  ```bash
  az cosmosdb create --name MyCosmosDB --resource-group MyResourceGroup --kind MongoDB
  ```

- **Delete a Cosmos DB account:**
  ```bash
  az cosmosdb delete --name MyCosmosDB --resource-group MyResourceGroup --yes
  ```

## Traffic Manager

- **List all Traffic Manager profiles:**
  ```bash
  az network traffic-manager profile list --output table
  ```

- **Create a new Traffic Manager profile:**
  ```bash
  az network traffic-manager profile create --name MyTrafficManager --resource-group MyResourceGroup --routing-method Priority --unique-dns-name mytrafficmanager
  ```

- **Delete a Traffic Manager profile:**
  ```bash
  az network traffic-manager profile delete --name MyTrafficManager --resource-group MyResourceGroup --yes
  ```

## Azure Kubernetes Service (AKS)

- **List all AKS clusters:**
  ```bash
  az aks list --output table
  ```

- **Create a new AKS cluster:**
  ```bash
  az aks create --resource-group MyResourceGroup --name MyAKSCluster --node-count 1 --enable-addons monitoring --generate-ssh-keys
  ```

- **Delete an AKS cluster:**
  ```bash
  az aks delete --resource-group MyResourceGroup --name MyAKSCluster --yes
  ```

- **Get AKS credentials:**
  ```bash
  az aks get-credentials --resource-group MyResourceGroup --name MyAKSCluster
  ```

This list includes a broad range of Azure CLI commands for managing various Azure resources and services. It should provide a solid foundation for interacting with Azure via the command line.
