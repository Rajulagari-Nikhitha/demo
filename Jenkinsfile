pipeline {
    agent any
 
    stages {
        stage('Clone Repository') {
            steps {
                git url: 'https://github.com/Rajulagari-Nikhitha/demo.git', branch: 'main'
            }
        }
 
        stage('Verify Python Installation') {
            steps {
                bat 'python --version'
            }
        }
 
        stage('Install Dependencies') {
            steps {
                bat 'python -m pip install --upgrade pip'
                bat 'python -m pip install pytest'
            }
        }
 
        stage('Run Tests') {
            steps {
                bat 'test.py'
            }
        }
    }
 
    post {
        always {
            echo 'Build finished'
        }
    }
}