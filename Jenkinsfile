pipeline {
    agent {
        node {
            label "docker_python_agent"
        }
    }
    triggers {
        pollSCM 'H/2 * * * *'
    }
    stages {
        stage("Build") {
            steps {
                echo "Building..."
                sh '''
                    echo "Doing Some Build Stuff..."
                    ls -la
                    python3 helloworld.py > resultFile.txt
                    ls -la
                    cat resultFile.txt
                    rm -rf resultFile.txt
                    ls -la
                '''
            }
        }
        stage("Test") {
            steps {
                echo "Testing..."
                sh '''
                    echo "Doing Some Test Stuff..."
                '''
            }
        }
        stage("Delivery") {
            steps {
                echo "Delivering..."
                sh '''
                    echo "Doing Some Delivery Stuff..."
                '''
            }
        }
    }
}