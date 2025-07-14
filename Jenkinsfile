pipeline{
    agent any

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