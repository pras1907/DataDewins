# Aim of the MINI PROJECT:

Create a MakeFile with 4 Targets:
This Makefile helps a PHP development team have a consistent development                 
environment. Fill in the commands for given rules such that conditions                   
provided in comments are met.


# prepare:                                                                                 
 install packages required for following rules                                      
                                                                                     
# up:                                                                                      
 run 'docker compose up'                                                            
 - run one container with MySQL database with persistent storage                    
 -  in ~/docker/db                                                                   
 - run another container apache server with persistent storage                     
 - in ~/docker/www                                                                  
 - apache server should be running with PHP module enabled                          
 - php files stored in ~/docker/www should be live updatable                        
 - create index.php in ~/docker/www, this script                                   
 - connects to MySQL DB and prints MySQL server version                             
 - files in ~/docker/* should be reusable in subsequent runs   


                                                                                  
                                                                                     
# down:                                                                                    
-shut down containers gracefully                                                    
-retain files in ~/docker/* for future 'make up'                                   
                                                                                     
# teardown:                                                                                
-delete ~/docker/* for fresh start                                                  
-implicitly run 'down' rule's commands before teardown                              
-remove all packages installed in prepare steps
