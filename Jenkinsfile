pipeline {
    agent any

    stages {
        stage('Clone Repo') {
            steps {
                git branch: 'main', url: 'https://github.com/srinuboori/sampe_repos.git'
            }
        }

        stage('Build') {
            steps {
                echo "Checking Python version..."
                sh 'python3 --version'
            }
        }

        stage('Test') {
            steps {
                echo "Running hello.py..."
                sh 'python3 hello.py'
            }
        }

        stage('Deploy') {
            steps {
                echo "Deployment placeholder..."
            }
        }
    }

    post {
        always {
            echo "Pipeline finished!"
        }
    }
}
