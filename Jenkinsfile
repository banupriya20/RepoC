pipeline {
    agent any
    stages {
        stage('Parse warnings log') {
            steps {
                bat "python -u C:/ProgramData/Jenkins/.jenkins/workspace/doxygen_parser.py"
            }
        }
        stage('Push artifacts to RepoC') {
            steps {
                dir('C:/ProgramData/Jenkins/.jenkins/workspace/RepoC') {
                    git branch: 'main', credentialsId: 'Githubtoken', url: 'https://github.com/banupriya20/RepoC.git'
                    bat 'git push origin main'
                }
            }
        }
      }
    }
