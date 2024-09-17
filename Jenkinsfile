pipeline{
    agent any
    
    stages{
        stage("Code checkout"){
            steps{
               git branch: 'main', url: 'https://github.com/Brainy016/dockerapp.git'
                
            }
        }
        stage("Image build"){
            steps{
                sh "docker image build -t @brainy016/devapp:$BUILD_ID ."
                sh "docker image tag @brainy016/devapp:$BUILD_ID @brainy016/devapp:latest "
            }
        }
    }
}