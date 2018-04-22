pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                echo 'Building..!!'
                echo GIT_URL
                echo repo_url
                echo params.repo_url
                echo env.repo_url
                checkout([$class: 'GitSCM', branches: [[name: '*/master']],
                    doGenerateSubmoduleConfigurations: false, 
                    submoduleCfg: [], 
                    userRemoteConfigs: [[credentialsId: 
                    'aafadd97-6037-457e-9ea5-3f20b7c61e02', 
                    url: env.repo_url]]])
                
                //["git", "clone", repo_url, "C:/Program Files (x86)/Jenkins/workspace/DemoPipeline/"].execute()
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....!!!'
            }
        }
    }
}

