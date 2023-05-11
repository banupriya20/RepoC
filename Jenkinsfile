pipeline {
    agent any
    stages {
        stage('Parse warnings log') {
            steps {
                bat "python -u C:/ProgramData/Jenkins/.jenkins/workspace/doxygen_parser.py"
            }
        }
