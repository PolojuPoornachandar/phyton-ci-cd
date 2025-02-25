pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/PolojuPoornachandar/phyton-ci-cd.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'pip install -r requirements.txt'
            }
        }

        stage('Run Tests') {
            steps {
                sh 'pytest --disable-warnings'
            }
        }

        stage('Deploy') {
            steps {
                sh 'echo "Deploying application..."'
                sh 'python3 app.py > output.log'
            }
        }
    }
}
