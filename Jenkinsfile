properties([pipelineTriggers([githubPush()])])
node('linux') {
    git url: 'https://github.com/Nothing2CHere/infrastructure-pipeline.git', branch: 'master'
    stage('Test') {
        sh "env"
    }
}
