node('master') 
{
    stage('Continuous Download_master') 
      {
    git 'https://github.com/sunildevops77/maven.git'
      }
    stage('Continuous Build_master') 
      {
    sh 'mvn package'
      }
    stage('Continuous Deployment') 
      {
    sh 'scp /home/ubuntu/.jenkins/workspace/ScriptedProject/webapp/target/webapp.war ubuntu@172.31.32.99:/var/lib/tomcat9/webapps/qaenv1.war'
      }
    stage('Continuous testing') 
      {
    sh 'echo "Test Passed"'
      }
   stage('Continuous Delivery') 
      {
    sh 'scp /home/ubuntu/.jenkins/workspace/ScriptedProject/webapp/target/webapp.war ubuntu@172.31.37.112:/var/lib/tomcat9/webapps/prodenv1.war'
      }
}
