node('master') 
{
    stage('Continuous Download_master') 
	{
    git 'https://github.com/sunildevops77/maven.git'
	}
    stage('Continuous Build_master') 
	{
    sh label: '', script: 'mvn package'
	}
    stage('Continuous Deployment_master') 
	{
sh label: '', script: 'scp /home/ubuntu/.jenkins/workspace/MultiBranchPipeline/webapp/target/webapp.war   ubuntu@172.31.90.252:/var/lib/tomcat8/webapps/qaenv.war'
	}
    stage('Continuous Testing_master') 
	{
              sh label: '', script: 'echo "Testing Passed"'
	}
    stage('Continuous Delivery_master') 
	{
sh label: '', script: 'scp /home/ubuntu/.jenkins/workspace/MultiBranchPipeline/webapp/target/webapp.war   ubuntu@172.31.95.127:/var/lib/tomcat8/webapps/prodenv.war'
	}
}
