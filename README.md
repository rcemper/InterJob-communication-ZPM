 ~~~
 This is a coding example working on IRIS 2020.2 and on Caché 2018.1.3 
 It will not be kept in sync with new versions      
 It is also NOT serviced by InterSystems Support !   
~~~ 

Earlier I've written about command pipes.  
This is the internal variant of a PIPE.  
  
To make this more tangible and visible for you I prepared a small example  
       
The scenario is to run a monitoring process that receives  
input from an unknown number of sensors. 
(Could be Lab equipment or similar.)  
       
The monitor should not poll his sensors nor run  
in a hang loop to scan a common global  
and work independently of any disk access.  
   
To try it log into a terminal     
.    DO ##class(IJC.Demo).%Start()        
The Highlander principle applies for this example: __There can only be one__                      
Next open a new terminal and run    
.    DO ##class(IJC.Demo).Sensor("mytext")      
and see what happens.     
       
It's clear that for real applications:  
- the monitor might run in a background tasks  
- the sensors will do something useful.     
But this reduces visibility. 
 
