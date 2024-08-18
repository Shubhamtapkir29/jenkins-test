pipeline{
  agent  {
     label {
             label "built-in"
             customWorkspace "/mnt/git"
              }
          }
 stages {
          stage ( "one" ) {
                        steps {
                                 sh "sudo yum install httpd -y "
                              }
                           }
          stage ("two") {
             steps {
                     sh "service httpd start"
                     sh " sudo chmod -R 777 /var/www/html "
                     sh "sudo cp -r /mnt/git/jenkins-test/index.html   /var/www/html "
                  }
                }
              }
            }
