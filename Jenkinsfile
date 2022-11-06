pipeline {
  
  agent{
	label{
		label 'built-in'
		customWorkspace '/mnt/01/'
	}
  }

	stages {
	
		stage ('httpd install') {
		
			steps {
			
			sh''' //yum install httpd -y
				  service httpd start 
				 // chkconfig httpd on 
				  cp index.html /var/www/html/
				  chmod -R 777 /var/*
				  service httpd restart'''
			}
			
			
		}
	}


}
