# Reusable GitHub Actions workflows
Maintained by Team Plattform.

## Policy check skipped and why

### Postgres module

| CKV Rule | Description | Status | Reason|
| --- | --- | --- | --- |
| CKV_GCP_52 | Ensure network is private | Skipped | Already handled by vpc not on internet and ssl not public in any way |
| CKV_GCP_53 | Ensure IP is not public | Skipped | The IP is not public |
| CKV_GCP_54 | Require SSL | Skipped | Already enforced |
| CKV_GCP_55 | Ensure default namespace not used | Skipped | Handled by core infra |
| CKV_GCP_56 | AllowPrivilegeEscalation should be set to false | Skipped | Not relevant as this is based on a variable in prod |
| CKV_GCP_57 | Set password for MySQL instances | Skipped | Does not account for postgres databases |
| CKV_TF_1 | Pin modules to commit hash | Skipped | Not relevant as we tag semantic versions |
| CKV_GCP_79 | Ensure latest major version of SQL database | Skipped | Not possible yet |
| CKV_GCP_108 | Ensure hostnames logged | Skipped | Not using hostnames |
| CKV_GCP_51, CKV_GCP_52, CKV_GCP_53, CKV_GCP_54, CKV_GCP_55, CKV_GCP_56, CKV_GCP_57, CKV_GCP_109, CKV_GCP_111, CKV2_GCP_13, CKV2_GCP_14, CKV2_GCP_15, CKV2_GCP_16, CKV2_GCP_17 | Ensure log_* is set to * | Skipped | Logging is handled by googles query insight module which is better than postgres logging |
| CKV_AZURE_136 | Ensure Azure PostgreSQL Flexible Server enables geo-redundant backups | Skipped | Using global disaster recovery backup |
| CKV_AZURE_128 | Ensure PostgreSQL server enables Threat Detection policy | Skipped | Non-Flexible DB type will be deprecated |
| CKV_AZURE_130 | Ensure PostgreSQL server enables infrastructure encryption | Skipped | This property is currently still in development and not supported by Microsoft. |

### module 2

### module 3
