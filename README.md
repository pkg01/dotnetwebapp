# dotnetwebapp Blank App

az cli commands

```
azgroupname=azgroup$RANDOM
azappname=azwebapp#RANDOM

az group create --location westus2 -n $azgroupname

az appservice plan create -n $azappname -g $azgroupname --sku free

az webapp create -n $azappname -g $azgroupname --plan $azappname

az webapp deployment source config -n $azappname -g $azgroupname --repo-url https://github.com/pkg01/dotnetwebapp.git --branch master --manual-integration
```
