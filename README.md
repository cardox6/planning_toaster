# planning_toaster

Your Task: Write a planning algorithm for making toast!

Please use the attached python file. It contains states, actions, state transition function and goal function al prepared for you. You get to write a planning function.

The task comes in multiple difficulties:
- (Simple) Look over the file, understand how the formal setup of the planning problem has been implemented in Python.
- (Medium) Implement breadth first search (you may refer to the pseudo code).
- (Hard) find the plan that toasts bread the fastest by finding a solution where parameter "time" is minimal.
- (Very-Hard) Solve the hard task with an algorithm that needs as little run time as possible.


## A* Search with Heuristic

- testing: {'toaster_has_power': False, 'toaster_is_on': False, 'bread_location': 'plate', 'bread_state': 'untoasted', 'time': 0}
  
         found sequence: ['put_in_bread', 'plug_in_toaster', 'switch_on_toaster', 'wait', 'take_out_bread']
         runtime: 0.0012060999870300293 seconds
         fulfills goal? True
         in world time 14


- testing: {'toaster_has_power': True, 'toaster_is_on': False, 'bread_location': 'toaster', 'bread_state': 'untoasted', 'time': 0}

         found sequence: ['switch_on_toaster', 'wait', 'take_out_bread']
         runtime: 0.0006686329725198448 seconds
         fulfills goal? True
         in world time 12


- testing: {'toaster_has_power': True, 'toaster_is_on': True, 'bread_location': 'plate', 'bread_state': 'untoasted', 'time': 0}
  
         found sequence: ['unplug_toaster', 'put_in_bread', 'plug_in_toaster', 'switch_on_toaster', 'wait', 'take_out_bread']
         runtime: 0.0013730840291827917 seconds
         fulfills goal? True
         in world time 15


 - testing: {'toaster_has_power': False, 'toaster_is_on': True, 'bread_location': 'plate', 'bread_state': 'untoasted', 'time': 0}
   
         found sequence: ['unplug_toaster', 'put_in_bread', 'plug_in_toaster', 'switch_on_toaster', 'wait', 'take_out_bread']
         runtime: 0.0013879329781048 seconds
         fulfills goal? True
         in world time 15

## BFS Time Optimized
 - testing: {'toaster_has_power': False, 'toaster_is_on': False, 'bread_location': 'plate', 'bread_state': 'untoasted', 'time': 0}
   
         found sequence: ['plug_in_toaster', 'put_in_bread', 'switch_on_toaster', 'wait', 'take_out_bread']
         runtime: 0.00400552898645401 seconds
         fulfills goal? True
         in world time 14


 - testing: {'toaster_has_power': True, 'toaster_is_on': False, 'bread_location': 'toaster', 'bread_state': 'untoasted', 'time': 0}
   
         found sequence: ['switch_on_toaster', 'wait', 'take_out_bread']
         runtime: 0.0030718619818799198 seconds
         fulfills goal? True
         in world time 12


 - testing: {'toaster_has_power': True, 'toaster_is_on': True, 'bread_location': 'plate', 'bread_state': 'untoasted', 'time': 0}
   
         found sequence: ['unplug_toaster', 'plug_in_toaster', 'put_in_bread', 'switch_on_toaster', 'wait', 'take_out_bread']
         runtime: 0.003617484006099403 seconds
         fulfills goal? True
         in world time 15


 - testing: {'toaster_has_power': False, 'toaster_is_on': True, 'bread_location': 'plate', 'bread_state': 'untoasted', 'time': 0}
   
         found sequence: ['unplug_toaster', 'plug_in_toaster', 'put_in_bread', 'switch_on_toaster', 'wait', 'take_out_bread']
         runtime: 0.005143280955962837 seconds
         fulfills goal? True
         in world time 15


## BFS Optimized 

- testing: {'toaster_has_power': False, 'toaster_is_on': False, 'bread_location': 'plate', 'bread_state': 'untoasted', 'time': 0}
  
         found sequence: ['plug_in_toaster', 'put_in_bread', 'switch_on_toaster', 'wait', 'take_out_bread']
         runtime: 0.01822316600009799 seconds
         fulfills goal? True
         in world time 14


 - testing: {'toaster_has_power': True, 'toaster_is_on': False, 'bread_location': 'toaster', 'bread_state': 'untoasted', 'time': 0}
   
         found sequence: ['switch_on_toaster', 'wait', 'take_out_bread']
         runtime: 0.0011098409886471927 seconds
         fulfills goal? True
         in world time 12


 - testing: {'toaster_has_power': True, 'toaster_is_on': True, 'bread_location': 'plate', 'bread_state': 'untoasted', 'time': 0}
   
         found sequence: ['wait', 'put_in_bread', 'switch_on_toaster', 'wait', 'take_out_bread']
         runtime: 0.13135956297628582 seconds
         fulfills goal? True
         in world time 23


 - testing: {'toaster_has_power': False, 'toaster_is_on': True, 'bread_location': 'plate', 'bread_state': 'untoasted', 'time': 0}
   
         found sequence: ['plug_in_toaster', 'wait', 'put_in_bread', 'switch_on_toaster', 'wait', 'take_out_bread']
         runtime: 0.26640287501504645 seconds
         fulfills goal? True
         in world time 24

## BFS pseudo code


- testing: {'toaster_has_power': False, 'toaster_is_on': False, 'bread_location': 'plate', 'bread_state': 'untoasted', 'time': 0}
  
         found sequence: ['plug_in_toaster', 'put_in_bread', 'switch_on_toaster', 'wait', 'take_out_bread']
         runtime: 0.00400552898645401 seconds
         fulfills goal? True
         in world time 14


- testing: {'toaster_has_power': True, 'toaster_is_on': False, 'bread_location': 'toaster', 'bread_state': 'untoasted', 'time': 0}
  
         found sequence: ['switch_on_toaster', 'wait', 'take_out_bread']
         runtime: 0.0030718619818799198 seconds
         fulfills goal? True
         in world time 12


- testing: {'toaster_has_power': True, 'toaster_is_on': True, 'bread_location': 'plate', 'bread_state': 'untoasted', 'time': 0}
  
         found sequence: ['unplug_toaster', 'plug_in_toaster', 'put_in_bread', 'switch_on_toaster', 'wait', 'take_out_bread']
         runtime: 0.003617484006099403 seconds
         fulfills goal? True
         in world time 15


- testing: {'toaster_has_power': False, 'toaster_is_on': True, 'bread_location': 'plate', 'bread_state': 'untoasted', 'time': 0}
  
         found sequence: ['unplug_toaster', 'plug_in_toaster', 'put_in_bread', 'switch_on_toaster', 'wait', 'take_out_bread']
         runtime: 0.005143280955962837 seconds
         fulfills goal? True
         in world time 15
