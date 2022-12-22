pipeline{
    agent{
          label{
               label "slave-2"
              customWorkspace "/mnt/project/"
}
}
        stages{
            stage ("clone repo"){
               steps{
                sh "sudo rm -rf test"
                sh "sudo git clone https://github.com/ajay9922/test.git -b dev"
}
}
        stage ("install httpd"){
          steps{
             sh "sudo yum install httpd -y"
}
}
        stage ("copy file"){
          steps{
            sh "sudo cp -r test/index.html /var/www/html"
            sh "sudo chmod -R 777 /var/www/html/"
}
}
        stage ("service start"){
           steps{
              sh "sudo service httpd start"
}
}

}

}
