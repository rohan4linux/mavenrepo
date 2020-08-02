pipeline{
agent { label 'dev' }
    stages{
        stage("Checkout"){
          steps{
            checkout([$class: 'GitSCM', 
            branches: [[name: '*/feat01']], 
            userRemoteConfigs: [[credentialsId: '7a4adb71-15e9-418a-ae6b-404307ed026c', url: 'https://github.com/rohan4linux/mavenrepo.git']]
            ])
          } 
        }

        stage("Build"){
          steps{
            sh "mvn package"
          }
        }
     }
}
