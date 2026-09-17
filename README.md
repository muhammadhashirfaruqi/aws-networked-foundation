# AWS Networked Foundation (Project 1)

Project 1 of my hands-on AWS cloud engineering learning track. I build each
piece in the console first, understand *why* it works, then document it here.

**End goal:** transition into a Cloud / Cloud-Ops Engineering role.

## What this project covers
Building the core network layer that real applications sit on — the same
foundations I work with on a production UK energy programme:

- S3 (object storage fundamentals)
- VPC (public/private subnets across availability zones)
- Internet Gateway, route tables, NAT
- Security Groups vs NACLs
- EC2 placement (public and private subnets, bastion access)

## Sub-projects
| # | Sub-project | Status |
|---|-------------|--------|
| 1.1 | S3 basics — private, encrypted bucket + object | ✅ Done |
| 1.2 | Custom VPC — public + private subnets | ⏳ Next |
| 1.3 | Internet Gateway + route tables | ⬜ |
| 1.4 | Security Groups vs NACLs | ⬜ |
| 1.5 | EC2 in public subnet | ⬜ |
| 1.6 | EC2 in private subnet (via bastion/NAT) | ⬜ |

## Approach
Console-first → CLI → IaC (SAM, then Terraform). Depth over breadth:
each setting is learned when there's a real reason to use it.

## Region
All resources in `us-east-1`.
