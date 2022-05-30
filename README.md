# JOSI-AUTO-LLC

# Apache Maven Installation And Setup In AWS EC2 Redhat Instnace.

Prerequisite

* AWS Acccount.
* Create Redhat EC2 T2.medium Instnace with 4GB of RAM.
* Create Security Group and open Required ports 22 ..etc
* Attach Security Group to EC2 Instance.
* Install java openJDK 1.8+

# Install Java JDK 1.8+ and other softares (GIT, wget and tree)

# install Java JDK 1.8+ as a pre-requisit for maven to run.

sudo hostname maven
cd /opt
sudo yum install wget nano tree unzip git-all -y
sudo yum install java-11-openjdk-devel java-1.8.0-openjdk-devel -y
java -version
git --version
