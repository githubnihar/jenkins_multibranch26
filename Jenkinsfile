node('master') 
{
    stage('Continuous Download_loans') 
	{
    git 'https://github.com/gitubnihar/jenkins_multibranch26.git'
	}
    stage('Continuous Build_loans') 
	{
    sh label: '', script: 'mvn package'
	}
}
