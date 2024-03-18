pipeline {
    agent { docker { image 'maven:3.9.6-eclipse-temurin-17-alpine' } }
    stages {
        stage('build') {
            steps {
        nexusPolicyEvaluation iqStage: 'build', iqApplication: 'gitZipTest2',
            iqScanPatterns: [[[scanPattern: '**'], scanPattern: '!.zip/**']],
            failBuildOnNetworkError: true
            }
        }
    }
}
