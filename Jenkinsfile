node {
    stage('scm') {
      git 'https://github.com/itsmedineshk/game-of-life.git'
 }
    stage('build&Package') {
        sh label: '', script: 'mvn package'
    }
    stage('results') {
        archiveArtifacts 'gameoflife-web/target/gameoflife.war'
        junit 'gameoflife-web/target/surefire-reports/*.xml'
    }
}
