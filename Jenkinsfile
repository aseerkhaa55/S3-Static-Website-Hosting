pipeline {
agent any

stages {
stage ('Build') {
steps {
withCredentials([[$class: 'UsernameWithPasswordCredentialsBinding', credentialsId: 'Jenkins-cred', accessKeyVariable: 'AWS_ACCESS_KEY_ID', secretKeyVariable: 'AWS_SECRET_ACCESS_KEY']]) {
sh 'aws s3 cp -r build/ s3://staticwebsitejenkins'
}
}
}
}
}
