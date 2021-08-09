Azure CLI (cloud shell)


```
git clone https://github.com/Azure-Samples/html-docs-hello-world.git
cd html-docs-hello-world
az webapp up --location westus --name [your_name] --html
http://[your_name].azurewebsites.net
az group delete --name [resource_group_name]
```
