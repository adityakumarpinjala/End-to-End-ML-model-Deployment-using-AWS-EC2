1.go to EC2 in AWS,click on launch instance,acually iam creating a server cloud and we are deploying our model.


2.Create New instance.click launch,Then we need to create a download key pair.Then a pem file(PEM files are used to store SSL certificates and their associated private keys. 
Multiple certificates are in the full SSL chain, and they work in this order: ) will be created(this is a private keyfile where this will interact with the Linux env or whatever)


3.Generate private key with the help of puttygen ,private key is important to interact with AWS EC2


4.Also we need to have WINSCP,where we this can be used to connect to AWS instance


5.Open Winscp,hostname can be got by going to actions in AWS instance,click on connect,then you can select the hostname(Connect to your instance using its Public DNS:)
6.I need to install the libraries ,as most of the libraries were not installed.
7.open putty,give hostname,and again go ssh--authentication,put the private ppk file.
8.login username ubuntu.
9.Type  sudo apt-get update && sudo apt-get install python3-pip    this is for installing pip.
10.go to security groups in the AWS instance--create security group.Destination is (Anywhere)--create it
11.Go to Network interface,select the one,and click change security groups
12.copy the required files into the Required (/home/ubuntu)folder using WINSCP
13.Update the port number i.e 0.0.0.0:8080 in the flask code
14.install necessary libraries by connecting through putty 
15.Python3 app.y
15.Take the web uri from the EC2 instance and verify it.

if __name__== '__main__':
    app.run(host='0.0.0.0', port=8080)


Ref Link:

https://www.youtube.com/watch?v=oOqqwYI60FI
