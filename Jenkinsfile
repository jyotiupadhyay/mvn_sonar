pipeline
{ 
      agent any
      stages{ 
 stage ('git checkout SCM')
      { 
            steps{
            git 'https://github.com/jyotiupadhyay/mvn_sonar'
      }
      }
 stage ('Analysis')
    {     steps {
                sh '/opt/maven/bin/mvn clean verify sonar:sonar'
                }
     }
  stage ('Build')
    {     steps  {
                  sh '/opt/maven/bin/mvn clean install'
                 }
    }
  stage ('Deploy')
  {     steps   {
                  echo "Deployed"
                  }
   }
}
}
