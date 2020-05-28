# dotnetwebapp Blank App

az cli commands

```
gitrepourl=$(git config --get remote.origin.url)
azlocation=westus2
azgroupname=azgroup$RANDOM
azappname=azwebapp#RANDOM

az group create --location $azlocation -n $azgroupname

az appservice plan create -n $azappname -g $azgroupname --sku free

az webapp create -n $azappname -g $azgroupname --plan $azappname

az webapp deployment source config -n $azappname -g $azgroupname --repo-url $gitrepourl --branch master --manual-integration
```
