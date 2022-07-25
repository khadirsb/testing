node('master') 
{
    stage('Continuous Download') 
	{
    git 'https://github.com/khadirsb/devops.git'
	}
    stage('Continuous Build') 
	{
    sh label: '', script: 'mvn package'
	}
    stage('Continuous Deployment') 
	{
sh label: '', script: 'scp /home/ubuntu/.jenkins/workspace/job/webapp/target/webapp.war   ubuntu@172.31.46.45:/var/lib/tomcat9/webapps/qaenv.war'
	}
    stage('Continuous Testing') 
	{
              sh label: '', script: 'echo "Testing Passed"'
	}
    stage('Continuous Delivery') 
	{
sh label: '', script: 'scp /home/ubuntu/.jenkins/workspace/job/webapp/target/webapp.war   ubuntu@172.31.46.64:/var/lib/tomcat9/webapps/prodenv.war'
	}
}
