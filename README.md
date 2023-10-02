# Reusable GitHub Actions workflows
Maintained by Team Plattform.

## Policy check skipped and why

### Postgres module
CKV_GCP_51,CKV_GCP_52,CKV_GCP_53,CKV_GCP_54,CKV_GCP_55,CKV_GCP_56,CKV_GCP_57,CKV_GCP_109,CKV_GCP_111,CKV2_GCP_13,CKV2_GCP_14,CKV2_GCP_15,CKV2_GCP_16,CKV2_GCP_17 - Ensure log_* is set to *: Logging is handled by googles query insight module which is better than postgres logging
CKV_GCP_11 - Ensure network is private: Already handled by vpc not on internet and ssl not public in any way
CKV_GCP_60 - Ensure IP is not public: The IP is not public
CKV_GCP_6 -  Require SSL: already enforced
CKV_K8S_21 - Ensure default namespace not used: Handled by core infra
CKV_K8S_20 - AllowPrivilegeEscalation should be set to false: Not relevant as this is based on a variable in prod
CKV2_GCP_7 - Set password for MySQL instances: Does not account for postgres databases
CKV_TF_1 - Pin modules to commit hash: Not relevant as we tag semantic versions
CKV_GCP_79 - Ensure lates major verision of SQL database: Not possible yet
CKV_GCP_108 - Ensure hostnames logged: Not using hostnames

### module 2

### module 3