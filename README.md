 <h1>Terraform AWS</h1>

This is a Terraform Project that builds a solution on AWS. 

<h2>Terraform AWS Project: Multi-Region Infrastructure</h2>
This Terraform project sets up infrastructure in two different AWS regions: Project 1 and Project 2. It includes modules for creating EC2 instances, DynamoDB tables, S3 buckets, VPCs, and subnets. In the latest commit, we added VPC endpoints to enhance security and connectivity.

<h2>Table of contents</h2>

- Installation
- Usage
- Contributing

<h3>Installation</h3>
Provide clear instructions on how to install and set up your project. Include any prerequisites or dependencies. For example:

<h4>Prerequisites</h4>

Before you begin, ensure you have the following installed:

- Terraform
- AWS CLI
  
<h4>Getting Started</h4>

Clone this repository:

`git clone https://github.com/Mahfouz98/terraform_aws_project`

Navigate to the project directory:

`cd terraform-aws-project/project1`

Initialize Terraform:

`terraform init`

Customize your variables in `variables.tf`.

Deploy the infrastructure:

`terraform apply`

<h3>Usage</h3>

This is a screen after `terraform apply` which is creating the resources.

![Screenshot from 2024-03-11 01-16-57](https://github.com/Mahfouz98/terraform_aws_project/assets/145352617/f3dbc489-e037-4bf5-874e-1329fff94f5f)


<h4>Adding VPC Endpoints</h4>

We’ve recently added VPC endpoints to improve security and reduce data transfer costs. To enable VPC endpoints, update your `main.tf` of project2.
its ready to go in project1.

```
module "endpoint" {
  source = "../modules/vpc_endpoints"
  
  vpc_id         = module.network.vpc_id
  route_table_id = module.network.route_table_id
  region         = var.region
}
```

<h2>Contributing</h2>
Great projects are built by a community of passionate individuals. Your contribution matters! 🌟

Please feel free to contribute to the project. and add some improvements. I am still learning.

<h4>How to Contribute</h4>

- Fork this repository.
- Create a new branch: git checkout -b feature/my-feature
- Make your changes and commit: git commit -m "Add new feature"
- Push to your fork: git push origin feature/my-feature
- Submit a pull request.

