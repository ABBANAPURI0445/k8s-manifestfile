node {
    stage('SCM') {
     git 'https://github.com/wakaleo/game-of-life.git'
} 
 stage('build-maven') {
    sh 'mvn package'
} 
stage('publish junit reports') {
   junit 'gameoflife-web/target/surefire-reports/*.xml'
}
stage('archive the artifact') {
   archive 'gameoflife-web/target/*.war'
}
}