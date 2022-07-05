pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
        stage ('checkout') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/cbabu85/maven_project.git']]])
            }
        }
        stage('Build') {
            steps {
                echo 'Maven Hello'
            }
        }
    }
}
