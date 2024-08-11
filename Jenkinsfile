pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
        stage("Get Git Repo") {
            steps {
                script {
                    git branch: 'main', url: 'https://github.com/prashantjadhav-ocp/four.git'
                }     
            }
        }
        stage("Docker Build") {
            steps {
                  oc apply -f ./gitops-examples/bgd/
            }
        }
    }
}
