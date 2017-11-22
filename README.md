# AWS Cryptocurrency Miner 
The AWS Cryptocurrency miner lets you quickly and effortlessly test mining different cryptocurrencies with a variety of EC2 instance types to help you find a profitable combination.  The miner used is an AWS optimized version of xmr-stak (https://github.com/fireice-uk/xmr-stak)

Currently supports mining Monero and Aeon

# Usage

Note: Currently only works in N. Virigina region (US-East-1)

1) Download this git repo locally to your machine
2) Open CloudFormation and click Create Stack
3) Upload a template to Amazon S3 and upload AWSMultiCryptoMiner.template
4) Pick a generic stack name, choose the type of Crypto to mine, instance type you want to mine on, and provide a previously created KeyName
5) Continue through options until you get to create and create the stack 
6) Wait for stack creation to complete, then select the stack in CloudFormation and navigate to the Outputs section
7) Put Hash Report URL into browser to view perfromance of miner (example: <public IP of instance>:16000)
8) When complete, remember to delete stack 
  
 
# Please note: 
This should only be used to test performance of EC2 instance types for various Cryptocurrencies.  The wallet address being mined by this tool is generic and will not generate you profits unless you SSH into the instance and adjust the config.txt file under /xmr-stak/bin with your wallet address.

Example of ouput:
![Alt text](https://gist.githubusercontent.com/fireice-uk/2da301131ac01695ff79539a27b81d68/raw/4c09cdeee86f94df2e9dd86b927e64aded6184f5/xmr-stak-cpu-hashrate.png "Sample Hashrate report from browswer")
