pipeline {
    agent any
    
    stages  {
        stage ('Compile Stage')     {
            steps   {
                withMaven(maven : 'maven3.5.0')  {
                    sh 'clean install'
                    }
                }
            }
            stage ('Testing Stage') {
                steps{
                        withMaven(maven : 'maven3.5.0') {
                            sh 'mvn clean install'
                        }
                    }
            }
            stage ('Deployement Stage') {
                steps   {
                    withMaven(maven : 'maven3.5.0')  {
                    sh 'mvn deploy'
                    }
                }
            }    
        }
    }    
