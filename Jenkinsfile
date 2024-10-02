pipeline
{

agent any
stages

{ 
    stage ('scm checkout')
    {
        steps{ git 'https://github.com/shubhu34/Ant-WebProject.git' }
    }

    stage ('ant-prepare-target')
    {
        steps { withAnt(installation: 'ANT_HOME', jdk: 'JAVA_HOME') 
        {
          sh 'ant prepare'
        }     }
    }

    stage ('ant-init-target')
    {
        steps 
         { withAnt(installation: 'ANT_HOME', jdk: 'JAVA_HOME') 
           {
               sh 'ant init'
           }  }
    }

}


}