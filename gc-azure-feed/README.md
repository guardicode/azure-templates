# GcAzureFeed infra template

Allows to deploy Azure infrastructure needed for Guardicore integration application.

### Deploy infra via Azure portal

[![Deploy to Azure](https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/1-CONTRIBUTION-GUIDE/images/deploytoazure.svg?sanitize=true)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fguardicode%2Fazure-templates%2Fmaster%2Fgc-azure-feed%2fazuredeploy.json)


### Deploy infra via AZ CLI

1. Download/install AZ CLI
   Make sure you are able to login to your Azure subscription

2. Download ARM template: 
   `curl https://raw.githubusercontent.com/guardicode/azure-templates/master/gc-azure-feed/azuredeploy.json -o azuredeploy.json`

3. Set `TargetUrl` within `azuredeploy.json`

4. Create Azure ResourceGroup and deploy infra
  - `az group create --location eastus --name GcGroup`
  - `az deployment group create --resource-group GcGroup  --template-file azuredeploy.json`
