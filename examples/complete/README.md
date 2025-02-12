# Complete AWS Global Accelerator Example

Configuration in this directory creates:

- A standard Global Accelerator
- Multiple listeners
- An endpoint group for one of the listeners with multiple endpoints

## Usage

To run this example you need to execute:

```bash
$ terraform init
$ terraform plan
$ terraform apply
```

Note that this example may create resources which will incur monetary charges on your AWS bill. Run `terraform destroy` when you no longer need these resources.

<!-- BEGINNING OF PRE-COMMIT-TERRAFORM DOCS HOOK -->
## Requirements

| Name | Version |
|------|---------|
| <a name="requirement_terraform"></a> [terraform](#requirement\_terraform) | >= 1.0 |
| <a name="requirement_aws"></a> [aws](#requirement\_aws) | >= 4.35 |

## Providers

| Name | Version |
|------|---------|
| <a name="provider_aws"></a> [aws](#provider\_aws) | >= 4.35 |

## Modules

| Name | Source | Version |
|------|--------|---------|
| <a name="module_alb"></a> [alb](#module\_alb) | terraform-aws-modules/alb/aws | ~> 7.0 |
| <a name="module_global_accelerator"></a> [global\_accelerator](#module\_global\_accelerator) | ../.. | n/a |
| <a name="module_global_accelerator_disabled"></a> [global\_accelerator\_disabled](#module\_global\_accelerator\_disabled) | ../.. | n/a |
| <a name="module_s3_log_bucket"></a> [s3\_log\_bucket](#module\_s3\_log\_bucket) | terraform-aws-modules/s3-bucket/aws | ~> 3.0 |
| <a name="module_vpc"></a> [vpc](#module\_vpc) | terraform-aws-modules/vpc/aws | ~> 5.0 |

## Resources

| Name | Type |
|------|------|
| [aws_caller_identity.current](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/data-sources/caller_identity) | data source |

## Inputs

No inputs.

## Outputs

| Name | Description |
|------|-------------|
| <a name="output_dns_name"></a> [dns\_name](#output\_dns\_name) | The DNS name of the accelerator |
| <a name="output_endpoint_groups"></a> [endpoint\_groups](#output\_endpoint\_groups) | Map of endpoints created and their associated attributes |
| <a name="output_hosted_zone_id"></a> [hosted\_zone\_id](#output\_hosted\_zone\_id) | The Global Accelerator Route 53 zone ID that can be used to route an Alias Resource Record Set to the Global Accelerator |
| <a name="output_id"></a> [id](#output\_id) | The Amazon Resource Name (ARN) of the accelerator |
| <a name="output_ip_sets"></a> [ip\_sets](#output\_ip\_sets) | IP address set associated with the accelerator |
| <a name="output_listeners"></a> [listeners](#output\_listeners) | Map of listeners created and their associated attributes |
<!-- END OF PRE-COMMIT-TERRAFORM DOCS HOOK -->

Apache-2.0 Licensed. See [LICENSE](https://github.com/terraform-aws-modules/terraform-aws-global-accelerator/blob/master/LICENSE).
