pipeline {

       agent any {

           label "built-in"

         }

       stages { 

          stage('install-apache'){

               sh'yum install httpd -y'

          }

           stage('deploy-index'){

               sh'cp -r index.html >> /var/www/html'
			   sh 'chmod 777 -R /var/www/html/index.html'

          }
		  
		  stage('restart apache'){

               sh'service httpd restart'

          }


}
}
