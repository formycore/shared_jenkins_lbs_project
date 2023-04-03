@Library ('my-shared-library') _ 
// under the config system, we have mentioned the resusable repo , we have mentioned the 
// name,url and branch paths here
// space and _ are used to pull all the functions 
pipeline {
    agent any 
    stages {
        stage ('Git Checkout'){
            steps {
                    // git 'https://github.com/formycore/shared_jenkins_lbs_project.git'
                    // name of the function is gitCheckout
                    // we have passed 2 variables github branch and url
                    gitCheckout (
                        branch: "master",
                        // url for the java app
                        url: "https://github.com/formycore/shared_jenkins_lbs_project.git"
                    )
                
            }
        }
        stage ('Mvn test'){
            steps {
                mvnTest()
            }
        }
        stage ('Maven Integration Test'){
            steps {
                mvnIntegrationtest()
            }
        }
    }
}