# aws-eb
AWS Elastic Beanstalk CloudFormation

## Create S3 content bucket
* upload CloudFormation template `templates/eb-content.yaml`
* choose unique S3 bucket name, e.g. `eb-content-7897y456ty8`
* this will create S3 content bucket for Elastic Beanstalk
* disable block public access
* disable bucket owner enforced
* upload `eb-content/content.zip`
* allow public read to object

## Create ElasticBeanstalk environment
* upload CloudFormation template `templates/eb-vpc.yml`
* Enter a stack name, must be alphanumeric e.g. `ElasticBeankstalkStack`
* Enter the Bucket Name created earlier for content, e.g. `eb-content-7897y456ty8`
* Enter domain prefix, must be alphanumeric, e.g. `MyWebApplication777`
* Press Next twice, agree to the warning and Submit
* This will create an Elastic Beanstalk in a VPC running a demo app
