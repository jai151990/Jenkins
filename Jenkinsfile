pipeline {
   agent { label 'pipe' }
        stages {
           stage ('checkout'){
                 steps {
                       checkout scm }
                  }
             stage ('build'){
                  steps {
                       sh 'mvn install'}
                  }
             stage ('definescript'){
                  steps {
                       sh 'cp target/student.war /home/siva/soft/apache-tomcat-8.5.32/webapps'}
                  steps {
                       sh 'export JAVA_HOME=/home/siva/soft/jdk1.8.0_171/bin ;/home/siva/soft/apache-tomcat-8.5.32/bin/startup.sh'}
                  }
               }
         }
