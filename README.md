### Dependencies
##### 0. Create zip file with index.html and upload it to s3 bucket. This is inculded in submission as udacity.zip

##### 1. Create Network using following command (using Stack file UdagramNetwork.yml and parameter file network-parameters.json)
aws cloudformation create-stack --stack-name UdagramNetworkCreation --template-body file://UdagramNetwork.yml --parameters file://network-parameters.json --capabilities "CAPABILITY_IAM" "CAPABILITY_NAMED_IAM" --region=us-east-2

##### 1a. Update Network using following command (using Stack file UdagramNetwork.yml and parameter file network-parameters.json)
aws cloudformation update-stack --stack-name UdagramNetworkCreation --template-body file://UdagramNetwork.yml --parameters file://network-parameters.json --capabilities "CAPABILITY_IAM" "CAPABILITY_NAMED_IAM" --region=us-east-2

##### 2. Create Servers using following command (using Stack file UdagramServers.yml)
aws cloudformation create-stack --stack-name UdagramServerCreation --template-body file://UdagramServers.yml --parameters file://server-parameters.json --capabilities "CAPABILITY_IAM" "CAPABILITY_NAMED_IAM" --region=us-east-2

##### 2a. Update Network using following command (using Stack file UdagramNetwork.yml and parameter file network-parameters.json)
aws cloudformation update-stack --stack-name UdagramServerCreation --template-body file://UdagramServers.yml --parameters file://server-parameters.json --capabilities "CAPABILITY_IAM" "CAPABILITY_NAMED_IAM" --region=us-east-2

##### 3. Test out the application
Output parameter was provided. (appending the http) - To test out go to http://Udagr-WebAp-1EPM4BSG5RC4P-2006087772.us-east-2.elb.amazonaws.com



