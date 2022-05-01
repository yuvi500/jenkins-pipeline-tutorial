# jenkins-pipeline-tutorial
Jenkins Pipeline Tutorial



# webhook
ngrok http 8080
webhook create
webhook ngrok http link paste /github-webhook/
webhook applicaton json
build triggers : github hook trigger for gitscm polling
pipeline: defn: pipeline script from scm
scm git
repo url
script path: hello-world/Jenkinsfile
build manually once
FInally update github repo


4.
make java file
build execute windows batch command
D:
cd D:\joBhiHai
javac ulala.java
java ulala 



make java file for parameters
This project is parameterized
string1
string2

class StringArguments
{
    public static void main(String args[])
    {
        System.out.println("My name is "+args[0]);
        System.out.println("My surname is "+args[1]);
    }
}

build execute windows batch command
D:
cd D:\joBhiHai
javac ulala.java
java ulala %string1% %string2%



5.
for parameters code
echo "Your name is %str1%"
echo "Your Surname is %str2%"
echo "Your Favorite City is %city%"
echo "Are you a student %student%"


3.
git init
git clone url
cd 
git remote add origin url
git config --global user.name "your_username"
git config --global user.email "your_email_address@example.com"
git pull
git push
git fetch 
git status
git merge


8.
pipeline {
  agent any
  stages {
    stage('Form') {
      input {
        message "Please fill this form"
        parameters {
          string(name: 'PERSON', defaultValue: '', description: 'Your Name: ')
          booleanParam(name: 'STUDENT', defaultValue: true, description: 'Student')
          choice(name: 'DIVISION', choices: ['A', 'B'], description: 'Pick division')
          text(name: 'PID', defaultValue: '', description: 'Enter your PID')
        }
      }
      steps {
        echo "Hello, ${params.PERSON}"
        echo "Toggle: ${params.TOGGLE}"
        echo "Choice: ${params.CHOICE}"
        echo "PID: ${params.PID}"
      }
    }
    stage('info') {
            steps {
                echo 'This was your information'
            }
        }
    stage('Bye') {
            steps {
                echo 'Bye'
            }
        }
  }
  post {
    failure {
      echo 'The build was unsuccessful, try again later.'
    }
  }
}


20 commands of linux
compgen -c
