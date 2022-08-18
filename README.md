# Azure-virtual-machine-scale-set-using-Terraform

Azure virtual machine scale sets allow you create and manage a group of load balanced VMs. The number of VM instances can automatically increase or decrease in response to demand or a defined schedule. Scale sets provide the following key benefits:

Easy to create and manage multiple VMs

Provides high availability and application resiliency by distributing VMs across availability zones or fault domains

Allows your application to automatically scale as resource demand changes

With Flexible orchestration, Azure provides a unified experience across the Azure VM ecosystem. Flexible orchestration offers high availability guarantees (up to 1000 VMs) by spreading VMs across fault domains in a region or within an Availability Zone.

Now imagine the following example, we need to create a website with high availability and scalable in Terraform, like the following infrastructure diagram:

Following the official Microsoft documentation the first thing we need is an azure account, If you don't have one, go to this link .

Next, we require Terraform, If you don't have it, go to this link.

Deploy the Terraform demo project located in this repository

Modify with Visual Studio Code terraform.tfvars file, change the values of subscription_id and tenant_id.

Locate the address of the folder where we host the configuration files;

Open the CLI and start terraform with the next command,

terraform init

Use the command validate to check everything is ok,

terraform validate

Our next step is to execute the plan command, terraform will create a JSON file that will contain all the instructions established;

terraform plan

We continue to apply the terraform.tfstate, with the next command,

terraform apply

As a result we have the following infrastructure deployment,

Congratulations, this concludes our demo, you can automate infrastructure deployment with terraform,

In the case we don’t need the virtual machine anymore we can destroy the deployed resources with the following command:

terraform destroy

If you want to know more about terraform or azure check other posts in our blog.

https://gdservices.io/blog/
