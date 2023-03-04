pipeline {

	agent{
		label {
			label 'built-in'
			customWorkspace '/mnt/nitin'
			}
		}
	
	stages {
		
			stage ('install'){
				steps {
					sh "rm -rvf *"
					sh "yum install httpd -y"
					}
				}
			
			stage ('service satrt'){
				steps {
					sh "systemctl start httpd "
					sh "chkconfig httpd on"
					}
				}
			
			stage ('deploy'){
				steps {
					sh "echo 'Apache server start' >> /var/www/html/index.html"
					sh "chmod -R 777 /var/www/html"
					}
				}
			
			}
		}
	
