# cloudlast
aws configure

curl --silent --location "https://github.com/eksctl-io/eksctl/releases/latest/download/eksctl_$(uname -s)_amd64.tar.gz" | tar xz -C /tmp

sudo mv /tmp/eksctl /usr/local/bin

sudo yum install -y kubectl

eksctl create cluster \

--name eks-cluster-1 \

--region us-east-1 \

--nodegroup-name eks-nodes1 \

--node-type t3.medium \

--nodes 1 \

--nodes-min 1 \

--nodes-max 2 \

--managed

================machine===================

sudo apt update

snap install kubectl --classic

sudo apt install unzip curl -y

# 2. Download the AWS CLI v2  installer

curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"

# 3. Unzip the  installer

unzip awscliv2.zip

# 4. Run the  installer

sudo ./aws/install

# 5. Verify the installation

aws --version

aws configure

aws eks update-kubeconfig --region us-east-1 --name MyEKSCluster
