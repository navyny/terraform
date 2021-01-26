# terraform for Azure

## Install powershell module "Az" Windows

```
PS C:\> Install-Module Az
```
You should not install Az side-by-side with AzureRM. Remove all AzureRM modules before installing Az.
"AzureRM" was reaplced by "Az"

Typing az -h will show you the extensions available to be used.

## Login to Azure
```
PS C:\WINDOWS\system32> az login
Note, we have launched a browser for you to login. For old experience with device code, use "az login --use-device-code"
```

Once we login on browser..this will list all the Subscriptions I have access to.

## To see a list of all Subscriptons/Accounts

```
$ az account list
```
The output (similar to below) will display one or more Subscriptions - with the id field being the subscription_id field referenced above.

```
[
  {
    "cloudName": "AzureCloud",
    "id": "00000000-0000-0000-0000-000000000000",
    "isDefault": true,
    "name": "PAYG Subscription",
    "state": "Enabled",
    "tenantId": "00000000-0000-0000-0000-000000000000",
    "user": {
      "name": "user@example.com",
      "type": "user"
    }
  }
]
```

Subscriptions:

NZ-DEV
NZ-TEST
NZ-PROD

NZ-CORE

NZ-SBOX-IT-SUB-01
NETSCOUT Sandbox

NZ-DEV-ENGOPS-SUB-01

Origin and File Services - Production

Should you have more than one Subscription, you can specify the Subscription to use via the following command:
```
$ az account set --subscription="SUBSCRIPTION_ID"
```


#### Installing a package manager on Windows 10:
```
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))
```

### Installing Terraform uisng the Chocolatey Package Manager:
```
choco install terraform -y
```

