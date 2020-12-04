pipeline {

  agent { 
    node { label 'master'} 
  }

  stages{
        stage('FirstStage') {
            steps {
                script{
                    os = sh script: 'cat /etc/os-release', returnStdout:true
                    echo os
                }
            }
        }
        stage('SecondStage'){
            steps {
                script{
                    dns = sh script: 'cat /etc/resolv.conf', returnStdout:true
                    echo dns
                }
            }
        }
        stage('ThirdStage'){
            steps {
                script{
                    logs = sh script: 'cat /var/log/syslog ', returnStdout:true
                    echo logs
                }
            }
        }
  }
}
