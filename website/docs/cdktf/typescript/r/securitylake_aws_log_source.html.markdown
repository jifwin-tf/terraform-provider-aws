---
subcategory: "Security Lake"
layout: "aws"
page_title: "AWS: aws_securitylake_aws_log_source"
description: |-
  Terraform resource for managing an Amazon Security Lake AWS Log Source.
---


<!-- Please do not edit this file, it is generated. -->
# Resource: aws_securitylake_aws_log_source

Terraform resource for managing an Amazon Security Lake AWS Log Source.

## Example Usage

### Basic Usage

```typescript
// DO NOT EDIT. Code generated by 'cdktf convert' - Please report bugs at https://cdk.tf/bug
import { Construct } from "constructs";
import { TerraformStack } from "cdktf";
/*
 * Provider bindings are generated by running `cdktf get`.
 * See https://cdk.tf/provider-generation for more details.
 */
import { SecuritylakeAwsLogSource } from "./.gen/providers/aws/";
class MyConvertedCode extends TerraformStack {
  constructor(scope: Construct, name: string) {
    super(scope, name);
    new SecuritylakeAwsLogSource(this, "test", {
      source: [
        {
          accounts: ["123456789012"],
          regions: ["eu-west-1"],
          source_name: "ROUTE53",
          source_version: "1.0",
        },
      ],
    });
  }
}

```

## Argument Reference

The following arguments are required:

* `source` - (Required) Specify the natively-supported AWS service to add as a source in Security Lake.

`source` supports the following:

* `accounts` - (Optional) Specify the AWS account information where you want to enable Security Lake.
* `regions` - (Required) Specify the Regions where you want to enable Security Lake.
* `sourceName` - (Required) The name for a AWS source. This must be a Regionally unique value. Valid values: `ROUTE53`, `VPC_FLOW`, `SH_FINDINGS`, `CLOUD_TRAIL_MGMT`, `LAMBDA_EXECUTION`, `S3_DATA`.
* `sourceVersion` - (Optional) The version for a AWS source. This must be a Regionally unique value.

## Attribute Reference

This resource exports no additional attributes.

## Import

In Terraform v1.5.0 and later, use an [`import` block](https://developer.hashicorp.com/terraform/language/import) to import AWS log sources using the source name. For example:

```typescript
// DO NOT EDIT. Code generated by 'cdktf convert' - Please report bugs at https://cdk.tf/bug
import { Construct } from "constructs";
import { TerraformStack } from "cdktf";
class MyConvertedCode extends TerraformStack {
  constructor(scope: Construct, name: string) {
    super(scope, name);
  }
}

```

Using `terraform import`, import AWS log sources using the source name. For example:

```console
% terraform import aws_securitylake_aws_log_source.example ROUTE53
```

<!-- cache-key: cdktf-0.20.0 input-ee1a170608deb904f09e1ba901701686ec29394191b588406f73bc8dadef1e52 -->