node{
  stage 'checkout'
  git url: 'https://github.com/bogo-devops/game-of-life.git'
  def mvnHome = tool M3
  stage 'build'
  sh "${mvnHome}/bin/mvn clean install"
  step([$class: 'JUnitResultArchiver', testResults: '**/target/surefire-reports/TEST-*.xml'])
}
