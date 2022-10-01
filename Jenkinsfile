pipeline {
    agent { label 'LABEL.PY' }
    stages {
        stage('vcs') {
            steps {
                git url: 'https://github.com/microsoft/python-sample-vscode-flask-tutorial.git', 
                    branch: 'master'
                
            }
        }
        stage('python') {
            steps {
                sh """ python3 -m pip install --upgrade pip setuptools wheel
                       pip install -r requirements.txt
                       pip install pytest pytest-azurepipelines
                       pip install pytest-cov
                    """   
                    
                
            }
        }
    }
}
