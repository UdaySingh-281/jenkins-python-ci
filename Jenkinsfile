pipeline{
    agent{
        docker{
            image 'python:3.9'
        }
    }

    stages{
        stage('Clone'){
            steps{
                echo 'Cloning Code from repo....'
                checkout scm
            }
        }

        stage('Install dependencies'){
            steps{
                sh 'pip install -r requirements.txt || echo "No dependencies needed"'
            }
        }

        stage('Run tests'){
            steps{
                sh 'python -m unittest discover.'
            }
        }
    }
}