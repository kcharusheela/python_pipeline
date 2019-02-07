node {
   stage('Checkout Code') {
      git 'https://github.com/kcharusheela/python_pipeline.git'
   }
   stage('Unit Test') {
      // run the unit tests
      dir("python_pipeline") {
	 sh "pwd"
         sh "virtualenv .env"
         sh ". .env/bin/activate"
	 sh "pwd"
	 sh "sudo su -"
	 sh "sudo find / -name requirements.txt"
         sh "pip install -r requirements.txt"
         sh "python -m pytest tests/test_app.py"
      }
   }
}
