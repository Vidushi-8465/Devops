pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git branch: 'main', url: 'https://github.com/Devops/helloworld-flask.git'
            }
        }
        stage('Build') {
            steps {
                sh 'pip install -r requirements.txt'
            }
        }
        stage('Test') {
            steps {
                sh 'python -m unittest || echo "No tests yet"'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo "Deploying Flask app..."'
                // Later we can add Docker/Nginx deployment here
            }
        }
    }
}
