A Terraform/CX as Code remote module for the following Custom REST API operation: GET 5 top KB articles by category ID

## Usage

Shown below is an example of how to configure the remote module.

```hcl
module "data_action" {
    source             = "git::https://github.com/GenesysCloudDevOps/custom-rest-get-5-top-kb-articles-by-category-id-data-action-module.git?ref=v1.0.0"
    action_name        = "GET 5 top KB articles by category ID"
    action_category    = "${module.integration.integration_name}"
    integration_id     = "${module.integration.integration_id}"
    secure_data_action = false
}
```

`Note:` The remote module for creating this data action integration can be found [here](https://github.com/GenesysCloudDevOps/ "Opens github.com/GenesysCloudDevOps/")

## Requirements

| Name | Version |
|------|---------|
| <a name="provider_terraform"></a>[terraform](https://www.terraform.io/) | >= 1.0 |

## Providers

| Name | Version |
|------|---------|
| <a name="provider_genesyscloud"></a> [genesyscloud](https://registry.terraform.io/providers/MyPureCloud/genesyscloud/latest) | >= 1.0|


## Inputs

| Name | Description | Type | Required |
|------|-------------|------|:--------:|
| <a name="action_name"></a> [action_name](#action\_\name)  | The name for the data action. | `string` | yes |
| <a name="action_category"></a> [action_category](#action\_\category)  | Category of action. | `string` | yes |
| <a name="integration_id"></a> [integration_id](#integration\_\id)  | The ID of the integration this action is associated with. | `string` | yes |
| <a name="secure_data_action"></a> [secure_data_action](#integration\_\id)  | Indication of whether or not the action is designed to accept sensitive data. Defaults to `false`. | `bool` | no |