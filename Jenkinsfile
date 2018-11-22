node {
    withEnv(['GOPATH=/home/glva/.jenkins/workspace/Hello Go Pipeline']) {
        dir('src') {
            dir('github.com/golang/example/') {
                checkout scm
                dir('hello') {
                    sh 'go build'
                    archiveArtifacts artifacts: 'hello', fingerprint: true
                }
            }
        }
    }
}
