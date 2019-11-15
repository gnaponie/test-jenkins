pipeline {
    agent{
        node {
            label 'rcm-tools-jslave-fedora-28'
        }
    }
    
    stages {
        stage('take return 0') {
            steps {
                script {
                    output = sh(returnStatus: true, script: 'python3 returnzero.py')
                    echo "output: ${output}"
                }
            }
        }
        stage('raise exception') {
            steps {
                script {
                    output = sh(returnStatus: true, script: 'python3 raiseerror.py')
                    echo "output: ${output}"
                }
            }
        }
    }
}