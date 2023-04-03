pipeline {
    agent any 
    stages {
        stage ('Git Checkou'){
            steps {
                script {
                    git 'https://github.com/formycore/shared_jenkins_lbs_project.git'
                }
            }
        }
    }
}