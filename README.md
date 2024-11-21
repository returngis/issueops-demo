# IssueOps Demo

## Create an application registration in Microsoft Entra ID

In order to use Terraform to create a service principal, you need to have an application registration in Microsoft Entra ID. You can create one by following the steps below:

```bash
az ad sp create-for-rbac --name "issueOps" --role contributor --scopes /subscriptions/$(az account show --query id -o tsv)
```