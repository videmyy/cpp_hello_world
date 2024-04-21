
pipeline{
    agent any
    stages{
        stage('Print Info'){
            steps{
                sh 'echo "Branch: HEAD"'
                sh 'echo "Hash: HEAD"'
                sh 'echo "g++ version: g++ (Ubuntu 11.4.0-1ubuntu1~22.04) 11.4.0
Copyright (C) 2021 Free Software Foundation, Inc.
This is free software; see the source for copying conditions.  There is NO
warranty; not even for MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE."'
            }
        }
        stage('Build Executable file'){
            steps{
                // Компилируем main.cpp и сохраняем результат в файл main
                sh 'g++ main.cpp -o main'
            }
        }
        stage('Application Launch Test'){
            steps{
                // Запускаем исполняемый файл main из текущего каталога
                sh './main'
            }
        }
    }
}
