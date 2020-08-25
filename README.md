First and foremost, the Terraform IaC scripts are based on an excellent on-line tutorial by Bradford Lamson-Scribner, https://medium.com/@bradford_hamilton/deploying-containers-on-amazons-ecs-using-fargate-and-terraform-part-2-2e6f6a3a957f, and adapted from the accompanying TF artifacts shared at https://github.com/bradford-hamilton/terraform-ecs-fargate. <br />
The code automates the tasks of provisoning various AWS resources and deploying the targer micro service container as a Fargate service on an ECS cluster. The container is confgured to run as a pod of 3 replicas with the cluster capable of scaling automatically from a min of 3 nodes to a max of 6. <br />
