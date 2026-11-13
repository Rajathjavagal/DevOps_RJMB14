pipeline {
    agent any

    tools {
        maven 'Maven3'
    }

    stages {
        stage('Pull SCM Git') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/Rajathjavagal/DevOps_RJMB14.git'
            }
        }

        stage('Compile') {
            steps {
                sh 'mvn clean compile'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean install'
            }
        }
    }

    post {
        success {
            echo 'Build success!'
        }
        failure {
            echo 'Failure in the build'
        }
    }
}
