pipeline {

       agent{

           label "built-in"

         }

       stages { 

          stage('install-apache'){
  
		  steps{	  
                   sh'yum install httpd -y'
		  }
          }

           stage('deploy-index'){
		   steps{
                           sh'cp -r index.html >> /var/www/html'
			   sh 'chmod 777 -R /var/www/html/index.html'
		   }
          }
		  
		  stage('restart apache'){
			  steps {
                           sh'service httpd restart'
			  }
          }


}
}
