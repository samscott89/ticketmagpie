pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'inspec exec https://github.com/dev-sec/cis-docker-benchmark --format junit'
            }
        }
        stage('test') {
            steps {
                // sh 'mvn sonar:sonar -Dsonar.host.url=http://sonarqube:9000 -Dsonar.login=cd8ee2305440df27f74a66c6bb817f5040780ef6'
                sh 'echo 123'
            }
        }
    }
}
