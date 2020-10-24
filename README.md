# helium-aws
Run your Helium miner in AWS

CloudFormation template that will deploy a new Helium miner in a ‘t4g’ EC2 instance (uses ARM CPU like RPi), setup logging in AWS CloudWatch Logs and rotate logs locally, create a block height metric in CloudWatch Metrics and backup the private swarm key in Amazon S3 with encryption enabled.

Once you have setup your miner, you can then forward traffic from your LoRaWan Gateway to the Elastic IP provided in the "outputs" tab
