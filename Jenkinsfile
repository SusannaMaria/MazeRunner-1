pipeline {
    agent {
        label {
            label ""
            customWorkspace "D:\\_Projects\\MazeRunner\\jenkins_build\\${BRANCH_NAME}"
        }
    }

    stages {
        stage('Stage SayHello') {
            steps {
                echo 'Hello Mazerunner!' 
            }
        }

        stage('Stage Setup') {
            steps {
                echo 'Hello Setup'
                dir ("D:\\_Projects\\MazeRunner\\jenkins_build\\${BRANCH_NAME}\\Framework\\Test") {
                    sh(script: "run_broker_test.bat" , returnStdout: true)
                }
            }
        }
    }
}