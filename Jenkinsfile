pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/jdufresne12/JenkinsOnAws.git'
            }
        }

        stage('Display README') {
            steps {
                script {
                    def readme = readFile 'README.md'
                    echo readme
                }
            }
        }
    }

    post {
        always {
            echo 'Pipeline execution complete.'
        }
    }
}
