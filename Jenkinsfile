

pipeline {
  
  agent any
  
  stages {
    
    stage("checkout_and_catch") {
      parallel {
        stage("checkout") {
          steps {
            echo 'checkout the code start...!'
            delay(10)
            echo 'checkout the code end...!'  
          }
        }
        stage("catch_abort") {
          steps {
            echo 'catch_abort start...!'
            delay(10)
            echo 'catch_abort end...!'  
          }    
        }
      }
      
    }
    
    
    stage("build") {
    
      steps {
        echo 'build the code...!'  
      }
      
    }
    
    
    stage("deploy") {
    
      steps {
        echo 'deploy the code...!'  
      }
      
    }
    
  }
  
}



def delay(num) {
    for (int i = 0; i < num; i++) {
        sleep(time:1,unit:"SECONDS")
    }
}
