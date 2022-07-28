node {
   stage('download') {
   git 'http://github.com/khadirsb/devops.git'
}
stage('build') {
    sh 'mvn package'
}
stage('deploy') {
   sh 'scp /home/ubuntu/.jenkins/workspace/pipeline/webapp/target/webapp.war ubuntu@172.31.44.121:/var/lib/tomcat9/webapps/junaid.war'
}
stage('test') {
    sh 'echo "hello sir"'
}
stage('delivery') {
   sh 'scp /home/ubuntu/.jenkins/workspace/pipeline/webapp/target/webapp.war ubuntu@172.31.45.57:/var/lib/tomcat9/webapps/khadir.war'
}
}
