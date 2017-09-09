==================================================================================
README INSTRUCTIONS
==================================================================================
CONTENTS
1.DESCRIPTION
2.BUILD INSTRUCTIONS
3.TEST INSTRUCTIONS
4.RUNNING THE APPLICATION
5.NOTES
==================================================================================
1. DESCRIPTION
The application is a simulation of a toy robot moving on a square tabletop, 
of dimensions 5 units x 5 units. There are no other obstructions on the table surface.
The robot is free to roam around the surface of the table, but must be prevented from 
falling to destruction. Any movement that would result in the robot falling from 
the table must be prevented, however further valid movement commands must still be allowed.
Requirements
Create an application that can read in commands of the following form:
PLACE X,Y,F
MOVE
LEFT
RIGHT
REPORT
 Where PLACE will put the toy robot on the table in position X,Y and facing 
	NORTH, SOUTH, EAST or WEST. The origin (0,0) can be considered to be 
	the SOUTH WEST most corner.
 It is required that the first command to the robot is a PLACE command, after that, 
	any sequence of commands may be issued, in any order, including another PLACE 
	command. The application should discard all commands in the sequence until a 
	valid PLACE command has been executed.
 Where MOVE will move the toy robot one unit forward in the direction it is 
	currently facing.
 Where LEFT and RIGHT will rotate the robot 90 degrees in the specified direction 
	without changing the position of the robot.
 Where REPORT will announce the X,Y and F of the robot. This can be in any form, 
	but standard output is sufficient.
 A robot that is not on the table can choose to ignore the MOVE, LEFT, RIGHT 
	and REPORT commands.
 Input can be from a file, or from standard input, as the developer chooses.
 Provide test data to exercise the application.
Constraints
The toy robot must not fall off the table during movement. This also includes the 
initial placement of the toy robot. Any move that would cause the robot 
to fall must be ignored.
==================================================================================
2. BUILD INSTRUCTIONS
please use maven to build the application using the command mvn clean install.
==================================================================================
3. TEST INSTRUCTIONS
please use maven to run the unit test scripts written for the application using 
the command mvn clean install.
==================================================================================
4. RUNNING THE APPLICATION
	a. 	Once the application is build, the executable jar will be available 
		in the target folder within the project.
 	b.	Please use the terminal and navigate to the target location mentioned above.
	c.	Use the command java -jar robot-demo-0.0.1-SNAPSHOT.jar to run the 
		application.
Please make sure Java is installed and available in your PATH environment variable
for the above command to work.
==================================================================================
5. NOTES
This is a spring boot application with Java 8. Maven is the build tool used.
As it is a production ready code logging is used.


