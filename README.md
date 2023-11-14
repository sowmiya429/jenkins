# jenkins
Installation on EC2 Instance
YouTube Video -> https://www.youtube.com/watch?v=zZfhAXfBvVA&list=RDCMUCnnQ3ybuyFdzvgv2Ky5jnAA&index=1

Install Jenkins, configure Docker as agent, set up cicd, deploy applications to k8s and much more.

- GO TO AWS CONSOLE
- Launch Ec2 with UBUNTU AMI
![image](https://github.com/sowmiya429/jenkins/assets/80743760/2afe1e84-ba31-43be-bd31-d9b8ed4b4094)
- connect to EC2 instance connect
  ![image](https://github.com/sowmiya429/jenkins/assets/80743760/fbb23fc8-da06-4b84-ab33-c3b5a7e62135)
  ![image](https://github.com/sowmiya429/jenkins/assets/80743760/6d46e3ee-8092-4d3b-8cf7-119166abd8ef)
To install JENKINS need to install java because jenkins is a java application.
prerequisite:
 -Java (JDK)
### Install Java:
### Run below command
```
sudo apt update
sudo apt install openjdk-11-jre
```
### To verify java installation:
```
java --version
```
![image](https://github.com/sowmiya429/jenkins/assets/80743760/2c63ffc9-6342-472a-906b-90875babf857)
Install jenkins using below command
```curl -fsSL https://pkg.jenkins.io/debian/jenkins.io-2023.key | sudo tee \
  /usr/share/keyrings/jenkins-keyring.asc > /dev/null
echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
  https://pkg.jenkins.io/debian binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null
sudo apt-get update
sudo apt-get install jenkins
```
Install jenkins by using official website
![image](https://github.com/sowmiya429/jenkins/assets/80743760/029a220f-81a6-4a2d-891d-e1c47e3db57f)
###To see in which port the jenkins is running
```
ps -ef | grep jenkins -a
```
Now copy the public IP ADDRESS of the EC2 instance and specify the port 8080 to access the jenkins
```
13.233.138.38:8080
```
![image](https://github.com/sowmiya429/jenkins/assets/80743760/fcd7da2d-4e54-4226-b17d-3bf288b41419)
After you login to Jenkins, - Run the command to copy the Jenkins Admin Password - sudo cat /var/lib/jenkins/secrets/initialAdminPassword - Enter the Administrator password
![image](https://github.com/sowmiya429/jenkins/assets/80743760/73cae487-e4db-4920-b849-b083c69321fd)
![image](https://github.com/sowmiya429/jenkins/assets/80743760/9351e1c7-5243-4823-b288-17916bd549c4)
After that go with Jenkins suggested plugins because it provides the most used plugins.
![image](https://github.com/sowmiya429/jenkins/assets/80743760/3c8da37f-b0ef-4986-aa75-b34e0ed02ba4)
The plugins are getting installed
![image](https://github.com/sowmiya429/jenkins/assets/80743760/105d79a3-fb3a-4f52-99d2-8c400461d265)
###Create First Admin User or Skip the step [If you want to use this Jenkins instance for future use-cases as well, better to create admin user]
![image](https://github.com/sowmiya429/jenkins/assets/80743760/f0f4cd20-5eff-499f-9b08-b63003d0b8b2)
Give all the details for creating admin access
![image](https://github.com/sowmiya429/jenkins/assets/80743760/5ecfe389-e68b-4833-92a0-5ca1e66d317a)
```
password: Sherlock16&
```






