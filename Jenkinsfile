node {
    def mvnHome
    stage('Preparation') { 
        git 'https://github.com/boopathikt/fleetman-position-simulator/'

    }
    stage('Build') {
        
        sh "mvn package"
    }

    stage('Results') {
        junit '**/target/surefire-reports/TEST-*.xml'
        archiveArtifacts 'target/*.jar'
    }
}
