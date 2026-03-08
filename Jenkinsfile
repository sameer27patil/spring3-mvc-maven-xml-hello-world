@Library("jmsdevops@main") _

pipeline {
    agent any

    stages {

        stage('Push Maven ECR Repo') {
            steps {
                pushMavenEcrRepo(
                    ecrRepoName: 'spring3-mvc-maven-xml-hello-world'
                )
            }
        }

        stage('Push ECR Repo') {
            steps {
                pushEcrRepo(
                    ecrRepoName: 'spring3-mvc-maven-xml-hello-world_shared_lib'
                )
            }
        }

    }
}
