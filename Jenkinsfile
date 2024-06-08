pipeline {
    agent any

    stages {
        stage('Check Disk Space') {
            steps {
                script {
                    // Получение информации о дисках на Linux
                    def diskInfo = sh(script: "df -h", returnStdout: true).trim()
                    
                    // Получение информации о дисках на Windows
                    // def diskInfo = bat(script: "wmic logicaldisk get size,freespace,caption", returnStdout: true).trim()
                    
                    echo "Disk Space Information:\n${diskInfo}"
                }
            }
        }
    }
}
