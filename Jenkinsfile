pipeline {
  agent any
    stages{
      stage ('install nginx'){
        steps{
            sh 'sudo apt install nginx -y'          
        }
      }
      stage ('delete default page'){
        steps{
            sh 'sudo rm -rf /var/www/html/*'          
        }
      }
      stage ('hosting'){
        steps{
            sh 'sudo cp -rf ecomm/* /var/www/html/'          
        }
      }
      stage ('restart nginx'){
        steps{
            sh 'sudo systemctl restart nginx'          
        }
      }
    }  
}
