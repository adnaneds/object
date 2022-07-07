#!/usr/bin/groovy

@Library(['github.com/indigo-dc/jenkins-pipeline-library@1.4.0']) _

def job_result_url = ''

pipeline {
    agent {
        label 'python3.6'
    }

    environment {
        author_name = "Adnane"
        author_email = "adnane.aitoussayer@etud.univ-angers.fr"
        app_name = "object"
        job_location = "Pipeline-as-code/DEEP-OC-org/DEEP-OC-object/${env.BRANCH_NAME}"
    }

    stages {
        stage('Code fetching') {
            steps {
                checkout scm
            }
        }

        stage("Re-build Docker images") {
            when {
                anyOf {
                   branch 'master'
                   branch 'test'
                   buildingTag()
               }
            }
            steps {
                script {
                    def job_result = JenkinsBuildJob("${env.job_location}")
                    job_result_url = job_result.absoluteUrl
                }
            }
        }



    }
}
