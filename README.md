My name is Yehia Fahmy and this is my submission for the software training, started on Sept 22 2021

# This package aims to complete the following tasks

1. Clears any existing turtles
2. Create a component that moves 'turtle1' in a circular motion
3. Spawns a turtle named "stationary_turtle" at x = 5, y = 5
   Spawns a second turtle named "moving_turtle" at x = 25, y = 10
4. Create a service that resets the "moving_turtle" to its starting position. The service response should be whether or not it was successful.
5. Create a publisher that publishes a custom msg. This custom msgs should have 3 float fields that correspond with the x and y distances of "stationary_turtle" to "moving turtle", as well as the distance between the two turtles.

6. Create an action that moves "moving_turtle" to a waypoint in a straight line by publishing geometry_msgs/Twist msgs to turtleX/cmd_vel.The action's goal command is an absolute position of the waypoint, feedback is distance to the goal, and result is the time it took to reach the goal. You should define a custom action file. 