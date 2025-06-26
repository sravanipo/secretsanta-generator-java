pipeline {
    agent any
    stages {
        stage('SonarQube Analysis') {
            steps {
                withSonarQubeEnv('sonar') { // Replace 'SonarQube' with your SonarQube server name in Jenkins
                    sh '''
                    sonar-scanner \
                      -Dsonar.projectKey=santa \
                      -Dsonar.sources=. \
                      -Dsonar.host.url=http://44.220.139.204:9000 \
                      -Dsonar.login=6ae82d50b2ee4536319121691e4209c55239c29c
                    '''
                }
            }
        }
    }
}
