pipeline{
    agent any

    tools {
         maven 'Maven3'
         jdk 'Java21'
    }

    stages{
        stage('checkout'){
            steps{
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: 'github', url: 'https://github.com/chprasannaawscloudarch/java-hello-world-with-maven.git']]])
            }
        }
        stage('build'){
            steps{
               bat 'mvn package'
            }
        }
    }
}
