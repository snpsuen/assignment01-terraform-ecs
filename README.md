First and foremost, the Terraform IaC scripts are based on an excellent on-line tutorial by Bradford Lamson-Scribner, https://medium.com/@bradford_hamilton/deploying-containers-on-amazons-ecs-using-fargate-and-terraform-part-2-2e6f6a3a957f, and adapted from the accompanying TF artifacts shared at https://github.com/bradford-hamilton/terraform-ecs-fargate. <br />
<br />
The code automates the tasks of provisoning various AWS resources and deploying the target micro service container, "snpsuen/assign01:node-app01", as a Fargate service on an ECS cluster. The container is confgured to run as a pod of 3 replicas with the cluster scalable automatically from a min of 3 nodes to a max of 6. <br />
<br />
To edit or use the code, copy the entire directory tree of assignment01-terraform-ecs to a local base directory or unzip assignment01-terraform-ecs.zip in there. <br>
cd terraform and check out these tf files. <br />
<br />
variables.tf ---> AWS resource varialble definitions <br />
provider.tf  ---> AWS provider resources <br />
ecs.tf  ---> ECS cluster resources <br />
alb.tf  ---> Application load balancer resources <br />
network.tf  ---> Network resources <br />
security.tf  ---> Security group resources <br />
auto_scaling.tf  ---> Autoscaling resources <br />
logs.tf  ---> CloudWatch logging resources <br />
outputs.tf  ---> DNS output resources <br />
roles.tf  ---> AWS user role resources <br />
version.tf  ---> AWS user role resources <br />
The TF file names are self-explanatory and the scripts are specified with declarative statements to provision the resources concerned. <br />
<br />
After editing the scripts as necessary to align with a given AWS account, run these commands in the assignment01-terraform-ecs directory to set up the ACS infrastructure and services.<br />
terraform init terraform/ <br />
terraform plan terraform/ <br />
terraform apply terraform/ <br />

