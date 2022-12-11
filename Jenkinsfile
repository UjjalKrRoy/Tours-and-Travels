node('master') 
{
    stage('Remove project content') 
	{
    	sh label: '', script: 'rm -rf /var/lib/jenkins/workspace/WebProject_master/*'
	}
    stage('Remove html root') 
	{
    	sh label: '', script: 'rm -rf /var/www/html/*'
	}
    stage('Download') 
	{
    	git 'https://github.com/UjjalKrRoy/Tours-and-Travels.git'
	}
    stage('Deployment') 
	{
    	sh label: '', script: 'cp -r /var/lib/jenkins/workspace/WebProject_master/* /var/www/html/'
	}
    stage('Restart web service') 
	{
    	sh label: '', script: 'sudo systemctl restart httpd'
	}
}