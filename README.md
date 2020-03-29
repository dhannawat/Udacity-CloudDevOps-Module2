### Dependencies
##### 0. Create zip file with index.html and upload it to s3 bucket. This is inculded in submission as udacity.zip. Ensure that this zip file name is updatedin the `UdagramServers.yml` file.

##### 1. Create Network using following command (using Stack file UdagramNetwork.yml and parameter file network-parameters.json)
aws cloudformation create-stack --stack-name UdagramNetworkCreation --template-body file://UdagramNetwork.yml --parameters file://network-parameters.json --capabilities "CAPABILITY_IAM" "CAPABILITY_NAMED_IAM" --region=us-east-2

##### 1a. Update Network using following command (using Stack file UdagramNetwork.yml and parameter file network-parameters.json)
aws cloudformation update-stack --stack-name UdagramNetworkCreation --template-body file://UdagramNetwork.yml --parameters file://network-parameters.json --capabilities "CAPABILITY_IAM" "CAPABILITY_NAMED_IAM" --region=us-east-2

##### 2. Create Servers using following command (using Stack file UdagramServers.yml)
aws cloudformation create-stack --stack-name UdagramServerCreation --template-body file://UdagramServers.yml --parameters file://server-parameters.json --capabilities "CAPABILITY_IAM" "CAPABILITY_NAMED_IAM" --region=us-east-2

##### 2a. Update Network using following command (using Stack file UdagramNetwork.yml and parameter file network-parameters.json)
aws cloudformation update-stack --stack-name UdagramServerCreation --template-body file://UdagramServers.yml --parameters file://server-parameters.json --capabilities "CAPABILITY_IAM" "CAPABILITY_NAMED_IAM" --region=us-east-2

##### 3. Test out the application
Output parameter was provided. (appending the http) - Copy the `Url of Website` output parameter value out out of the `UdagramServerCreation` stack to test out your application. 



