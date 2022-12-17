"Publish Azure Kubernetes Service using an ARM Template"

Using these templates, Azure Kubernetes Service can be deployed.

Running the deployment:

->To deploy a template, sign in to either the Azure CLI or Azure PowerShell

     az login
     
->Create a resource group

     az group create --name resourceGroupName --location "<location>"
     
->Deploy template

     az deployment group create --resource-group $resourceGroupName --template-file <PATH-TO-aks.JSON> --parameters <PATH-TO-aks.JSON> 
     
    
A Kubernetes manifest file: "azure-vote.yaml" defines a cluster's desired state, such as which container images to run.

This manifest includes two Kubernetes deployments:

          The sample Azure Vote Python applications.
          A Redis instance.
          
Two Kubernetes Services are also created:

          An internal service for the Redis instance.
          An external service to access the Azure Vote application from the internet.

  
 
