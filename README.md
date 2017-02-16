# AzureX
ARM templates to support AzureX project.

## Session 2 Deployment Instructions
### PowerShell
1. Open .\deploymentParameters\virtualNetwork.Parameters.json
2. Replace the IP address in `mgmtSubnetNsgSourceAddressPrefix` with your IP address.
  The ARM template will whitelist this IP address in the *mgmt* subnet to allow SSH connections to the jumpbox (bastion host).
3. Open a PowerShell console.
```PowerShell
# Authenticate to Azure Subscription
Login-AzureRmAccount

# Deploy session 2 ARM templates.
.\Session2-ARM-Templates\Deploy-AzureResourceGroup.ps1 -ResourceGroupLocation westus -UploadArtifacts

```
