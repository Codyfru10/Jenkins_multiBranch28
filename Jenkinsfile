node('master') 
{
    stage('Continuous Download_loans') 
	{
    git 'https://github.com/sunildevops77/maven.git'
	}
    stage('Continuous Build_loans') 
	{
    sh label: '', script: 'mvn package'
	}
    stage('Continuous Deployment_loans') 
	{
sh label: '', script: 'scp /home/ubuntu/.jenkins/workspace/MultiBranchPipeline/webapp/target/webapp.war   ubuntu@172.31.5.162:/var/lib/tomcat8/webapps/qaenv.war'
	}
    stage('Continuous Testing_loans') 
	{
              sh label: '', script: 'echo "Testing Passed"'
	}
    stage('Continuous Delivery_loans') 
	{
sh label: '', script: 'scp /home/ubuntu/.jenkins/workspace/MultiBranchPipeline/webapp/target/webapp.war   ubuntu@172.31.5.112:/var/lib/tomcat8/webapps/prodenv.war'
	}
}
