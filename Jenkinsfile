pipeline {
    agent any

    stages {
        stage('PreBuild') {
            steps {
                echo 'This is executing the prebuild steps.....'
                sleep 10
                echo "This is executing another prebuild step..."
                sh("env > variables.txt")
                sh("cat variables.txt")
            }
        }
        stage('Build') {
            steps {
                echo 'Building..'
                sleep 10
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                sleep 10
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
                sleep 10
            }
        }
        stage('PostDeploy') {
            steps {
                echo 'Executing the post-deploy steps'
                sleep 10
                echo "Checking if varibles.txt was preserved..."
                sh("cat variables.txt")
            }
        }
    }
}
