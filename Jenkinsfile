pipeline {
    agent any
    stages {
        stage('Install Python') {
            steps {
                echo "Checking if Python is installed.."
                script {
                    def pythonInstalled = sh(returnStatus: true, script: 'python3 --version').toInteger() == 0
                    if (!pythonInstalled) {
                        echo "Python not found, installing.."
                        sh 'sudo apt-get update && sudo apt-get install -y python3'
                    } else {
                        echo "Python is already installed"
                    }
                }
            }
        }
        stage('Build') {
            steps {
                echo "Building.."
                sh '''
                echo "doing build stuff.."
                '''
            }
        }
        stage('Test') {
            steps {
                echo "Testing.."
                sh '''
                echo "doing test stuff.."
                '''
            }
        }
        stage('Deliver') {
            steps {
                echo 'Deliver....'
                sh '''
                echo "doing delivery stuff.."
                '''
            }
        }
    }
}
