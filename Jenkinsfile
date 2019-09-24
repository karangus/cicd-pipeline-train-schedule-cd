node  {
    stage('SCM') {
        git 'https://github.com/karangus/cicd-pipeline-train-schedule-cd.git'
    }
    
    stages {
        stage('Build') {
            steps {
                echo 'Running build automation'
                sh './gradlew build --no-daemon'
                archiveArtifacts artifacts: 'dist/trainSchedule.zip'
            }
        }
    }
}
