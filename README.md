# Advanced-AI

Dead line : 11 nov for both groups (note book + report describing your mdp, including a drawing)

Consider a house-cleaning robot. It can be either in the living room or at its charging station - or out  of battery. 
The living room can be clean or dirty. So there are five states: LD(in the living room, dirty), LC(in the living room, clean), CD(at the charger, dirty), CC(at the charger, clean), O (out of power).


####  
When in the living room,    the robot  can either choose to clean or to charge. 

When in the charging station, the robot can either choose to clean or to keep charging.

When out of order, any of the two actions (clean, charge) leads to the same results: staying out of power

####  

The reward for being  in a clean state is rc 

The reward for being in a dirty state is rd < rc at each time step

The reward for being out of power is  costcrash  -  lower or equal to rd ; let us set it equal to rd  (the living rooms becomes dirty anyway)
 

####  

When  the robot decides to  clean,
*  if it is in the living room, then it may become out of power with proba e
*  if it is in the charging station, no risk of running out of power   
*  cleaning a clean floor leaves it clean
*  cleaning a dirty floor can sometimes fail (even is battery is ok) - let eps be the probability of fail of the cleaning
     
When  the robot decides to  charge,  action charge always takes the robot to the charging station. The  dirtiness of the room can go from clean to dirty with a probability  pDust  and it stays for sure at the dirty level if dirty
