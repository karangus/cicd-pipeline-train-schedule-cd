pipeline {
stages {
    stage('SCM') {
        git 'https://github.com/karangus/cicd-pipeline-train-schedule-cd.git'
    }
        stage('Build') {
            steps {
                echo 'Running build automation'
                sh './gradlew build --no-daemon'
                archiveArtifacts artifacts: 'dist/trainSchedule.zip'
            }
        }
    }
}
