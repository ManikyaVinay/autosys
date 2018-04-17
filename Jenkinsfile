pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                echo 'my parameter for git repo url is: ${repo_url}'
                echo 'my parameter for git repo url is: env.repo_url'
                echo 'repo_url: ${env.repo_url}'
                echo 'repo_url1: ${params.repo_url}'
                echo env.repo_url
                checkout([$class: 'GitSCM', branches: [[name: '*/master']],
                    doGenerateSubmoduleConfigurations: false, 
                    submoduleCfg: [], 
                    userRemoteConfigs: [[credentialsId: 
                    'aafadd97-6037-457e-9ea5-3f20b7c61e02', 
                    url: env.repo_url]]])
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}

