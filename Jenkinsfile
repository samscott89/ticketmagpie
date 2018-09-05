pipeline {
    agent {
        docker {
            image 'maven:3-alpine'
            args '-v $HOME/.m2:/root/.m2'
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'mvn clean install'
            }
        }
        stage('test') {
            steps {
                sh 'mvn sonar:sonar -Dsonar.host.url=http://172.26.0.4:9000'
            }
        }
    }
}
