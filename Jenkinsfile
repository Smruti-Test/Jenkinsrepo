pipeline {
  agent any
    stages {
        stage('build') {
            steps {
                echo 'build ...'
                sleep 5
            }
        }
        stage('test') {
            steps {
                echo 'test ..'
            }
        }
        stage('Deploy for development') {
            steps {
              snDevOpsChange()
              echo 'Deploy for development ...'
              sleep 5
              snDevOpsArtifact(artifactsPayload:"""{"artifacts": [{"name": "development_artifact.jar","version": "1.18","semanticVersion": "1.8.0","repositoryName": "Jenkinsrepo"}],"stageName": "Deploy for development"}""")
            }
        }
    }
}
