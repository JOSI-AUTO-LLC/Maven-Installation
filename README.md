# Apache Maven Installation And Setup In AWS EC2 Redhat Instnace.This is a step by step process. OR run the install_maven.sh script to intall maven together with java,nano,vim,tree and wget.

Prerequisite

* AWS Acccount.
* Create Redhat EC2 T2.medium Instnace with 4GB of RAM.
* Create Security Group and open Required ports 22 ..etc
* Attach Security Group to EC2 Instance.
* Install java openJDK 1.8+

# 1. Install Java JDK 1.8+ and other softares (GIT, wget and tree)

#install Java JDK 1.8+ as a pre-requisit for maven to run.

sudo hostname maven

cd /opt

sudo yum install wget nano tree unzip git-all -y

sudo yum install java-11-openjdk-devel java-1.8.0-openjdk-devel -y

java -version

git --version

# 2. Download, extract and Install Maven

#Step1) Download the Maven Software

sudo wget https://dlcdn.apache.org/maven/maven-3/3.8.5/binaries/apache-maven-3.8.5-bin.zip

sudo unzip apache-maven-3.8.5-bin.zip

sudo rm -rf apache-maven-3.8.5-bin.zip

sudo mv apache-maven-3.8.5/ maven

# 3. Set Environmental Variable - For Specific User eg ec2-user

vi ~/.bash_profile  # and add the lines below

export M2_HOME=/opt/maven

export PATH=$PATH:$M2_HOME/bin

# 4. Refresh the profile file and Verify if maven is running

source ~/.bash_profile

mvn -version
