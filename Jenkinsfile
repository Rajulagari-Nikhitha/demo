pipeline {
    agent any
    environment {
        PATH = "C:\\Users\\nikhitha.rajulagari.TL293\\AppData\\Local\\Programs\\Python\\Python312;C:\\Users\\nikhitha.rajulagari.TL293\\AppData\\Local\\Programs\\Python\\Python312\\Scripts;${env.PATH}"
    }
 
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
                bat 'test_cal.py'
            }
        }
    }
 
    post {
        always {
            echo 'Build finished'
        }
    }
}
