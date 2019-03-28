# Quick Start: AWS CloudFormation Template for Rubrik CloudCluster

Walkthrough for commpleting the AWS configuration process required for deploying a 4-node Rubrik CloudCluster.

The end-to-end workflow is as follows:

* Specify AWS Deployment Variables
* Specify CloudCluster Configuration Variables
* Specify CloudCluster Bootstrap Variables

![Template Design](/docs/img/rubrik_cloudcluster-designer.png)

# CloudFormation Stack
------------------

Navigate to **Services** > **CloudFormation** > **Stacks** and select **Create Stack**. 

![Create a Stack](/docs/img/image1.png)

Either select **Upload a template to Amazon S3** or, preferably, **Specify an Amazon S3 template URL**. 

![Select Template](/docs/img/image2.png)

The template file can be downloaded [here](https://s3-us-west-1.amazonaws.com/cloudformation-templates-rubrik-prod/rubrik_cloudcluster.template). Alternatively, copy the following URL:

```
https://s3-us-west-1.amazonaws.com/cloudformation-templates-rubrik-prod/rubrik_cloudcluster.template
```

On the **Specify Details** page, enter the **Stack name** and the **Parameters**. 

Under **AWS Deployment**, you will need to define the following: 

 * ImageID
 * Availability Zone
 * SubnetId
 * SecurityGroupIds

![Specify Details](/docs/img/image3.png)

Under **Cloud Cluster Version and Size**, you will need to define the following: 

 * RubrikCDMVersion
 * RubrikCDMSize

 Under **Cloud Cluster Boostrap Parameters**, you will need to define the following: 

 * SubnetNetmask
 * SubnetGateway
 * NTPServer
 * DNSNameServer
 * AdminEMailAddress
 * AdminPassword

Press **Next** through the **Options** page. 

Use the **Review** page to ensure all the information is correct. Press **Create** once reviewed.

Follow the Rubrik CDM User Guide to complete the setup once bootstrap has finished. 
