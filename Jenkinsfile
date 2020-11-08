pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'mvn compile'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
        stage('sonar') {
            steps {
                sh 'mvn sonar:sonar -Dsonar.host.url=http://3.139.99.147:9000 -Dsonar.login=925709d27ee4790e4ef8bbe2ce21c5c7213ce8e8'
            }
        }
    }
}
