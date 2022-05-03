# Optimal-Architecture-From-Build-to-Deploy
Optimal automated cloud hosted architecture from code commit to deployment

![Architecture](https://i.ibb.co/G0JDWJG/Deployment-Strategy-1.png)

## Steps

As first we launch an EC2 or Azure virtual machine image, We only have to setup projects configuration files e.g credenitals/keys of settings files that our app will use to run. We can also create those file with ansibl.

- Repo hosted on Azure/AWS will trigger pipeline when code is pushed/merge in master branch.
- After CI pipeline, artifact are passed to CD pipeline.
- CD pipeline first create directory if not exist to store/run artifact on remote server.
- CD pipeline unzip artifact on remote server and replace configuration present on remote server.
- As UAT/Prod configuration only present on remote os this make it more secure.
- Script to run app e.g .NET/NodeJS script is also presend on configuration file on remote server.

This make deployement automated from code commit to deployement.
