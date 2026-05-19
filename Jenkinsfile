pipeline {
    agent any
    
    stages {
        stage('System Info') {
            steps {
                script {
                    echo "========== ИНФОРМАЦИЯ О ДИСКАХ =========="
                    sh '''
                        echo "Разделы, размер, использовано, доступно:"
                        df -h
                        
                        echo ""
                        echo "============================================"
                    '''
                }
            }
        }
        
        stage('Top Memory Process') {
            steps {
                script {
                    echo "========== ПРОЦЕСС, ПОТРЕБЛЯЮЩИЙ БОЛЬШЕ ВСЕГО ПАМЯТИ =========="
                    sh '''
                        echo "PID, %MEM, COMMAND:"
                        ps aux --sort=-%mem | head -2 | tail -1
                        
                        echo ""
                        echo "============================================"
                    '''
                }
            }
        }
    }
}
