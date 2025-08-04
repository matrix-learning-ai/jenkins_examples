pipeline{
    agent{ docker { image'maven:3.9.11-eclipse-temurin-21-alpine'}}
    stages{
        stage('build'){
            steps{
                sh 'echo "Hello World!!"'
                sh 'mvn --version'
                sh '''
                    echo "Multiline shell steps"
                    ls -latr
                '''
                echo "Environment variable Build Id is ${env.BUILD_ID} running on ${env.JENKINS_URL}"
            }
        }
    }
}