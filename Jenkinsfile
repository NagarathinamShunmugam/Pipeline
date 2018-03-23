
@Library("atJenkinsLib") _
def err_mess
def is_ko=false;
try
{  
  node("master")  
    {    
      stage ("Update Deploy Repository")    
      {      
        err_mess= "SBL000 : Update Deploy Repository"      
        echo "Update Devops repository on master node"    
      }
    }
}
catch(Exception e)    
{      
  echo e.getMessage()      
  is_ko=true      
  err_mess += "-> " + e.getMessage()    
}  
finally
{      
  stage("Final contact DOO") 
  {        
    if ( is_ko == "false") 
    {          
      echo "Updated Devops repository on master node"        
    }      
  }    
}

