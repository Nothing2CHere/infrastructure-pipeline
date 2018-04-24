properties([pipelineTriggers([githubPush()])])
node('linux') {
    git url: 'https://github.com/Nothing2CHere/infrastructure-pipeline.git', branch: 'master'
    stage('Test') {
        sh "env"
    }
    stage ("GetInstances") {
        sh "aws ec2 describe-instances --region us-east-1"
    }
    stage ("CreateInstance") {
         sh "aws ec2 run-instances --image-id ami-6735fd1a --count 1 --instance-type t2.micro --key-name Dan665-1 --security-group-ids sg-6d8cf424 --subnet-id subnet-6f56b333 --region us-east-1"
    }
}

