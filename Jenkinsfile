node('master') 
{
    stage('continuous download') 
{
    
git 'https://github.com/tramu139/maven.git'

}

stage('continuous build')
 {
   
 sh label: '', script: 'mvn package'

}

stage('continuous deployement')
 {

sh label: '', script: 'scp /home/ubuntu/.jenkins/workspace/mba/webapp/target/webapp.war ubuntu@172.31.29.181:/var/lib/tomcat8/webapps/ramu.war'
	
}
   
stage('continous testing')
 {
   
 
sh label: '', script: 'echo "testing is passerd"'

}


stage('continous delivery')
 {
   
 
sh label: '', script: 'scp /home/ubuntu/.jenkins/workspace/mba/webapp/target/webapp.war ubuntu@172.31.20.61:/var/lib/tomcat8/webapps/ramu.war'

}





 
}



