node {
   stage('Preparation') {
       git 'https://github.com/SGDemoAccount/Code'
   }
   stage('CodeAnalysis'){
       //Just Find there are some java files and print the names of them
       sh "/bin/find . -name *.java"

   }
   stage('Clean') {
         sh "/bin/mvn -f sample-app/pom.xml -Dmaven.test.failure.ignore clean"

   }
   stage('Build') {
         sh "/bin/mvn -f sample-app/pom.xml -Dmaven.test.failure.ignore  package"
   }
   stage('Test') {
         sh "/bin/mvn -f sample-app/pom.xml -Dmaven.test.failure.ignore  test"
   }
   stage('Deploy') {
         sh "/bin/mvn -f sample-app/pom.xml -Dmaven.test.failure.ignore  install"
   }
}
