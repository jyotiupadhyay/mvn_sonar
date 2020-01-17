node('master')
{ stage ('git checkout SCM')
      { git 'https://github.com/jyotiupadhyay/mvn_sonar'
      }
 stage ('Analysis')
    {     step {
                sh '/opt/maven/bin/mvn clean verify sonar:sonar'
                }
     }
  stage ('Build')
    {     step  {
                  sh '/opt/maven/bin/mvn clean install'
                 }
    }
  stage ('Deploy')
  {     step    {
                  echo "Deployed"
                  }
   }
}
