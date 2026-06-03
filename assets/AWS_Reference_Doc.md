# AWS Regions Cheat Sheet-Wk1

## AWS Region Table
| Region Name | Region Code | AZ Count | Key Services Available | Notes |
|:--:|:--:|:--:|:--:|:--:|
| US East (N. Virginia) | us-east-1 | 6 | EC2, S3, Lambda, RDS, Aurora, etc. (largest set) | Most services; default in AWS console |
| US West (Oregon) | us-west-2 | 4 | Same core services as us-east-1 | Popular for cost and green energy |
| Europe (Ireland) | eu-west-1 | 3 | Full set -- often used for EU compliance | Lowest latency in Europe |
| Africa (Cape Town) | af-south-1 | 3 | Core: EC2, EBS, S3, VPC, Lambda (limited vs us-east-1) | Best for South and West/Central Africa (incl. Nigeria) |
| Asia Pacific (Singapore) | ap-southeast-1 | 3 | Full core + services for fintech/gaming | Good for SE Asia |
| South America (São Paulo) | sa-east-1 | 3 | EC2, S3, RDS, etc. (some latency) | Only region in South America |

*\*NB: There is expected to be a new Geographic Region in South America (Chile)*

## Key Facts to Remember:

- **Service availability differs by Region** so it's best practice to check which services are available for use when carrying out operations and can also help mitigate certain costs.

- **Availability Zones (AZs) are physically separate**. There's a minimum of 3 AZs per region (older regions like us-east-1 have more unlike af-south-1 which has only 3). AZ count changes as AWS expands with new AZs or Regions.

- **Data transfer costs:** Moving data out of a region to the internet or another region costs money; moving data between AZs inside the same region is cheaper but not free.

## Nigeria Context:

- **Latency to af-south-1:** According to Google search, there's an 80-100ms latency from Lagos, Nigeria to af-south-1. From my experience with online multiplayers, it can range from 70ms -130ms (60ms with Fibre Optics connections)

- **Data sovereignty:** There's no AWS region physically present in Nigeria. For legal requirements to keep data in-country, you may need third-party partners or local cloud providers. Cape Town is the closest.

- **Edge Locations near Nigeria** -- There is one in Lagos, Nigeria (for CloudFront & Route 53). It speeds up content delivery(delivery optimization) but does not host EC2 or S3.

## Bonus - Latency Test:

- Latency to af-south-1: *461 ms*

- Latency to us-east-1: *1025 ms*

**Values according to https://cloudpingtest.com/aws**
