node('master') 
{
    stage('Remove project content') 
	{
    	sh label: '', script: 'rm -rf /var/lib/jenkins/workspace/HTML-Project/*'
	}
    stage('Remove html root') 
	{
    	sh label: '', script: 'rm -rf /var/www/html/*'
	}
    stage('Download') 
	{
    	git branch: 'master', url: 'https://github.com/UjjalKrRoy/Tours-and-Travels.git'
	}
    stage('Deployment') 
	{
    	sh label: '', script: 'cp -r /var/lib/jenkins/workspace/HTML-Project/* /var/www/html/'
	}
    stage('Restart web service') 
	{
    	sh label: '', script: 'sudo systemctl restart httpd'
	}
}