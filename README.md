## Deploy the Custom Connector
az login

az account set -s $SUBSCRIPTION_ID

az deployment group create \
  --name DeployLocalTemplate \
  --resource-group $RG_NAME \
  --template-file Connector.json \
  --parameters Connector.parameters.json \
  --verbose
