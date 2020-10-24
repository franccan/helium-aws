# helium-aws
Run your Helium miner in AWS

CloudFormation template that will deploy a new Helium miner in a ‘t4g’ EC2 instance (uses ARM CPU like RPi), setup logging in AWS CloudWatch Logs and rotate logs locally, create a block height metric in CloudWatch Metrics and backup the private swarm key in Amazon S3 with encryption enabled.

I will write a step by step guide soon. But at a high level there are the steps you would need to follow:

1. Get an AWS account and login making sure you are in the Ireland region (will fix this soon, but it doesn't really matter where the miner is)
2. Get a private key from EC2 (Services / EC2 /Network & Security / Key Pairs)
3. Go to CloudFormation service and select the template available in this repo. You will need the key used in step 2
4. Let the template run (3-5 minutes)
5. Done, you can now ssh to your miner just like the RPi and the service will be running

Once you have setup your miner, you can then forward traffic from your LoRaWan Gateway to the Elastic IP provided in the "outputs" tab
