pipeline {                            // 1  // Defines the start of the Jenkins pipeline block
    agent any                         // Specifies the pipeline can run on any available agent  
    stages {                          // 2  // Defines the stages block where multiple stages are declared
        stage('Stage 1') {            // 3  // Creates a stage named 'Stage 1'
            steps {                   // 4  // Defines the steps that will be executed in this stage
                echo 'Hello world!'   // Prints 'Hello world!' in the console output
            }                         // 4  // Ends the steps block
        }                             // 3  // Ends the stage block
    }                                 // 2  // Ends the stages block
}                                     // 1  // Ends the pipeline block




PipelineJob2

pipeline {                            // 1  // Defines the start of the Jenkins pipeline block
    agent any                         // Specifies the pipeline can run on any available agent

    stages {                          // 2  // Defines the stages block where multiple stages are declared
        stage('Build') {              // 3  // Creates a stage named 'Build'
            steps {                   // 4  // Defines the steps that will be executed in this stage
                echo 'Building..'     // Prints 'Building..' in the console output
            }                         // 4  // Ends the steps block for 'Build' stage
        }                             // 3  // Ends the 'Build' stage

        stage('Test') {               // 5  // Creates a stage named 'Test'
            steps {                   // 6  // Defines the steps that will be executed in this stage
                echo 'Testing..'      // Prints 'Testing..' in the console output
            }                         // 6  // Ends the steps block for 'Test' stage
        }                             // 5  // Ends the 'Test' stage

        stage('Deploy') {             // 7  // Creates a stage named 'Deploy'
            steps {                   // 8  // Defines the steps that will be executed in this stage
                echo 'Deploying....'  // Prints 'Deploying....' in the console output
            }                         // 8  // Ends the steps block for 'Deploy' stage
        }                             // 7  // Ends the 'Deploy' stage
    }                                 // 2  // Ends the stages block
}                                     // 1  // Ends the pipeline block



PipelineJob3

pipeline {                            // 1  // Defines the start of the Jenkins pipeline block
    agent any                         // Specifies the pipeline can run on any available agent

    stages {                          // 2  // Defines the stages block where multiple stages are declared
        stage('Build') {              // 3  // Creates a stage named 'Build'
            steps {                   // 4  // Defines the steps that will be executed in this stage
                sh 'date'             // Executes the shell command to print the current date
                sh 'pwd'              // Executes the shell command to print the current working directory
            }                         // 4  // Ends the steps block for 'Build' stage
        }                             // 3  // Ends the 'Build' stage

        stage('Test') {               // 5  // Creates a stage named 'Test'
            steps {                   // 6  // Defines the steps that will be executed in this stage
                echo 'Testing..'      // Prints 'Testing..' in the console output
            }                         // 6  // Ends the steps block for 'Test' stage
        }                             // 5  // Ends the 'Test' stage

        stage('Deploy') {             // 7  // Creates a stage named 'Deploy'
            steps {                   // 8  // Defines the steps that will be executed in this stage
                echo 'Deploying....'  // Prints 'Deploying....' in the console output
            }                         // 8  // Ends the steps block for 'Deploy' stage
        }                             // 7  // Ends the 'Deploy' stage
    }                                 // 2  // Ends the stages block
}                                     // 1  // Ends the pipeline block



PipelineJob4

pipeline {                            // 1  // Defines the start of the Jenkins pipeline block
    agent any                         // Specifies the pipeline can run on any available agent
    stages {                          // 2  // Defines the stages block where multiple stages are declared
        stage('Stage 1') {            // 3  // Creates a stage named 'Stage 1'
            steps {                   // 4  // Defines the steps that will be executed in this stage
                sh '''                // Starts a multi-line shell block
                ls                    // Lists the files in the current directory
                date                  // Prints the current date
                cal 2021              // Displays the calendar for the year 2021
                '''                   // Ends the multi-line shell block
            }                         // 4  // Ends the steps block for 'Stage 1'
        }                             // 3  // Ends the 'Stage 1' stage
    }                                 // 2  // Ends the stages block
}                                     // 1  // Ends the pipeline block


PipelineJob6



pipeline {                                    // 1  // Defines the start of the Jenkins pipeline block
    agent any                                 // Specifies the pipeline can run on any available agent
    environment {                             // 2  // Defines environment variables for the pipeline
        PATH = "/opt/maven/bin:$PATH"         // Adds Maven's path to the system's PATH variable
    }                                         // 2  // Ends the environment block
    stages {                                  // 3  // Defines the stages block where multiple stages are declared
        stage('git clone') {                  // 4  // Creates a stage named 'git clone'
            steps {                           // 5  // Defines the steps that will be executed in this stage
                git url: 'https://github.com/SaiDevOpsFaculty/war-web-project.git', branch: 'master'  
                                              // Clones the specified GitHub repository from the master branch
            }                                 // 5  // Ends the steps block for 'git clone' stage
        }                                     // 4  // Ends the 'git clone' stage

        stage('build') {                      // 6  // Creates a stage named 'build'
            steps {                           // 7  // Defines the steps that will be executed in this stage
                sh 'mvn clean install'        // Runs the Maven clean install command to build the project
            }                                 // 7  // Ends the steps block for 'build' stage
        }                                     // 6  // Ends the 'build' stage
    }                                         // 3  // Ends the stages block
}                                             // 1  // Ends the pipeline block
