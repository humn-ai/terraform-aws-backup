## Providers

| Name | Version |
|------|---------|
| aws | ~> 2.0 >= 2.7.0 >= 2.0 |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:-----:|
| backup\_resources | An array of strings that either contain Amazon Resource Names (ARNs) or match patterns of resources to assign to a backup plan | `list(string)` | n/a | yes |
| cold\_storage\_after | Specifies the number of days after creation that a recovery point is moved to cold storage | `number` | n/a | yes |
| completion\_window | The amount of time AWS Backup attempts a backup before canceling the job and returning an error. Must be at least 60 minutes greater than `start_window` | `number` | n/a | yes |
| copy\_action\_cold\_storage\_after | For copy operation, specifies the number of days after creation that a recovery point is moved to cold storage | `number` | n/a | yes |
| copy\_action\_delete\_after | For copy operation, specifies the number of days after creation that a recovery point is deleted. Must be 90 days greater than `copy_action_cold_storage_after` | `number` | n/a | yes |
| delete\_after | Specifies the number of days after creation that a recovery point is deleted. Must be 90 days greater than `cold_storage_after` | `number` | n/a | yes |
| destination\_vault\_arn | An Amazon Resource Name (ARN) that uniquely identifies the destination backup vault for the copied backup | `string` | n/a | yes |
| kms\_key\_arn | The server-side encryption key that is used to protect your backups | `string` | n/a | yes |
| schedule | A CRON expression specifying when AWS Backup initiates a backup job | `string` | n/a | yes |
| start\_window | The amount of time in minutes before beginning a backup. Minimum value is 60 minutes | `number` | n/a | yes |

## Outputs

| Name | Description |
|------|-------------|
| backup\_plan\_arn | Backup Plan ARN |
| backup\_plan\_version | Unique, randomly generated, Unicode, UTF-8 encoded string that serves as the version ID of the backup plan |
| backup\_selection\_id | Backup Selection ID |
| backup\_vault\_arn | Backup Vault ARN |
| backup\_vault\_id | Backup Vault ID |
| backup\_vault\_recovery\_points | Backup Vault recovery points |

