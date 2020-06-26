# #TerraformOnAzure Challenge - episode 2

The second challenge of the [Terraform On Azure](https://github.com/Terraform-On-Azure-Workshop/terraform-azure-hashiconf2020) initiative started when we left on [Challenge 1](https://github.com/Terraform-On-Azure-Workshop/terraform-azure-hashiconf2020/blob/main/challenges/challenge1/Readme.md).
We need to create an Azure SQL DB and a Mongo DB on a container instance to add the database backend to our [forked webapp](https://github.com/OmegaMadLab/AzureEats-Website).  
You can read more about the challenge [here](https://github.com/Terraform-On-Azure-Workshop/terraform-azure-hashiconf2020/blob/main/challenges/challenge2/Readme.md).

I used Terraform to:
- Deploy a resource group
- Deploy an app service plan
- Deploy an app service
- Deploy an Azure SQL DB
- Deploy a Cosmos DB on an Azure Container Instance
- execute an AZ CLI command locally on the Terraform client, to connect the app server to the GitHub repo for continuos deployment

The last step used a local-exec provider, since the app service resource in Terraform doesn't admit continuous deployment configurations at the time of writing.  
You need to previously register Azure as an authorized OAuth consumer on your GitHub account to call the last step successfully. This is a one time activity, and I did it manually.

Executed via VSCode connected to Ubuntu 18.04 WSL.  
Tools used:
+ Terraform v0.12.26
+ provider.azurerm v2.15.0
+ provider.null v2.1.2

My other repos, on for each challenge:
+ [Challenge 1](https://github.com/OmegaMadLab/TerraformOnAzure-Challenge1)
+ [Challenge 3](https://github.com/OmegaMadLab/TerraformOnAzure-Challenge3)
+ [Challenge 4](https://github.com/OmegaMadLab/TerraformOnAzure-Challenge4)
+ [Challenge 5](https://github.com/OmegaMadLab/TerraformOnAzure-Challenge5)